# Required descriptions for models and datasets for your project

The project requires a short description of your datasets. 
Modern AI and Machine Learning projects involve the use of multiple datasets.
Here are some examples:
* Datasets:
  You need to make sure that there are no overlaps between the training, validation,
  and testing datasets.
* Transfer learning training:
  In this example, you will find a model pre-trained on a large dataset and
  then adapt the top layer for a different dataset.
* Out of distribution testing:
  A mature model will be trained on a dataset from a specific sourse (e.g., a clinic)
  and be tested on a dataset from a different source (e.g., another clinic). This practice is called
  out-of-distribution testing. Ultimately, what matters most is how a model performs in
  out-of-distribution testing.
* Training and performance of foundation models on multiple tasks:
  In this example, you would pre-train a model on several datasets and then adjust your model
  for testing on another set of datasets. Here, you would need to explore how to train large
  models.

At the project proposal time, you will need to briefly describe how you want to address
these requirements. Clearly, you will not fully understand what each
model means when you prepare your project proposal. You will need to
meet the full requirements in your final project description.

To describe the source of your datasets, consider:

-   **External datasets**: Provide web-links and a brief summary for
    each dataset. In addition to the web link, you may need to supply
    the keywords that you used to obtain the dataset.
    You can find the standard datasets on PyTorch, Tensorflow, or Kaggle.

-   **Transfer learning datasets**: For student projects, it is very
    likely that your datasets will be very small. In this case, you will
    want to find a dataset that closely resembles your dataset. You will
    need to explain the differences between the project dataset and the
    training dataset.

-   **Models come with datasets**: For modern AI and Machine Learning models, we often
    consider pre-trained models. You must clearly indicate the dataset
    that each model was pre-trained on.

    Many modern models are based on Transformers. Consider the use
    of Vision Transformers for your project. Additionally, consider models
    based on YOLO, VGG-16, and Faster-CNN. Please refer to the main
    project website for models and datasets. You will need to provide brief
    descriptions for these models (e.g. , number of parameters, number
    of layers, whether they are based on ResNet, Inception, etc).

-   **User-generated data**:

    -   Explain the **need**. You need to justify why you need to
        collect a new dataset. Specifically, you need to make a
        statement that you could not find a dataset that addresses your
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

    -   **Data examples**: Once you have collected some data (after the
        project proposal), you will need to provide examples of the data
        with descriptions.

You will need to document your dataset using at least one Figure. This
Figure should contain a small number of representative examples that
capture the variation of your dataset (e.g., changes under scaling,
translations, and rotations). You should also provide examples from the
different categories.

For your project, you will need to clearly summarize the following:

-   **Training datasets**: Clearly indicate which part of the data you
    will be using for **model fitting** and **model validation** (e.g.,
    80% for fitting and 20% for validation).

-   **Testing datasets**: Clearly indicate how you want to test your
    final model. Remember that the final model is trained over the
    entire training dataset. Your testing dataset needs to be
    sufficiently complex to capture the variations of actual data.

You'll need to provide the metrics that you're using to evaluate
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

Face recognition in digital videos. There are several face recognition
    datasets and methods to consider. The development of video based
    methods is very interesting.

Person detection and tracking in the wild.

Pose estimation in the wild is used here to refer to the problem of understanding where people
    are looking. Examples include looking at another person, looking at
    the keyboard, or looking at a piece of paper.

Emotion recognition: The goal is to determine the emotional state from still images of
    the face (e.g., happy, sad, etc). You can find many datasets for
    this problem. In digital videos, identify the emotions associated
    with each video frame.

## Examples of Video Activity Recognition Problems

Talking: The goal is to identify when someone is talking.

Typing: These videos should include hands and keyboards.

Writing: The goal of this activity is to detect people writing on paper.

Pointing: The goal of this activity is to detect when someone is pointing to a
    computer screen or another person.

Hand gestures: The goal here is to detect hand activities where a student or an
    instructor uses his or her hands to describe a concept.
