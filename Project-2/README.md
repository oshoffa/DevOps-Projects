# GIT PROJECT

## Initializing a Repository and Making Commits

### Initializing a Repository

After opening the git bash terminal on the computer, you create a new directory with `mkdir <name>` command, you enter into the newly created directory with `cd <name>`. Then you run `git init` command to initialize the new repository. 

![Alt text](<Images/Screenshot (241).png>) 

### Making a first Commit 

Create a file using the `touch <name>` command, type anything you want in the created file and save it. Add the changes to the staging area with `git add .` command. Run `git commit -m "<commit message>"` command to commit the changes. 

![Alt text](<Images/Screenshot (249).png>)

## Working with Branches 

### Make a first git branch 
Use `git checkout -b <new branch name>` command to create the new branch and move into it. 

### Listing all the branches 
Use `git branch` command to list the branches.

### Change into an old branch 
use `git checkout <branch nanme>` to navigate into branches. 

### Merging a branch into another branch 
First we move into the branch we want to merge into, the main branch. Next, we run the command `git merge <other branch name>`. 

### Deleting a git branch 
Use `git branch -d <branch name>` to delete an obsolete branch. 

![Alt text](<Images/Screenshot (250).png>) 

## Colaboration and Remote Repositories 

### Creating a github account and creating a repository
It was created at the start of my programme at darey.io and used for my first project. 

![Alt text](<Images/Screenshot (245).png>) 

### Pushing local repository to remote github repository
First we add the remote repository to the local repository with the command `git remote add origin <link to the remote repo>`. 

Next, we will clone the remote repository to our local computer using `git clone <link to remote repo>`. 

We will now push our work to the remote repository in the cloud with `git push origin <branch name>`. 

![Alt text](<Images/Screenshot (251).png>) 

Thank you and God bless you. Cheers.