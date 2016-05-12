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
Below are some common commands in Git (functions are listed after the "//"):
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
#### Exercise: Let's "Git" Going!
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

## Working Remotely
Now that you've got a taste of working locally, let's take it up a notch. First, we need to re-configure your Git to work with your GitHub.

#### Configure Git for GitHub
In Bash, enter in the command to sync your folder with your GitHub account:
```
$ git config --global user.username "USeRnAMe" // this is case-sensitive and does not need "<" or ">"
```
Verify that the configuration was successful here:
```
$ git config -l
```
??
```
$ git config --list
user.name=John Doe
user.email=johndoe@example.com
color.status=auto
color.branch=auto
color.interactive=auto
color.diff=auto
...
```
OR
```
$ git config <key>

$git config user.name
John Doe
```

#### Pushing to GitHub
Pushing is another way to say that we're doing to upload code to GitHub from your local computer. 
- Gut check: what's the difference between PUSHING and COMMITTING?

#### Exercise: Create a Remote Repository in GitHub
1. Go to github.com, log in, and click the '+' in the top right to create a new repository.
2. Give it a name that matches your local repository's name, 'hello-world', and a short description.
3. Make it public.
4. Don't initialize with a README because we already have a file, locally, named 'readme.txt'.
5. Leave .gitignore and license on 'none'.
6. Click create repository!

#### Connect the remote to your GitHub repo
In Bash, in the folder of your choosing:
```
$ git remote add origin <URLfromGitHub>
```
Bonus: you can also change the remote to another URL:
```
$ git remote set-url <RemoteName> <URL>
```
#### Time to push!
Here is the command to push from your original remote copy to the GitHub master:
```
$ git push origin master
```
#### Practice a pull!
If you have access, you can also pull from the master or any repo to your computer:
```
$ git pull origin master
```

## Forking and Cloning
In GitHub you can make two kinds of copies with open-source code:

**Fork** - creating a copy within GitHub from one account to another

or

**Clone** - creating a copy from GitHub to your computer

#### Exercise: Copy our Cookie Recipe

1. Log in to your GitHub account
2. Go to: https://github.com/GalvanizeOpenSource/Chocolate-Chip-Cookies
3. Click the “Fork” Button


#### Exercise: Let's Clone the Recipe
Let’s do it in a different folder first.

Step 1: Navigate out of the "hello-world" folder
```
$ cd .. // to get out of the current folder
```
Step 2: Clone the precise URL
```
$ git clone <GitHubURL> // copies the folder and file to your computer
```
Step 3: Open the file in Atom to check it out!

Optional: You can also connect remotely to get updates faster
```
$ git remote add upstream <GitHubURL>
```

## Branching and Merging
We can’t/shouldn’t all be messing with the original master - even on your local computer.

**Solution:** create a branch to keep your changes until they’re ready to push. This protects the master from unwanted changes and allows for a smoother, safer workflow.

#### Here are some common branch commands in Git:
```
$ git branch // lists all the existing branch
```
```
$ git branch <BranchName> // create a new branch
```
```
$ git status // will tell you which branch you are on
```
```
$ git checkout <BranchName> // let’s you explore that branch (or switch to a different one)
```
```
$ git branch -m <BranchName> // rename a branch you are currently working on (checkout first)
```

#### Exercise: Let's Branch Our Readme!

1. Navigate back to the “hello-world” folder
2. Create a branch called “readme-edits”
3. Add some text to that readme.txt via your text editor
4. Go through the status/add/commit process to check-in your changes

#### Merging: may our forces combine!
Now that we've committed the branch changes, let's commit to the master.

#### Common Merging Commands
```
$ git merge <BranchName> // merges the branch you just worked on into the origin.
```
```
$ git branch -d <BranchName> // deletes the branch - it is no longer needed
```

#### Exercise: Let's merge our readme!
1. Navigate in Git to the origin branch by using “checkout”
2. Merge the branch “readme-edits” 
3. Push the branch to GitHub

Optional: delete the “readme-edits” branch

## YOU DID IT! YOU ARE NOW A SOCIAL CODER!

#### Play around in the sandbox a bit more
- Fork and clone some more open-source Github repos
- Make a pull request (what is this?)
- Push just your branch into GitHub
- Explore other commands “git help”

#### Optional: Install GitHub Desktop
If you prefer to do all of this on a Graphical User Interface (GUI), check out: https://desktop.github.com/

#### Want to code more? Check out Galvanize's Full Stack Immersive Program!

- 24 Week Full-Time Program
- 97% Job Placement Rate within six months
- Average starting salary: $77,000 per annum
- Scholarships available for those who qualify
- Learn more at http://galvanize.com/courses/fullstack/

**About the Author**

Lee Ngo is an evangelist for Galvanize based in Seattle. Previously he worked for UP Global (now Techstars) and founded his own ed-tech company in Pittsburgh, PA. Lee believes in learning by doing, engaging and sharing, and he teaches code through a combination of visual communication, teamwork, and project-oriented learning.

You can email him at lee.ngo@galvanize.com for any further questions.

