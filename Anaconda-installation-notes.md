# Install Anaconda with OpenCV 

Consult the official PyTorch installation instructions from
`GET STARTED`. This is currently given at [PyTorch Get Started
Locally](https://pytorch.org/get-started/locally/). It is recommended
for you to download the latest version identified as: [Anaconda
individual licence](https://www.anaconda.com/products/individual).
Scroll down to the end of the page and select the latest Python and a
`64-Bit Graphical Installer`. I did not find any issues with the 
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
I installed the 2024 version of Anaconda manually using:

    curl -O https://repo.anaconda.com/archive/Anaconda3-2024.10-1-MacOSX-arm64.sh
    cd /opt
    bash Anaconda3-2024.10-1-MacOSX-arm64.sh

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

# Working with different environments

    >conda activate
    (base) ...>conda info --envs
    ... environment names
    (base) ...>conda activate <environment-name>

# Uninstalling Anaconda
If you update your Operating System, Anaconda may fail to load. In this
case, follow the information given in [uninstall
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

For the following demos, hit `esc` key to escape the demos.

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
