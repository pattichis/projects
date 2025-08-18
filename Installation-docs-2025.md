# Install Anaconda

Consult the official PyTorch installation instructions from
`GET STARTED`. This is currently given at [PyTorch Get Started
Locally](https://pytorch.org/get-started/locally/). It is recommended
for you to download the latest version identified as: [Anaconda
individual licence](https://www.anaconda.com/products/individual).
Scroll down to the end of the page and select the latest Python and a
`64-Bit Graphical Installer`. I did not find any issues against the
official PyTorch installation instructions here.

## Anaconda on MacOS

### Optional: Uninstall older versions

On MacOS, I first removed the previous installation using:

    Open Finder and Go to the Applications folder.
    Move the Anaconda Navigator to the trash and empty the trash.

I then had to remove the anaconda3 folder using:

    cd /opt
    sudo rm -rf anaconda3

### Install new Anaconda using Command Prompt

I installed Anaconda manually using:

    curl -O https://repo.anaconda.com/archive/Anaconda3-2024.10-1-MacOSX-arm64.sh
    cd /opt
    bash Anaconda3-2024.10-1-MacOSX-arm64.sh

# Freely available books and required book example downloads

We have two books that should be available from the UNM library:\
1. *Hands-On Machine Learning with Schikit-Learn & Tensorflow*, 3rd
edition.\
2. *Programming PyTorch for Deep Learning: Creating and Deploying Deep
Learning Applications*\
3. *Machine Learning with PyTorch and Scikit-Learn: Develop machine
learning and deep learning models with\
Python* by Sebastian Raschka (Author), Yuxi (Hayden) Liu (Author), Vahid
Mirjalili (Foreword).\
All three books are freely available to all UNM students. To access
them, simply go to [UNM library link](https://libguides.unm.edu/Safari).
There are several other Python textbooks available through this link.
The current tutorial is based on the second book (2019). However, I
really like the material in the third book (2022). The first book is the
one that I used for my lecture notes (2022). Unfortunately, it does not
cover PyTorch. It only covers Scikit Learn.

The books come with github accounts that provide the code examples. In
class, we will be using the examples from the Hands-on book that is
based on: [Hands-on github for 3rd
edition](https://github.com/ageron/handson-ml3) . You can run these
examples directly using Google Colab. However, you can also install the
necessary packages and run them on your local machine as given here. If
a package is missing, you should be able to install additional packages
based on a similar approach as the one given here.

If you are interest in the PyTorch book, refer to [PyTorch
github](https://github.com/falloutdurham/beginners-pytorch-deep-learning).

# Simple Installation of PyTorch (NO C++ or source)

The basic idea here is to create an environment where you can install
everything you need to run your code. You can then delete the
environment if things do not work out and try again. You can install
elements of your environment using the graphical interface of Anaconda.
This is very nice and convenient. Here, I will cover how to install the
environments using the command prompt.

## Basic Packages

The following installation uses `conda` commands. You can download the
Anaconda environment cheatsheet from [ Anaconda Cheatsheet
Link](https://docs.conda.io/projects/conda/en/4.6.0/_downloads/52a95608c49671267e40c689e0bc00ca/conda-cheatsheet.pdf).
Run `Anaconda Prompt (Anaconda 3)` as Administrator. Then, in the
prompt, type:

    (base) ...>conda create --name pytorch
    (base) ...>conda activate pytorch
    (pytorch) ...>conda install opencv
    (pytorch) ...>conda install -c conda-forge jupyterlab
    (pytorch) ...>conda install pandas
    (pytorch) ...>conda install statsmodels
    (pytorch) ...>conda install -c conda-forge matplotlib
    (pytorch) ...>conda install jupyter

Follow the official PyTorch installation instructions from
`GET STARTED`. This is currently given at [PyTorch Get Started
Locally](https://pytorch.org/get-started/locally/). In 2025, the
installation is simplified to:

    conda install pytorch torchvision -c pytorch

Test the installation using:

    (pytorch) ...>python
    >>>import torch
    >>>
    >>>exit()
    (pytorch) ...>cd to-your-Python-notebook-directory
    (pytorch) ...>jupyter notebook

## Missing a package?

When running code in Python, you may get an error from a command such
as:

    import <library-name>

or similarly from a command such as:

    from <library-name> import <function-name>

In these cases, you can often fix the error by installing it in your
environment. For example, the following **command prompt code** often
works:

    (base) ...>conda activate pytorch
    (pytorch) ...>conda install <library-name>

If this does not work, you can search for the missing library using
Google and figure out how to install the correct library.

## Spyder: An Interactive Python Editor

Spyder allows us to run interactive examples. As before, run Anaconda
Prompt as an Administrator and do:

    (base) ...>conda activate pytorch
    (pytorch) ...>conda install spyder
    spyder

## Running PyTorch after installation

Every time you need to login, simply follow:

    Run the Anconda Prompt.
    Then switch to the pytorch environment using:
    (base) ...>conda activate pytorch
    conda install -c conda-forge jupyterlab

    (pytorch) ...>jupyter notebook

### Reinstall if you update the Operating System

Note that OpenCV uses low-level functions. If you updated the Operating
System between installations, you will need to re-install OpenCV.
Alternatively, you may want to create a new Anaconda environment and
re-install OpenCV so that you do not lose your work in other
environments.

## Remove Anaconda Environment if something goes wrong 

Make sure to restart Anaconda Prompt as Administrator. Then type:

    conda env remove --name pytorch

You can then restart the installation process. You will get a warning
that the pytorch directory exists. This is fine. You can overwrite it.

# Installation of PyTorch from Source and Purchasing NVIDIA GPUs

This process is covered in detail in [PyTorch from
source](https://github.com/pytorch/pytorch#from-source). This is not
covered here. However, note that you will need:

-   Python 3.8 or later.

-   C++17 compiler (gcc 9.4.0 or later).

-   For CUDA: NVIDIA CUDA, cuDNN v8.5 or later, CUDA compiler\
    Make sure to purchase a CUDA GPU board that supports this.

-   For AMD: AMD ROCm 4.0 or later (Linux only)\
    Make sure to purchase an AMD GPU board that supports this.

For NVIDIA GPUs, refer to:

-   PyTorch information at [ NVidia Developer
    Information](https://developer.nvidia.com/deep-learning-frameworks).

-   Compatibility information at [NVidia
    Compatibility](https://docs.nvidia.com/deeplearning/frameworks/support-matrix/index.html).

-   NVIDIA GPUs at [NVidia
    link](https://resources.nvidia.com/l/en-us-gpu).

# Install Scikit Learn and run some demos

The following instructions will allow you to run some basic demos in
Scikit Learn. First, you can leave the current environment using:

    (pytorch) ...>conda deactivate

We then want to create the sklearn-env and install some basic packages:

    (base) ...>conda create -n sklearn-env -c conda-forge scikit-learn
    (base) ...>conda activate sklearn-env
    (sklearn-env) ...>conda install -c conda-forge jupyterlab
    (sklearn-env) ...>conda install matplotlib
    (sklearn-env) ...>conda install anaconda::seaborn
    (sklearn-env) ...>conda install scikit-image

You can now review some important demos from sklearn.

    1. Navigate in the Scikit Learn website to find a demo that you like to see.
    2. Click on Download Jupyter notebook to save the file to run.

You can then run the demo by navigating to the directory where the file
was saved and then running:

    (base) ...>conda activate sklearn-env
    (sklearn-env) ...>jupyter-lab

Then open the file locally and run it.

## Topological Data Analysis

Click here for information about installing [Topological Data Analysis
in Scikit Learn](https://docs.scikit-tda.org/en/latest/). I installed
all libraries given in [Library
link](https://docs.scikit-tda.org/en/latest/libraries.html):

    (base) ...>conda activate sklearn-env
    (sklearn-env) ...>pip install scikit-tda
    (sklearn-env) ...>pip install ripser
    (sklearn-env) ...>pip install kmapper
    (sklearn-env) ...>pip install persim
    (sklearn-env) ...>pip install dreimac
    (sklearn-env) ...>pip install cechmate
    (sklearn-env) ...>pip install tadasets

I then followed the code given at [Tutorials
link](https://docs.scikit-tda.org/en/latest/notebooks/scikit-tda%20Tutorial.html).

The graph tutorials required special treatment. I had to run:

    (sklearn-env) ...>pip install -force-reinstall "networkx<2.7"

I then had to download [Graph datasets
link](https://github.com/KostyaLyman/scikit-tda/tree/master/docs/data)
into the local directory so that I could run the Graph examples.

I saved the running code in `tda-tutorial.ipynb`.

After that, I had to edit line 703 of `nx_pylab.py` located at
` /anaconda3/envs/sklearn-env/lib/python3.13/site-packages/networkx/drawing`
to make sure that `np.all` replaced `np.alltrue`.

## Successful Demos

After the installation described here, I managed to get the following
demos to work:

-   cluster comparison demos using [ Scikit learn for Cluster comparison
    code](https://scikit-learn.org/stable/auto_examples/cluster/plot_cluster_comparison.html)

-   Classifier comparisons using [classification comparison
    link](https://scikit-learn.org/stable/auto_examples/classification/plot_classifier_comparison.html).

-   Coin segmentation example using [ Coin Segmentation
    example](https://scikit-learn.org/stable/auto_examples/cluster/plot_coin_segmentation.html)

# Working with different environments

    >conda activate
    (base) ...>conda info --envs
    ... environment names
    (base) ...>conda activate <environment-name>

# Uninstalling Anaconda

If you update your Operating System, Anaconda may fail to load. In this
case, follow the information given in [ NVidia uninstall
link](https://docs.anaconda.com/free/anaconda/install/uninstall/).

# Working with OpenCV libraries

The following instructions allow you to download OpenCV from [OpenCV
link](https://github.com/opencv/opencv):

      Go to https://github.com/opencv/opencv
      Click on "<> Code"
      Click Download ZIP
      Open the ZIP file in the local directory

After unzipping, navigate to `/opencv-4.x/samples/python`.\
You can **run the demos one-by-one using**:

    (base) ...>conda activate pytorch
    (pytorch) ...>python demo.py

However, I also provide some important demos below.\
Please note that if you run into problems accessing the image files, you
will need to add (depends on the shell program that you are running):

     Export OPENCV_SAMPLES_DATA_PATH=/path-to-opencv/opencv-4.x/samples/data

If you still have issues, then you want to look at the source code in
Python, identify the filename that OpenCV is looking for, and copy it to
your Python directory.

For example, the following line often fails because of path issues:

      img = cv.imread(cv.samples.findFile(img_fn))

You will have to replace this line with:

      img = cv.imread(img_fn)

For example, for `dft.py`, I had to copy the 'baboon.jpg' from
`/path-to-opencv/opencv-4.x/samples/data` to the Python directory and
then modify the code to read it locally using:

    def main():
        if len(sys.argv) > 1:
            fname = sys.argv[1]
        else:
            fname = 'baboon.jpg'
            print("usage : python dft.py <image_file>")

        im = cv.imread(fname)

For the following demos, hit `esc` key to escape the demos.\
 \
You can visualize the histogram functions available in OpenCV using:

                   python hist.py

The Discrete Fourier Transform demo can be seen using:

                   python dft.py

You can run a nice deconvolution example using:

                   python deconvolution.py

You can run the following great multithreaded demos:

                   python video_threaded.py  
                   python gabor_threads.py

Use the spacebar to generate different distributions for K-means given
by:

                  python kmeans.py

We can see a demo of edge detection using:

                  python edge.py

The following demos are also working with video motions:

                  python opt_flow.py
                  python dis_opt_flow.py
                  python lk_track.py

# Optional: Digital Image Processing class demos

On a PC, you can download the demos from [UT Live demos
link](https://live.ece.utexas.edu/class/siva/siva_dip/siva_dip.htm).
Unfortunately, they only work on old PCs that run the National
Instrument software. They are excellent!

# Jupyter notebook basics

Saving the notebook does not save the values of Anaconda variables. It
only saves the printed output text. You will need to rerun the code to
reproduce the same environment with your saved values.

If you are interested in using markdown to document your Jupyter
notebooks, you can study the basics at: [Jupyter basics
link](https://daringfireball.net/projects/markdown/basics).

## Start Jupyter notebook

Open up a new Anaconda Prompt and type:

       conda activate pytorch
       jupyter notebook

## Basic operations

-   **Execute a Cell:** Click `Run` or simply hit `Shift-Enter` on the
    Cell.

-   **Run all from scratch:** Click `Cell` and then `Run All`.

-   **Save the current notebook:** Click on the disk icon to save your
    work.

-   **Interrupt long computation:** Click on `Kernel` and then click on
    `Interrupt`. This approach KEEPS ALL VARIABLES. Restart running
    after Kernel interrupt

-   **To run the rest do:** Click on Cell and select `Run All Below`.

## Restart up to a point

       To run up to a point: Click inside the last Cell
       Click on Kernel and Restart to lose all variables.
       Click on Cell and Run All Above.

## Exit after all computations are complete

**This process will loose all of your variables. You can only preserve
the current outputs.**

       Click on the disk icon to save your work.
       Click Kernel then Shutdown.
       Close the browser windows.
       Then close Anaconda Prompt.

## Emergency exit if Interrupt does not work after long wait

**This process will loose all of your variables. You can only preserve
the current outputs:**

       Save the current notebook by clicking on the disk icon.
       Simply type Control-C in the Anaconda Prompt.
       You may have to press Control-C multiple times.
       You can then click and close each tab in the browser.

## Scikit Learn Software Examples

Scikit learn has excellent packages for machine learning that we will be
using. Refer to: [scikit-learn link](https://scikit-learn.org/stable/).

Clustering

:   A very nice example that shows many clustering algorithms can be
    found at [Clustering
    link](https://scikit-learn.org/stable/auto_examples/cluster/plot_cluster_comparison.html).

Classifiers

:   A very nice example that compares several classifiers can be found
    at [classification comparison
    link](https://scikit-learn.org/stable/auto_examples/classification/plot_classifier_comparison.html).

Face classification in the wild example

:   The example uses PCA and SVM to recognize faces as given in [face
    recognition
    link](https://scikit-learn.org/stable/auto_examples/applications/plot_face_recognition.html).

Prediction latency

:   This is important for large datasets. See [prediction latency
    link](https://scikit-learn.org/stable/auto_examples/applications/plot_prediction_latency.html).

## PyTorch Tutorials

Refer to the [PyTorch Tutorials](https://pytorch.org/tutorials) Website
for the latest information.

-   [PyTorch Starting
    Examples](https://pytorch.org/tutorials/beginner/pytorch_with_examples.html)

-   [Pruning the size of a Neural
    Network](https://pytorch.org/tutorials/intermediate/pruning_tutorial.html)

-   [PyTorch
    Cheatsheet](https://pytorch.org/tutorials/beginner/ptcheat.html)

## PyTorch Resources

Please refer to `Safari` under [UNM Library resources for Computer
Science](https://libguides.unm.edu/computer-science).

You can create an account with your UNM ID in [O Reilly
website](https://learning.oreilly.com/home/) to gain full access to
`Programming PyTorch for Deep Learning`.

# Reproducible code: `conda` and `pip`

Anaconda provides virtual environments that cover Python and other
Languages. However, some Python packages may not be available using
`conda`. They may only be available using `pip`. It is thus recommended
to use `pip` under a specific `conda` environment.

## Reproduce an Anaconda Environment without `pip`

Here, the basic idea is to use Anaconda tools to reproduce everything.
The information is available at [conda environments
link](https://conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html).
Here is the process:

1.  Create and save the conda environment.\
    Here, we will follow a process of specifying versions for each
    package. Note that versions are optional. However, once something
    works, we need to save the versions. Here is the modified version
    that creates packages with versions:

            (base) ...>conda create --name MyExampleEnv python=3.10
            (base) ...>conda activate MyExampleEnv
            (MyExampleEnv) ...>conda install scipy=0.17.3
            (MyExampleEnv) ...>conda install other packages ....

2.  Reproduce the conda environment on the same computer\
    The following code creates a clone environment and shows it in the
    list:

           (base) ...>conda create --name myclone --clone MyExampleEnv
           (base) ...>conda info --envs

3.  Reproduce the identical conda environment on the same machine or
    another computer\

             (base) ...>conda activate MyExampleEnv
             (MyExampleEnv) ...>conda list --explicit > spec-file.txt
             ... share spec-file.txt with another machine or the same machine

    Then, you can create a new Environment with the same list using:

             (base) ...>conda create NewEnv --file spec-file.txt

    Alternatively, although it may not work, you can add it to an
    existing environment using:

             (base) ...>conda install --name OldEnvToAdd --file spec-file.txt

## Reproduce Python Environments Using `conda` and `pip`

The following process is far more elaborate. It should be followed if
the use of `conda` environments is not working. In this example, we
reproduce the Python virtual environment using `pip`. However, we still
operate inside an Anaconda environment to maintain some control of the
process.

1.  Hardware and Operating System documentation:\
    Make a note of the OS (e.g., Windows 11, Mac OS 14.4.1), available
    memory, CPU (e.g., Apple M1 Pro chip), and GPU (if using it).

2.  Create a virtual environment using conda.

           (base) ...>conda create --name MyExampleEnv
           (base) ...>conda activate MyExampleEnv

3.  Document the Python version.

           (MyExampleEnv) ...>which python3
           Make a note of your directory to your python executable
           (MyExampleEnv) ...>python3 --version
           Make a note of your Python version (e.g., Python 3.10.0).

4.  Install `pip` using `conda`\
    You will need to use this approach to minimize compatibility issues:

           (MyExampleEnv) ...>conda install pip

5.  Create a virtual environment in a new directory for using `pip`.

           (MyExampleEnv) ...>python3 -m venv MyDirectoryName
           (MyExampleEnv) ...>cd MyDirectoryName
           (MyExampleEnv) ...>ls
            ... displays the files created in your virtual environment

6.  Activate the virtual environment\
    If using Windows, run:

           Microsoft Windows example
           (MyExampleEnv) ...>MyDirectoryName\Scripts\activate.bat

    If using Linux or MacOS, run:

           Linux or MacOS example
           (MyExampleEnv) ...>source bin/activate
           (MyDirectoryName) ..>

7.  Install packages using `pip` from `conda`:\
    The following code gives fine control of the installations with
    version numbers:

           (MyDirectoryName) ..>pip install packageName==1.0.0
           (MyDirectoryName) ..>pip install packageName==version for all other packages ...

8.  Save the installations:\

           (MyDirectoryName) ..>python3 -m pip freeze > requirements.txt
           ... share requirements.txt

9.  Reproduce the installation:\
    Follow the same process as before:

           (base) ...>conda create --name MyExampleEnv
           (base) ...>conda activate MyExampleEnv
           (MyExampleEnv) ...>conda install pip
           (MyExampleEnv) ...>python3 -m venv NewDirectory
           (MyExampleEnv) ...>cd NewDirectory
           (MyExampleEnv) ...>source bin/activate
           (MyDirectoryName) ..>

    You may now reproduce everything using:

           (MyDirectoryName) ..>python3 -m pip install -r requirements.txt

    You can then verify that it all worked using:

           (MyDirectoryName) ..>python3 -m pip list

# Optional Material

## GitHub

You can access GitHub directly by creating an account and logging in
online. You can also edit Google Colab notebooks and upload them
directly into github without any help.

If you want to work at the terminal level, then you can find an
excellent video tutorial by Kevin Stratvert [ Kevin
Tutorial](https://www.youtube.com/watch?v=tRZGeaHPoaw). You can also
work through a Git tutorial at: [ www
tutorial](https://www.w3schools.com/git/default.asp?remote=github).

Visual Studio Code also support GitHub.

## Optional: Running the Natural Language Processing text examples

If you want to add the modules for Natural Language Processing support,
then run `Anaconda Prompt (Anaconda 3)` as Administrator, and follow the
steps to download the English Natural Language models:

        (base) ...>conda activate pytorch
        (pytorch) ...>conda install -c pytorch torchtext 
        (pytorch) ...>conda install -c conda-forge spacy
        (pytorch) ...>python -m spacy download en_core_web_sm
        (pytorch) ...>conda install -c conda-forge googletrans

Note: To add Spanish, you will need to modify the first function call.
After you complete these steps, you should be able to run the examples
of Chapter 5 of the book.\

## Optional: Running the audio processing examples

Similarly, if you want to install support for processing sound examples,
then download the `ESC-50` dataset from [ESC-50 download
link](https://github.com/karolpiczak/ESC-50#download). You can then
install

        (pytorch) ...>conda install -c conda-forge librosa 
        (pytorch) ...>conda install -c pytorch torchaudio
        (pytorch) ...>pip install PySoundFile

After you complete these steps, you should be able to run the examples
of Chapter 6 of the book. **Please note that the spectrogram examples
require a lot of time to be pre-computed.**\

## Optional: Running PyTorch Book Examples

To run the book examples, you will need to first download the Jupyter
notebooks from [ github for Programming PyTorch for Deep
Learning](https://github.com/falloutdurham/beginners-pytorch-deep-learning).
Then, after downloading the examples, you will need to navigate to the
book examples directory and run the following:

        (base) ...>conda activate pytorch
        (pytorch) ...>python download.py
        (pytorch) ...>mkdir tmp
        (pytorch) ...>jupyter notebook

Ignore any errors associated with not being able to find certain files.
The system will work with the images that it does find.

Then open up `Chapter 2.ipynb` and look for the `tmp` directory and
remove the leading \\. For example, modify the directory \\tmp
\\simplenet to tmp \\simplenet.

## Optional: Loading Model Languages in Spacy

Refer to [Spacy Language Models](https://spacy.io/usage/models) to load
different models.
