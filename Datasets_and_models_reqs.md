# Requirements

The project requires a short description of your dataset. At the project
proposal time, you will need to briefly describe how you want to address
these requirments. Clearly, you will not fully understand what each
model means when you prepare your project proposal. You will need to
meet the full requiremetns in your final project description.

The advise is to focus on working with digital videos (and possibly
associated audio). However, you can use standard image datasets to help
you find objects in videos. A good idea is to post-process the results
that you get from different video frames to provide a better result over
the video. In other words, consider building a video object detector
based on still image object detection. For example projects, please
refer to the subsections of this document.

To describe the source of your datasets, consider:

-   **External datasets**: Provide web-links and a brief summary for
    each dataset. In addition to the web-link, you may have to supply
    the keywords that you used to obtain the dataset.

    You can find the standard datasets on PyTorch or Tensorflow. For
    videos, consider searching the YouTube-8M Video dataset from
    <https://research.google.com/youtube8m>. You can also find datasets
    on Kaggle.

-   **Transfer learning datasets**: For student projects, it is very
    likely that your datasets will be very small. In this case, you will
    want to find a dataset that closely resembles your dataset. You will
    need to explain the differences between the project dataset and the
    training dataset.

-   **Models come with datasets**: For transfer learning, we often
    consider pre-trained models. You must clearly indicate the dataset
    that each model was pre-trained on.

    For image classification problems, consider YOLO, VGG-16, and Faster
    R-CNN. For video activity recognition problems, consider TSN,
    Slowfast & Slowonly, and I3D. You will need to provide brief
    descriptions for these models (e.g. , number of parameters, number
    of layers, whether they are based on ResNet, Inception, etc).

-   **User-generated data**:

    -   Explain the **need**. You need to justify why you need to
        collect a new dataset. Specifically, you need to make a
        statement that you could not find a dataset that addressess your
        need.

    -   **Data collection protocol**: Explain how you are going to
        collect the datasets. Here, you will need to provide:

        -   Camera model with brief summary.

        -   Light source descriptions.

        -   Brief scene description.

        -   Camera or object motions to understand the acquisition
            angle.

        -   Image or video source formats (e.g., png, tiff, jpeg
            (avoid), mp4, h264).

    -   **Data examples** : Once you have collected some data (after the
        project proposal), you will need to provide examples of the data
        with descriptions.

You will need to document your dataset using at-least one Figure. This
Figure should contain a small number of representative examples that
capture the variation of your dataset (e.g., changes under scaling,
translations, and rotations). You should also provide examples from the
different categories.

For your project, you will need to clearly summarize the following:

-   **Training dataset**: Clearly indicate which part of the data you
    will be using for **model fitting** and **model validation** (e.g.,
    80% for fitting and 20% for validation).

-   **Testing dataset**: Clearly indicate how you want to test your
    final model. Remember that the final model is trained over the
    entire training dataset. Your testing dataset needs to be
    sufficiently complex to capture the variations of actual data.

You are required to provide the metrics that you are using to evaluate
performance. The standard metrics include:

-   **AUC**: This is the standard metic for comparing classifiers with
    one metric.

-   **ROC curves**: This is used to understand different performance
    points.

-   **Object and activity detection**: We usually use **intersection
    over union** \>0.5 to denote successful detection.

-   **Confusion matrix**: This is the standard metric for reporting
    results for more than one category.

## Examples of Basic Video Processing Problems involving Humans

Face

:   recognition in digital videos. There are several face recognition
    datasets and methods to consider. The development of video based
    methods is very interesting.

Person

:   detection and tracking in the wild.

Pose estimation in the wild

:   is used here to refer to the problem of understanding where people
    are looking. Examples include looking at another person, looking at
    the keyboard, or looking at a piece of paper.

Emotion recognition

:   The goal is to determine the emotional state from still images of
    the face (e.g., happy, sad, etc). You can find many datasets for
    this problem. In digital videos, identify the emotions associated
    with each video frame.

## Examples of Video Activity Recognition Problems

Talking:

:   The goal is to identify when someone is talking.

Typing:

:   These videos should include hands and keyboards.

Writing:

:   The goal of this activity is to detect people writing on paper.

Pointing:

:   The goal of this activity is to detect when someone is pointing to a
    computer screen or another person.

Hand gestures:

:   The goal here is to detect hand activities where a student or an
    instructor uses his or her hands to describe a concept.
