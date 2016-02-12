# Learn To Code: GitHub and Git
Learn the fundamentals of Github, Git, and command-line coding

## Introductions
Hello, and welcome to Learn to Code! This lesson is designed to teach you how to work in Git and GitHub. 

##### What You'll Learn:
In this Learn to Code workshop, you'll learn the essentials of Git, the most common version control tool that millions of coders use while developing for the web. We will also learn how to use Github, a popular Git-based repository to host your projects online. 
- How to create and work in a local repository
- How to work remotely using GitHub (push and pull)
- How to fork, clone, merge, and delete and branch repositories

##### How to Prepare:  
- Bring your laptop, fully charged (bring your charger just in case)
- Install Git: http://git-scm.com/downloads
- Install the Atom text editor if you don't have a text editor. Go here: https://atom.io/

##### Prerequisites:
None, but it would be helpful to have previously completed our HTML and CSS workshops to see how everything fits together.

## Setting Up Your Computer
Before we begin, you need to make sure that the following is set up on your computer:
- Git Bash - To serve as our command prompt and terminal
- A GitHub account - To sync your work locally with an online repo
- Atom text editor - our text editor of choice for Learn to Code
Use the links under "How to Prepare:" to set these apps up. This may take some time...
Don't be afraid to ask for help. we'll get through it!

## Navigating Git

Git Bash is a Unix-based terminal - a text-based way to type commands into your computer. 
Below are some common commands in Git (functions are listed after the "//":
```
$ cd <FOLDER> // "change directory" to the listed folder. "cd" is used a lot to navigate in an out of folders.
```
```
$ mkdir <FOLDER> // This creates a new folder in your existing directory.
```
```
$ ls // This command lists files in your folder.
```
```
$ git init // This will turn Git "on" in this folder
``` 
```
$ git help // For more commands in Git, use "git help".
```
#### Exercise: let's "Git" Going!
Try to do the following:

1. Navigate to the place you want to create your folder with Git
2. See what’s in that folder
3. Create a new directory called “hello-world”
4. Navigate to that new folder
5. Initialize that folder for Git

#### Configure Your Git
First step we need to do is configure your computer so that Git know who is making changes.
Open up your Git Bash and enter in the following commands:
```
$ git config --global user.name "<Your Name>"
```
Now set your email:
```
$ git config --global user.email "<youremail@example.com>"
```
Your computer is now configured to you and your email address.

## Local Version Control
Code is easy to screw up in teams. Fortunately, Git has a LOT of processes to protect you from making mistakes.

#### Exercise: Create a basic text file

1. Open up your text editor (download one from http://atom.io).
2. Write a few lines of text
3. Save the file as “readme.txt” to your folder, “hello-world”

#### Status, Add, Commit - saving changes in Git

Any time you want to save changes in Git, you must follow this 3-step command process.

Step 1: Check the status 
```
$ git status // checks the changes you’ve made to this folder 
```
Step 2: Add the changes for commitment
```
$ git add <FILENAME> // add the files you’d like to commit (save) to change
```
Step 3: Commit the changes with a message
```
$ git commit -m “<your commit message>” // save your changes with a MANDATORY note
```



- Install GitHub Desktop: https://desktop.github.com/
