

Link to repo: https://github.com/briyoon/ECE551-Video-SegLinks to an external site.

 

This project takes previous course work and expands on it. In a previous course, I created a image segmentation annotation tool using SAM2. This semester, I added video annotation functionality. SAM2 natively supports video inference. It has a memory segment that uses past and future prompts to help identify objects. This required major changes and redesign of the workflow used for images. The video inference has to first load all of the frames into memory and then process them all for inference. Instead of recomputing after every prompt like for images, it instead batch updates once the user is ready to submit. There is also a frame scrubber to view each frame and playback the video. The annotations are exported as Youtube-VIS, which is a COCO style annotation.  I achieved around 0.85 J-score using the large SAM2 model to annotate 10 videos from the DAVIS 2017 train/val dataset. This tool retains the ease of use of a single docker compose command to run the app.

 

Heavy use of agentic AI was used for this feature update. Agentic AI focuses on using large language models to automate decision making to complete complex tasks. It works by first taking a user prompt describing what you would like it to accomplish. Then it creates artifacts such as an implementation plan and task list, then asking the user for review. This is where you go in and provide context and implementation details if it didn't quite nail it the first time. Once approved, the agent then starts writing code. Google has recently released Antigravity (Nov 18th 2025), an agentic IDE based off of a fork of Microsoft's VsCode. It allows users to use the new Gemini 3 Pro model to aid in AI assisted development. For example, from the previous version of the project, I asked

"take a current inventory of the code base. i need to add video functionality to both the back end and the front end. the backend needs similar functionality as the image parts, where i can annotate multiple classes etc. the front end needs some type of slick video playback where i can view frame by frame,displaying annotatiosn and prompts"

It then created the implementation plan and task file. After a few back and forth edits I let it start writing code. It initially had tons of issues with python environments, dependencies, and understanding which directory to run commands in (frontend vs backend). After explaining to it how the project is laid out a bit more, it spit out a couple hundred-line changes. Each change comes as a git diff, allowing you to easily see what has changed and accept or reject changes. This revision history is stored throughout the entire conversation, so you are able to review what the AI did at a later date. After the first pass, there were still tons of crashes in the backend. It took several more iterations for it to figure out how SAM2's video inference works. I eventually had to paste a small snippet from the SAM2 github for it to understand what it needed to do. After that there were minor feature implementation changes such as caching etc, but the agent was able to handle almost everything else with one or two tries. Here is another example of prompt + response:

"when a prompt is deleted, i ahev to move frames for it to update the annotations, also it shows the spinner on the left, so i need that to update when its deleted too to show when its done. also when manually srubbing the time line, the annotations lag, we can probably set seomthign up that when we receive a response from the server for the annotation, we make sure we are still on that frame before showing the annotation, that way we dont show annotations that dont match the frame from quick scrubbing the time line."

---
Thought for 8s


Implementing Deletion Refresh

I'm currently focused on the deletion refresh issue. I've pinpointed the need for a trigger to initiate the update after a prompt is deleted, and I'm figuring out how to integrate this with the existing frame move functionality. I'm also addressing the spinner behavior; it should now accurately reflect the re-computation status, starting when deletion is initiated and clearing once the process is complete.

Refining Spinner Behavior

The spinner issue with deletions is intriguing. I suspect the annotations_updated event from the backend isn't being correctly processed in the frontend context of a deletion. My current thinking is that while the queued.add call is functional, the event stream handler, responsible for removing from the queue and refreshing, might have a misconfiguration. I'm focusing my investigation on the backend's delete_video_prompt function and its emission of the annotations_updated event to ensure it mirrors the event sent with add_video_prompt. I'll trace this to see if the deletion event matches the existing event format.

Tracing Event Emissions

I'm now investigating the backend's delete_video_prompt function to ensure its event emission matches the add_video_prompt format. Following that, I'll scrutinize studio/+page.svelte for the "late frame check" logic needed within refreshAnnotations or drawOverlay. The goal is to verify that annotations displayed align with currentFrameIdx. I'll capture the requested frame index and compare it after the asynchronous getVideoAnnotation call.



Implementing Video Annotation Visualization
In prompt_router.py: delete_video_prompt calls _recompute_video_annotations(prompt.media_id). _recompute_video_annotations retrieves prompts: prompts = session.exec(select(VideoPrompt).where(VideoPrompt.media_id == media_id)).all()

The Issue: When deleting, if there are NO prompts left (user deleted the last one), prompts will be empty. In _recompute_video_annotations: if not prompts: session.exec(delete(VideoAnnotation)...) session.commit() return <-- RETURNS WITHOUT EMITTING EVENT! So if the user deletes the last prompt, the event is NEVER emitted! This explains why the spinner doesn't clear and annotations don't update (until manual refresh). I need to move the broker.emit call (or a variant of it) to ensure it fires even when prompts is empty. However, broker.emit needs project_id. If prompts is empty, I can't get prompts[0].project_id. I need to query the Media object (or get project_id passed into the function) to know where to emit. Usage in delete_video_prompt: prompt variable (the deleted one) has the project_id, but it's deleted from session. I'll update _recompute_video_annotations to verify media exists and fetch project_id from there (since  Media has project_id). This is safer. Then I'll fix the return statement to emit before returning. Wait, Media is fetched later media = session.get(Media, media_id). I should move this up.

Frontend Fix: In studio/+page.svelte:refreshAnnotations, I'll add const targetFrame = currentFrameIdx; and check if (targetFrame !== currentFrameIdx) return; after await. Also I'll modify deleteNearestPrompt to handle the spinner? No, queued.add is fine. The backend fix will solve the spinner getting stuck. And refreshAnnotations race condition fix addresses the "lag" / "scrolling" issue.

Plan:

Fix prompt_router.py: Ensure _recompute_video_annotations always emits
Fix studio/+page.svelte: Add frame index check to avoid race conditions.
Files Edited
+page.svelte
prompt_router.py
Progress Updates
1 Standardizing delete event in prompt_router and fixing frontend race conditions
2 Fixing delete event race condition in backend
I've implemented fixes for both issues:

Deletion Spinner / Update: The backend now properly sends the "updated" signal even when the last prompt is deleted, so the spinner will stop and annotations will clear immediately.
Scrubber Lag: The frontend now checks if the frame you are currently on matches the annotations it just received. If you've already scrubbed past that frame, it discards the old data, preventing "laggy" ghost annotations from flicking on screen.
Please restart the backend:

python app.py
And give it a rigorous test! Deleting prompts and fast scrubbing should feel smooth now.
---

This is a very comprehensive thought chain that allows me to follow along and check to make sure the models reasoning is correct.

 

This does bring up large concerns for use of AI in academia. I believe it is an inevitable force that will have to be accepted. However, if the user does not understand how to program, how to utilize best practices etc, they are at mercy of the generative AI to produce, maintain, and refactor code. It takes the user from the role of programming to someone how is designing and architecting code. To me, this seems like overlap with some 400 level CS courses. Thus, I believe AI should be allowed for explanations but not implementation until those 400 level classes are reached. Instead of a student being expected to understand syntax and boilerplate, manual debugging, and tool knowledge, it will eventually turn into them having to articulate their goals and vet the implementation plan with good software architecture. However, I would like to reiterate how important it is for the user to understand what the AI is doing. If you ask it to implement an algorithm, and it produces code with a slight bug, the focus now becomes debugging the code by either correcting its chain of thought or enabling it with the tools required to debug itself.
