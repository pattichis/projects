# Projects
The goal of this repository is to support projects that use Python, AI, and Machine Learning.<br />
🔴 Click on the Outline button (upper-right button in GitHub) for a table of contents and to jump to a particular topic.<br />
🔴 Right-click on each link to open in a new browser window.

# Final Project Presentation and Deliverables
## 1. Final presentation
All projects must be presented. You must select a presentation time.
An individual project gets 15 minutes. A group project of 2 or more must reserve 30 minutes.
A separate link to a sign-up sheet is provided in the class assignment.  
Make sure to select a presentation spot before the deadline. 
If none of the times work for you, please contact the instructor immediately.
You will receive zero credit if you do not present your project.

If you choose to deliver a list of Google Colab tutorials instead of a paper refer to 
[detailed requirements for Google Colab](https://github.com/pattichis/projects/blob/main/Colab-tutorial-list.md).

### Presentation guidelines
You must keep track of the feedback received during your presentation. 
You will be expected to address the feedback in your final submission.
You will have 15 minutes. Use 10 minutes for the presentation and 5 minutes for questions.

For a basic review method presentation, here is the recommended slide layout:
*	Title slide with your name, title, date
*	Outline slide summarizing the different parts of your talk
*	Introduction and Motivation of the Problem
*	Background: Existing or competitive methods and what they have missed
*	Proposed Method described via flow-chart or pseudocode
*	Results including side-by-side comparisons with alternative methods (if possible)
*	Discussion of your results and how they relate to other methods
*	Concluding remarks summarizing your accomplishments and proposed future work

For a basic review paper presentation, here is the recommended slide layout:
*	Title slide with your name, title, date
*	Outline slide summarizing the different parts of your talk
*	Introduction and motivation for the review: Why is this area still relevant? Why do you expect this area to grow? 
*	Background: A summary of older methods that are much older, classical, and will not be the focus of this review. 
*	Current Systems: An outline of common components and characteristics of most current systems. Carefully provide choices for the different components. You can demonstrate some basic components 
*	Emerging Systems: Show some more recent systems that are significantly different that most “deployed” systems and how they differ
*	Future Directions and Open problems in the area
*	Concluding remarks summarizing problems that you consider closed and where the growth is likely to be


## 2. Feedback response document
During the presentation, I will ask questions about different aspects of the project.
You will be required to provide a <b>response document</b> that addresses the questions made during the presentation. 

## 3. Final deliverables
You have to submit:
1. Final presentation slides.
2. Feedback response document.<br />
   Provide a separate document summarizing changes suggested during your presentation.
4. Final paper and/or GitHub link (see below)
5. Groups only: provide a statement detailing efforts by different group members.

The final paper page limit is 5 pages for a standard project.
For group projects, the limit is 10 pages.
You can also use unlimited pages of appendices to describe the code or datasets.
The final paper needs to follow the IEEE paper formatting guidelines.
Here is a list of other suggested guidelines:
•	You can follow your presentation guidelines on how to organize your paper
•	Follow the lectures on how to write the paper
•	IEEE Journal format required and IEEE-style transactions and journal paper references
•	Must clearly show and discuss the database of images that you are working with
•	Must show a flow-chart and/or pseudo-code of the methods
•	Must have comparisons with different methods or a discussion of how other methods perform 

For the Google Colab tutorials list you can find [detailed requirements for Google Colab](https://github.com/pattichis/projects/blob/main/Colab-tutorial-list.md).

# Project Proposals Guide
1. [Project proposal assignment](https://github.com/pattichis/projects/blob/main/proposal.md)
2. [Check if you can run your project on your computer](https://www.canirun.ai/)
3. See notes above on how to access different guides for the project.
4. You can see sample projects at the end of this document.

# Installations and Tutorials
## Install Anaconda and Jupyter notebooks
1. [Install Anaconda with necessary packages](https://github.com/pattichis/projects/blob/main/Anaconda-installation-notes.md).
2. [Tutorial for using Jupyter notebooks](https://github.com/pattichis/projects/blob/main/Jupyter-Notebooks-Notes.md).

## How to learn Python and Machine Learning for processing images and videos from scratch
You can access a self-paced image-processing-based introduction to AI and Machine Learning through 
[my guided tutorial](https://github.com/pattichis/AIML)


## How to learn Machine Learning using the Hands-on Machine Learning tutorials and book
For more advanced work, refer to the Google Colab notebooks developed for [Hands-On Machine Learning with Scikit-Learn and PyTorch: Concepts, Tools, and Techniques to Build Intelligent Systems by Aurélien Géron](https://github.com/ageron/handson-mlp). 
To install the tutorials locally on your machine, execute:
Follow [the installation instructions](https://github.com/ageron/handson-mlp/blob/main/INSTALL.md).<br>
If you have trouble with the torchvision installation, you may want to consult the link:
     ```
     conda config --add channels conda-forge
     conda config --set channel_priority strict
     conda install torchvision
     ```
This material is covered in [Conda trips and tricks](https://conda-forge.org/docs/user/tipsandtricks/)

Here is a screen dump of my successful installation based on [anaconda prompt](https://github.com/pattichis/projects/blob/main/handson-install.md).

His book titled <i>Hands-on Machine Learning with Scikit-Learn and Pytorch: Concepts, Tools, and Techniques To... Build Intelligent Systems</i>
can be accessed for free through [UNM library links to O'Reilly books, IEEE, etc](https://libguides.unm.edu/computer-science)

The original Scikit-Learn website has outstanding tutorials for Machine Learning. They can be found at [Scikit Learn website](https://scikit-learn.org/stable/).

Similarly, the [official PyTorch website](https://pytorch.org/) is a great place to start.

## How to run Google Colab tutorials available on the PyTorch website
Refer to my guide on how to mount datasets using Google Drive and how to test official PyTorch tutorials based on 
[my Colab guide for PyTorch](https://github.com/pattichis/projects/blob/main/Colab-Pytorch.md)

## How to learn more about Machine Learning and Statistical Learning theory using other recommended books
For the statistical foundations of AI and Machine Learning methods, I use [An Introduction to Statistical Learning](https://www.statlearning.com/). You can download the PDF of the book for free. The accompanying Python labs are excellent and demonstrate several essential concepts.

A book that covers learning theory from a probabilistic perspective, including important inequalities, I recommend 
is [Learning Theory from First Principles, Francis Bach, MIT Press, 2025](https://www.di.ens.fr/~fbach/ltfp_book.pdf)
(PDF link provided).

An accessible reference to modern AI/ML concepts can be found in [Deep Learning: Foundations and Concepts](https://www.bishopbook.com/). The book is freely available online.

One of my students found the Understanding Deep Learning book by Simon J.D. Prince to be highly accessible. This book can be accessed from [GitHub link](https://udlbook.github.io/udlbook/).

An excellent openly available textbook for modern Computer Vision is freely available at [computer vision book](https://visionbook.mit.edu/):
     ```
     Foundations of Computer Vision by Antonio Torralba, Phillip Isola,
     and William Freeman, MIT Press.
     ```

A sequence of openly available and accessible books can be found at:
 ["Probabilistic machine learning”: a book series by Kevin Murphy](https://probml.github.io/pml-book/):
```
Book 0: “Machine Learning: A Probabilistic Perspective” (2012)
Book 1: “Probabilistic Machine Learning: An Introduction” (2022)
Book 2: “Probabilistic Machine Learning: Advanced Topics” (2023)
```
I believe that the [introductory book](https://probml.github.io/pml-book/book1.html) and [advanced topics book](https://probml.github.io/pml-book/book2.html) are essential reading!

At UNM, you can openly access the book by Professor Martínez-Ramón who teaches our Deep Learning course. His book, co-authored with UNM students alumni, is titled at <i>Deep learning : a practical introduction / Manel Martínez-Ramón, Meenu Ajith, Aswathy Rajendra Kurup</i>. You can access it through [link](https://research.ebsco.com/c/kov46v/search/details/j5rkgtpylz?limiters=FT1%3AY&q=Manel%20Martinez-Ramon%20Deep%20Learning). If the link does not work, search for it through the [UNM library link](https://library.unm.edu/).

The following textbook contains simple explanations to many essential concepts:
   ```Machine Learning Q and AI by Sebastian Raschka.```
It is available at [Oreilly link](https://learning.oreilly.com/library/view/machine-learning-q/9781098168827/).
For UNM students, it is available for free through [UNM library links to O'Reilly books, IEEE, etc](https://libguides.unm.edu/computer-science).



# Project assignments
Requirements for project proposals, midterm presentations, and final presentations can be found in [project assignments webpage](https://github.com/pattichis/projects/blob/main/project-assignment.md). This readme file contains how-to tutorials to help you develop your project. Example projects are given at the end of this document.

## How to create a GitHub repo for your project
To create your own repo refer to the [GitHub guide](https://github.com/pattichis/projects/blob/main/GitHub.md).

## How to develop Google Colab tutorials for your project
In order to develop Google Colab tutorials for your own repo, refer to [Google Colab tutorial for repos](https://github.com/pattichis/projects/blob/main/Colab-tutorial.md).

## How to find datasets and models for your project
1. Special GitHub for [Medical image and video analysis projects (including regular images and videos)](https://github.com/pattichis/AIM/edit/main/README.md)
2. Special GitHub for [PyTorch model optimization](https://github.com/pattichis/AIMV/blob/main/opt.md).
3. Search for Datasets on [Google Dataset Search](https://datasetsearch.research.google.com/).
4. Search for [Papers with code](https://paperswithcode.com/). Look separately for Methods and Datasets.
5. Search for datasets, models, and dataset competitions on [kaggle](https://www.kaggle.com/).
6. Search for Computer Vision datasets on [PyTorch vision datasets website](https://pytorch.org/vision/stable/datasets.html).
7. Search for pretrained PyTorch models [PyTorch models website](https://pytorch.org/vision/stable/models.html).
8. You can start with well-developed tutorials from [PyTorch Hub](https://pytorch.org/hub/). 
   
## Toolboxes for specific Applications
### TorchIO for 3D Medical Imaging Transformations and MRI image intensity variations 
* [TorchIO](https://github.com/TorchIO-project/torchio)

# Sample projects
<b>Using VGGT and Affine Transformations on Point Clouds by Jason Wiberg</b><br>
Within VGGT_Tutorial.ipynb you can learn to use VGGT to generate point clouds from images, and align the point clouds to specified coordinate systems that can correspond to real-world geometry. Then, you can also try to use generative AI models like Qwen-Image_edit-2509 and specialized Loras to generate images of a scene from different angles. Use the generated images to improve VGGT inference on the original image
[GitHub](https://github.com/JasonWiberg/VGGT-and-Affine-Transformations-Tutorial)


<b>RF signal classification by Markus Parrish</b><br>
This project presents the development and evaluation of machine learning models for identification of radio–frequency (RF) signals, with a focus on
Automatic Modulation Classification (AMC) using the RadioML 2016.10A dataset.
[Tutorial: Automatic Modulation Classification Analysis of Traditional and Deep Learning Methods](https://github.com/Koosmaster/Tutorial-Automatic-Modulation-Classification/tree/main)

<b>Audio classification by Benjamin Metzner</b><br>
This GitHub demonstrates the new required format for GitHub projects for ECE 551. 
There are separate modules for data loading, training, and testing. Refer to 
[audio classification project based on separate modules](https://github.com/bman222112/ECE551)

<b>Video segmentation using SAM (complete) and SAM2 (incomplete) by Brian McCollum</b><br>
This GitHub demonstrates the use of foundation models with FastAPI to provide ground truth.
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
