# Repositories

A Repository allows you to update a collection of Google Colab notebooks
directly from your browser.

## Create a Repository

    1. Navigate to your main GitHub page.
    2. Click on + and select Repository.
    3. Select Public or Private for your repository.

## How to upload a folder with several files in GitHub

    1. Organize the files into a local folder.
    2. Click on + and drag the entire folder into the GitHub add.

# Create and use a Python library using Google Colab

It is a lot easier to create and debug your libraries as a single cell
at the beginning of your code. After debugging your library as a cell,
you may want to save it as a local Python library file. Once you save
it, updating your library needs to follow the steps described here.

## Mounting Google Colab Directories

The following code will let you mount the Google Colab directory under
[Colab Notebooks/temps](Colab Notebooks/temps){.uri}:

    from google.colab import drive
    drive.mount("/content/drive")

    import os
    os.chdir("/content/drive/MyDrive/Colab Notebooks/temp")

    !ls

## Creating and saving a library file

Inside the Google Colab where you have debugged your function do:

    1. Mount the directory where you want to save your Python library.
    2. Copy all of the functions for your library inside a single cell.
    3. At the top of the cell in your Google Colab, use:

    %%writefile plot_functions_lib.py

    Instead of plot_functions_lib.py, use your library name.

    4. Check that your file was properly saved:

    !ls

## Loading and Importing Libraries Using Google Colab

In order to debug your library locally use:

    1. Mount the directory where your library is located.
    2. Use an import command to import what you need from the library.

    The process to debug is:
    1. Open Runtime in your Google Colab notebook.
    2. Click  Disconnect and delete runtime to eliminate the previous library instance.
    3. Click  Run all to run a new library instance.

## Downloading Libraries from GitHub

    1. Upload the library file to your GitHub.
    2. Inside the Google Colab notebook, download the library.

    If you are NOT debugging the library, you can KEEP your local copy using:
    !wget -nc https://raw.githubusercontent.com/pattichis/GraphSpeeds2/main/lineart_v4.py

    Instead of pattichis, use your GitHub name.
    Instead of GraphSpeeds2, use the name of your Repository.
    Instead of lineart_v4.py, use the name of your Python file.

    If you want to OVERWRITE your local copy, remove the -nc option and remove older versions using:

    !rm -f lineart_v4.py*
    !wget https://raw.githubusercontent.com/pattichis/GraphSpeeds2/main/lineart_v4.py


    3. Use a Python import command to import functions from the library:

    from symbolic_graphs2 import graph_funs

    Instead of symbolic_graphs2, use your library name.
    Instead of graph_funs, use a list of your functions, separated by commas.

## Updating Libraries: Use GitHub

Local changes on libraries will be lost unless they are saved on a
different directory or uploaded to GitHub.

    1. Edit your library on your GitHub account.
    2. Make sure to use !wget to download the library in your Google Colab 
        notebook without the -nc option.

## Running Google Colab with an Updated Library

Once your run the setup portion of your code, the library is compiled in
memory. To work with a new library, you must:

    1. Navigate to Runtime and run Disconnect and Delete runtime. 
    2. Verify that you are deleting older versions and downloading the new version.
    As in the example above, use:

    !rm -f lineart_v4.py*
    !wget https://raw.githubusercontent.com/pattichis/GraphSpeeds2/main/lineart_v4.py

    3. Navigate to Runtime and run. 

# Download a GitHub zip file and unzip it to your local directory

For the following example, `RGAFA-2025` is the target directory. Replace
`RGAFA-2025` by your target directory.\
The GitHub account is `https://github.com/pattichis/GraphSpeeds2`.
Replace this with your own GitHub account.\
After executing the following script, everything will be saved in
`RGAFA-2025/GraphSpeeds2-main`.\
Note that if the `chdir` is successful, the new directory will be
`RGAFA-2025`.

    import os

    # Mount the drive:
    from google.colab import drive
    drive.mount('/content/drive')

    try:
      os.chdir("/content/drive/MyDrive/RGAFA-2025")
      print("Directory changed successfully.")
    except FileNotFoundError:
      print("Error: RGAFA-2025 directory not found.")

      # Create a local directory
      !mkdir /content/drive/MyDrive/RGAFA-2025

      # Get the repo as a zip file and save it locally:
      !wget https://github.com/pattichis/GraphSpeeds2/archive/refs/heads/main.zip -O repo.zip
      !unzip repo.zip -d /content/drive/MyDrive/RGAFA-2025/
      !rm -f repo.zip

# How to create a branch on GitHub

Note that you cannot clone branches. You will have to clone everything
and then get into a branch. Instead of a branch, consider using a
Release of your code. A branch allows you to make a copy of the current
library to continue development. Here are the steps.

    1. Select the Repository that you want to work on.
    1. Click on the upper left icon that shows branching.
    2. Enter the name of the branch. 
