# An Overview of Working with Google Colab Tutorials from PyTorch

The Pytorch website has many important tutorials that are worth
investigating. This section provides a summary of how to work with
them.\
Your initial steps involve:

1.  Create a Google Account

2.  Locate Google Drive on your account

3.  (Optional) Download App for linking to Google Drive on your
    computer.

Once you identify a tutorial, follow the steps below:

1.  Download the Google Colab notebook on your Google drive:

           Click on the filename to open the Google Colab notebook 
           Click on File
           Click on Save a copy in Drive

    This procedure will create a file named `Copy of Name.ipynb` in your
    `Colab Notebooks` directory in your Google drive. You can click on
    the filename `Copy of Name.ipynb` to rename the file.

2.  Run the Google Colab tutorial to see if it works!\
    If the tutorial fails, it is often because it requires special
    installations or a custom dataset. Follow the procedures below for
    each case.

3.  Custom package installations:\
    You can install packages using:

        !pip install package1 package2 ...

    After the installations are done, you can comment out these lines.
    If you do not comment, no harm is done!

4.  Custom datasets:\
    Mount Google Drive in your Google Colab using:

           import os
           from google.colab import drive

           drive.mount('/content/drive')
           os.chdir("/content/drive/MyDrive/Colab Notebooks")

    If you want to use another directory, then simply run:

          os.chdir("/content/drive/MyDrive/MyDirectoryNameHere")

    You can also figure out your current working directory using:

          !pwd

    You can look at the directory structure using:

          !ls

    You can move around different directories using:

          !cd DirectoryName

    Use `ls`, `cd`, `pwd` to figure out the directory and file
    structures. *Look for filenames and directories throughout the code
    and make sure you are loading them correctly.* Unzip the dataset in
    an appropriate directory that you can access.

5.  Run on GPUs\
    When running `torchivision_tutorial.ipynb`, the run would never get
    completed. It would take forever and never finish. After switching
    to a GPU, the code finished in a few minutes! Here is the process:

          Click on Runtime
          Click on Change runtime type
          Select T4 GPU
          Click Save

    Then run everything.

6.  (Optional) Download App for linking to Google Drive on your
    computer.

# PyTorch examples that have been tested

This section contains PyTorch examples that follow the general process
outlined above. For each tutorial, we outline what is needed to get them
running.

## Tutorials that run without any changes

-   Quickstart at [quickstart tutorial
    link](https://pytorch.org/tutorials/beginner/basics/quickstart_tutorial.html).

-   Tensors at [tensors
    link](https://pytorch.org/tutorials/beginner/basics/tensorqs_tutorial.html).

-   Datasets & DataLoaders at [data tutorial
    link](https://pytorch.org/tutorials/beginner/basics/data_tutorial.html).

-   Build the Neural Network at [build model
    link](https://pytorch.org/tutorials/beginner/basics/buildmodel_tutorial.html).

-   Optimizing Model Parameters at [model optimization
    link](https://pytorch.org/tutorials/beginner/basics/optimization_tutorial.html).

-   Tensorboard at [tensorboard
    link](https://www.tensorflow.org/tensorboard/tensorboard_in_notebooks).

## Model Understanding with Captum

1.  The tutorial is available at: [captum
    link](https://pytorch.org/tutorials/beginner/introyt/captumyt.html).

2.  For installations, you will only need:

        # Comment after you finish:
        !pip install torch torchvision captum matplotlib==3.3.4 Flask-Compress

3.  You will need to get the data from [data
    link](https://pytorch-tutorial-assets.s3.amazonaws.com/youtube-series/video7.zip).

4.  Follow the information on *Custom Datasets* given above.\
    You will need to unzip the files and copy them to the `data`
    directory as outlined above.

## TorchVision Object Detection Finetuning Tutorial 

1.  This tutorial is available at: [torchvision
    link](https://pytorch.org/tutorials/intermediate/torchvision_tutorial.html).

2.  Follow the information on *Custom Datasets* given above.\
    You can download the dataset as given by:

        !wget https://www.cis.upenn.edu/~jshi/ped_html/PennFudanPed.zip -P data
        !cd data && unzip PennFudanPed.zip
        !ls -al

    After downloading the dataset, there is no reason to download
    anything anymore. After executing the code, you can comment out the
    code above by placing \# before each line.

3.  Follow the instructions on how to *Run on GPUs.*

## Optimizing Vision Transformer Model for Deployment

1.  The tutorial is available at [vision transformer
    link](https://pytorch.org/tutorials/beginner/vt_tutorial.html).

2.  You need to install some packages as given by:

        !pip install torch torchvision timm pandas requests

3.  After executing the code, you can comment out the code above by
    placing \# before each line.

## Transfer Learning Tutorial

1.  The tutorial is given at [transfer learning
    link](https://pytorch.org/tutorials/beginner/transfer_learning_tutorial.html).

2.  Download its dataset from [dataset
    link](https://download.pytorch.org/tutorial/hymenoptera_data.zip).

3.  Follow the information on *Custom Datasets* given above.

## Adversarial Example Generation

1.  The tutorial is given at [adversarial
    example](https://pytorch.org/tutorials/beginner/fgsm_tutorial.html).

2.  Make sure to install Google Drive as given above and keep track
    where the files are.

3.  Make sure to download the file given from \"here\" in the text:
    `For simplicity, download the pretrained model here.` I saved it and
    unzipped it in my Google Drive.

4.  Follow the information on *Custom Datasets* given above.\
    To load the file, I had to change the filename to:

          pretrained_model = "lenet_mnist_model.pth.pt"

    The original tutorial was using `lenet_mnist_model.pth`. I had to
    change the filename to `lenet_mnist_model.pth.pt` for this to work.

# Other important libraries that we use

-   [Retinal face for face
    detection](https://github.com/serengil/retinaface)

-   Models for object detection, instance segmentation, image
    classification, pose estimation, and multi-object tracking can be
    found based on YOLO at [Ultralytics
    website](https://docs.ultralytics.com/).
