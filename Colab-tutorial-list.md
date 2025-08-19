# Required elements of each Tutorial

You are required to use Google Colab to develop the tutorials. Google
Colab will allow to run the code without complex installations. You can
add videos to explain the tutorial.

The following is a list of requirements to make your tutorials useful:

Text cells for documentation:
    
    Document the main part of the tutorial using text cells, not code cells.

Sections:

   Create sections using:
   
          # Section title in a single text cell.

Subsections:

     Create subsections using:

          ## Subsection title of a section in a single text cell.

Top level description:

    Describe the scope of the tutorial at the top of the document.

References at the top:

    Provide a list of references. This can include references to arxiv
    papers, GitHub Repos, datasets, etc.

Top level library requirements:

    Provide a list of required libraries and how to install them. Make
    sure to include appropriate versions of each library. Use `assert`
    commands to ensure that the libraries versions are available.

    Provide the installation code near the top of each tutorial, below
    the scope. Give users the option to skip installations if running
    the code for a second time. You can do this with a simple `if`
    statement. You also may want to add `pip` commands for installing
    different libraries.

Mount Google Drive:

    This step includes information on how to mount Google Drive
    directories in Google Colab.

Dataset requirements:

    Use `training`, `validation`, and `testing` directories. Provide
    Google Drive directories and approximate storage requirements. This
    is especially important if you require large datasets. You may want
    to use a zip file to allow for the entire dataset. You must let
    users know how the files are stored in different directories.

Hardware used for running:

    Provide a description of where the tutorial will run (e.g., CPU,
    GPU, TPU). You may want to provide the GPU type.

Approximate execution times:

    You need to provide an approximate execution time for running the
    entire tutorial. It may also be appropriate to provide approximate
    execution times for downloading the dataset, training, and testing.

Expected results in terms of metrics:

    Provide brief descriptions of expected results (e.g., 75% accuracy,
    an AUC of 0.71, etc).

# List of Required Google Colab Tutorials

#1. Dataset Tutorial:   

    Provide sufficient information to define all elements of a dataset:

    -   Explain how to setup a dataset using Google Drive. Explain the
        directory structure and provide any zip, unzip commands.
    -   Provide code to play audio, display image, or play video based
        on what you are doing.
    -   Describe what the inputs are. Is it 1D/2D/3D NumPy array?
    -   Describe what the output labels are: What are the categories?
    -   Describe how to extend the dataset. Show how to download and add
        an audio, image, or a plain video to the dataset.
    -   Explain how to setup the training, validation, and testing
        datasets.

#2. Model Description Tutorial:   

    Provide sufficient information to access all elements of the model:

    Load a model:   
    Give Python code of how to load a pretrained model. 
    You may want to use `wget` from a GitHub account.

    Save a model:   
    Give Python code of how to save your model.

    Number of parameters:   
    You can give a command that prints how many.

    Input layer:   
    Demonstrate compatibility with the dataset tutorial.

    Output layer:   
    How many outputs? What are the activation functions? How do we
        train the model? What is the loss function? Do you use
        cross-entropy, mean squared error? What is it?

    Intermediate layers:   
    Is the model using CNNs? Is it LSTM? Is it ResNet? Give a brief
        description of intermediate layers. You can reuse images from
        the reference papers. If small, print the entire model. Else,
        describe major parts of the model.

#3. Model Optimization Tutorial:   

    Provide sufficient information to show how to fine-tune a model:

    Loss function: 
    Specify the loss function (as in the model description).

    Optimization algorithm:   
    Give the name. Is it Adams? Which one. 
    Give basic parameters of the optimization algorithm.

    Learning rate:   
    Give initial learning rate. 
    If you adjust it, explain how.

    Batch size:   
    Give the number of audio, images, or videos that are used in
        each batch.

    Number of epochs:   
    Provide the maximum number of epochs. Are you using early
        stopping?

    Train versus validation loss graphs:   
    Explain any gaps between the training and validation graphs. Did
        you use early stopping? How did you avoid overfitting?

#4. Basic Testing Tutorial:   
    
    Load the pre-trained model using wget to download it and run it on
    one test example.

#5. Basic fine-tuning Tutorial:   
    
    Download a pre-trained model, setup the optimization loop, and show
    that the loss function is getting reduced. Retrain the pre-trained
    model for a few iterations to demonstrate the optimization process.

#6. Full training Tutorial:   
    
    Run the loop multiple times and show that the validation and testing
    losses converge to a good number. If the losses do not converge, you
    will need to add data augmentation.

# Basic References
The document covers the minimum requirements for developing Machine
Learning tutorials code. While the information here is about tutorials,
it provides a list of basic questions that everyone working with machine
learning code should be able to answer.

Refer to the `How to ...` tutorials for technical information on how
to setup the tutorials.

# Grading information

The provided tutorials are considered minimal and essential. Unless
otherwise stated, they carry equal weight. For more mature datasets, the
`Full training tutorial` will carry twice or more credit. This will be
made clear during the one-to-one meetings. The Google Colab tutorials
are expected to run. You will receive little to no credit if a tutorial
does not run.
