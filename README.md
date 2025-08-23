# projects
The goal of this repository is to support projects that use Python, AI, and Machine Learning.

# Project assignments
Requirements for project proposals, midterm presentations, and final presentations can be found in [project assignments webpage](https://github.com/pattichis/projects/blob/main/project-assignment.md). This readme file contains how-to tutorials to help you develop your project. Example projects are given at the end of this document.

## How to create a GitHub repo for your project
To create your own repo refer to the [GitHub guide](https://github.com/pattichis/projects/blob/main/GitHub.md).

## How to develop Google Colab tutorials for your project
In order to develop Google Colab tutorials for your own repo, refer to [Google Colab tutorial for repos](https://github.com/pattichis/projects/blob/main/Colab-tutorial.md).

## How to find datasets and models for your project
1. Search for [Papers with code](https://paperswithcode.com/). Look separately for Methods and Datasets.
2. Search for datasets, models, and dataset competitions on [kaggle](https://www.kaggle.com/).
3. Search for Computer Vision datasets on [PyTorch vision datasets website](https://pytorch.org/vision/stable/datasets.html).
4. Search for pretrained PyTorch models [PyTorch models website](https://pytorch.org/vision/stable/models.html).
   
## How to learn Python and Machine Learning from scratch
You can access a self-paced image-processing-based introduction to AI and Machine Learning through 
[my guided tutorial](https://github.com/pattichis/AIML)

## How to learn Machine Learning using the Hands-on Machine Learning tutorials and book
For more advanced work, refer to the Google Colab notebooks developed for [Hands on Machine Learning by Aurélien Géron](https://github.com/ageron/handson-mlp). 
To install the tutorials locally on your machine, execute:
  1. Follow [the installation instructions](https://github.com/ageron/handson-mlp/blob/main/INSTALL.md).<br>
     If you have trouble with the torchvision installation, you may want to consult the link:
     ```
     conda config --add channels conda-forge
     conda config --set channel_priority strict
     conda install torchvision
     ```
     This material is covered in [Conda trips and tricks](https://conda-forge.org/docs/user/tipsandtricks/)

     Here is a screen dump of my successful installation based on [anaconda prompt](https://github.com/pattichis/projects/blob/main/handson-install.md).
     
  2. To learn more about working with Anaconda environments, refer to [my installation guide](https://github.com/pattichis/projects/blob/main/Anaconda-installation-notes.md).
  3. Refer to my notes on working with [Jupyter notebooks](https://github.com/pattichis/projects/blob/main/Jupyter-Notebooks-Notes.md).

His book titled <i>Hands-on Machine Learning with Scikit-Learn and Pytorch: Concepts, Tools, and Techniques To... Build Intelligent Systems</i>
can be accessed for free through [UNM library links to O'Reilly books, IEEE, etc](https://libguides.unm.edu/computer-science)

The original Scikit-Learn website has outstanding tutorials for Machine Learning. They can be found at [Scikit Learn website](https://scikit-learn.org/stable/).

Similarly, the [official PyTorch website](https://pytorch.org/) is a great place to start.

## How to run Google Colab tutorials available on the PyTorch website
Refer to my guide on how to mount datasets using Google Drive and how to test official PyTorch tutorials based on 
[my Colab guide for PyTorch](https://github.com/pattichis/projects/blob/main/Colab-Pytorch.md)

## How to learn more about Machine Learning and Statistical Learning theory using other recommended books
For the statistical foundations of AI and Machine Learning methods, I use [An Introduction to Statistical Learning](https://www.statlearning.com/). You can download the PDF of the book for free. The accompanying Python labs are excellent and demonstrate several essential concepts.

An accessible reference to modern AI/ML concepts can be found in [Deep Learning: Foundations and Concepts](https://www.bishopbook.com/). The book is freely available online.

One of my students found the Understanding Deep Learning book by Simon J.D. Prince to be highly accessible. This book can be accessed from [GitHub link](https://udlbook.github.io/udlbook/).

At UNM, you can openly access the book by Professor Martínez-Ramón who teaches our Deep Learning course. His book, co-authored with UNM students alumni, is titled at <i>Deep learning : a practical introduction / Manel Martínez-Ramón, Meenu Ajith, Aswathy Rajendra Kurup</i>. You can access it through [link](https://research.ebsco.com/c/kov46v/search/details/j5rkgtpylz?limiters=FT1%3AY&q=Manel%20Martinez-Ramon%20Deep%20Learning). If the link does not work, search for it through the [UNM library link](https://library.unm.edu/).


## Sample projects

<b>Audio classification by Benjamin Metzner</b><br>
This GitHub demonstrates the new required format for GitHub projects for ECE 551. 
There are separate modules for data loading, training, and testing. Refer to 
[audio classification project based on separate modules](https://github.com/bman222112/ECE551)

<b>Video segmentation using SAM (complete) and SAM2 (incomplete) by Brian McCollum</b><br>
This GitHub demonstrates the use of foundation models to provide ground truth.
It can be accessed through [video segmentation project](https://github.com/briyoon/ECE551-Video-Seg)

<b>Custom dataset for image classification by James Griego</b>  
This early GitHub provides essential information on how to build a 
[custom dataset for image classification using open datasets](https://github.com/jgreg4/ML-ImageClassify-Tutorial).

<b>Custom dataset for 1000 handwritten digit images captured by Raphael Perea</b><br>
This GitHub provides information on how to build a dataset based on your own images.
It can be accessed through
[custom dataset based on 1000 handwritten digit images](https://github.com/perear2/Custom-Dataset-Tutorial).

<b>Mars image segmentation by Ary Naim<b><br>
This GitHub provides an [image segmentation example](https://github.com/naimaryan1/LunarMUnet).
You can directly run the tutorial based on the [Google drive link](https://colab.research.google.com/drive/1aiZMAFvt1e5_HM59oQ0EtJy6HIflzMpB?usp=sharing).
