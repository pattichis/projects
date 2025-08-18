# Create a GitHub Account

Go to <https://github.com/> and create a user account.

# Create a GitHub Repo

    1. Login into your GitHub.
    2. Click on Repositories.
    3. Click on New.

    4. Type in the name for your Repository. 
    Choose a cool name but you may want to do a global search 
    under github.com to make sure nobody else is using this name.

    5. Type a short description.

    6. Click on Public for everyone to see. 
    Else choose Private to control who can see. 
    We still control who can commit changes.

    7. Add a README file. We can edit it later.

# Working with Google Colab notebooks

    1. Login into your Gmail account.

    2. Create a “New Folder” under “Colab Notebooks” with the same name as your Repo.

    3. Under the Repo directory, create a “New Google Colaboratory”. 
    If this option is not available, consult a setup tutorial on how to set one up.

    4. Under “File” In “Google Colab” click “Copy to GitHub”.

    5. Select your Repository name, “Brach: main”, preserve the same name, 
    enter a message that reflects the changes, and click to “Include a link to Colab”.

After this, you will be able to open files in your GitHub account in
your Gmail account. Make sure to save them into your local directory.

General Reference: <https://colab.research.google.com/>.\
Markdown reference:
<https://colab.research.google.com/notebooks/markdown_guide.ipynb>.

# Manipulating Files inside GitHub

It is very convenient to:

    1. You can delete files inside your GitHub account.
    2. You can also edit files inside your GitHub account. 
    This is extremely useful for editing library files for Python.

# Create Local Repo

## Create a personal access token for your local Repo:

    1. Click on your picture (top right).
    2. Click on Settings.
    3. Go to the bottom of the left-hand side to find “Developer Settings”.
    4. Click on “Personal Access Tokens”.
    5. Click on “Tokens (classic)”.
    6. Click on “Generate New Token” for “General Use”.
    7. Save token. You will need for your password.

## Create the local Repo files and upload

    1. Create a new directory to store everything.
    2. If your attempts failed, use “rm -f -r .git” to clean up. Use “ls -al” to see 
         what is happening.
    3. The following commands are from GitHub:
            git init
            git add .  
            git commit -m "test"
            git branch -M main
    The rest depend on your Repo, use “origin” to allow you to push and pull locally.
             git remote add origin https://github.com/pattichis/FASTrain.git
             git push -u origin main

# Updating to the default branch

To update, use:

             git add .      
             git commit -m "Updating Readme"
             git push

which: 1. Adds files, 2. Updates commit statement, 3. Pushes the file.\
You should now be able to see the repo if it is public. If not, login
and you will have access to the private repos.

# Make it private:

    1. Click on the Repo name.
    2. Click on Settings.
    3. Click on “General”
    4. Click on “Danger Zone” (at the bottom).
    5. Click on “Change Visibility” to make it private.

# Add Collaborators:

    1. Click on the Repo name.
    2. Click on “Collaborators”.
    3. Click on “Manage access”.
    4. Click on “Add people”.

The collaborator needs to accept the invite by going to
`github.com/origin-repo-user-name/repo-name/invitations` where
`origin-repo-user-name` refers to the repo of the origin user to accept
the invitation.

# Working with local folder

Move your files to the local folder.

# Cloning to a local directory

Clone locally using:

    1. Go to a clean directory.
    2. Use:
           git clone git@github.com:origin-user-name/Repo-name.git

# Tutorial material that was not covered

-   Create a different branch.

-   Merging branches.

# Tutorial link to learn more about Git and GitHub

You can follow a step-by-step YouTube tutorial at
<https://www.youtube.com/watch?v=tRZGeaHPoaw>.\
You can also learn interactively by following simple tutorials at:
<https://www.w3schools.com/git/default.asp?remote=github>.
