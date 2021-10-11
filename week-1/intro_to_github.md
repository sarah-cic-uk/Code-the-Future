# Code the Future </>

## Week 1: Git & GitHub Install & Tutorial

### Content covered in this session

- What is Git and GitHub?
- How to install Git
- Making your first repository

### Session goals

- Learn what Git/GitHub are, and how they're used
- Have Git installed on your local system
- Make your first GitHub repository

### What is Git and GitHub?

#### Git

Git is an open-source version control system. Basically a way of easily saving progress on a project and tracking what's been done.
Git is a command-line tool, favoured by the majority of developers to keep track of their projects due to its many advantages.  
Git is currently used by many companies, including:

- Netflix
- Facebook
- Google
- Twitter
- GNU/Linux

#### GitHub

Now that you've learnt what git is, time to learn what it all revolves around, GitHub.
GitHub is a central repository to store your projects and have several other developers collaborate on it together. Simply, GitHub will look after our code, then let other people copy it down without changing the code we've saved ourselves (unless you want to).  
In this course we're going to be using a tool called "GitHub Desktop", a user friendly program that will let you use git and GitHub without needing to touch the command line.

---

### Install Tutorial

#### Sign up to GitHub

Open a browser:

1. Navigate to https://github.com
2. Enter a unique username, your email address and a memorable password. (You'll need these to sign in with GitHub Desktop)
3. Verify that you're not a robot
4. Click "Create Account"
5. Your GitHub account setup is now complete.

#### Windows

Open a browser:

1. Visit desktop.github.com.
2. Click Download for WIndows (64bit).
3. When prompted, click Run.
4. Allow the installation to download and install.
5. Once the installation completes, GitHub Desktop will launch.

#### Mac

Open a browser:

1. Visit desktop.github.com.
2. Click Download for macOS.
3. In your computer's Downloads folder, double-click the GitHub Desktop zip file.
4. After the file has been unzipped, double-click GitHub Desktop
5. Once the installation completes, GitHub Desktop will launch.

#### GNU/Linux

Currently, GitHub Desktop doesn't support any GNU/Linux distribution, so you'll be required to use the Git CLI (Command Line Interface).

---

### First Repository

The goal of this tutorial is to teach you:

- How to make your first repository (sometimes refered to as a repo)
- Clone it to your local computer
- Make a change,
- Push it back up to GitHub.

Now that you have GitHub Desktop installed, know what Git and GitHub are, and what we're going to do, let's get started:

1. Once logged in, click the green "New" button on the left side of the screen.
2. Give a name to this repository and be sure to check the box titled "Add a README file".
   This will ensure that you can easily clone down the repository.
3. Click "Create Repository".  
   Your repository is now created, and can be changed however you want.
   Everything saved here is backed up on GitHub, safe if you accidentally delete it on your personal computer.  
   Scroll down the page and you should see the title of your repository, our goal is to change this.
4. Click the green "Code" button and take a look at the dropdown. Copy the link that is shown and head back to GitHub Desktop.
5. Under file, choose "Clone Repository" and go to the URL tab. Paste in the link you copied, choose where you want to save your repository, and finally click clone.
6. Open VSCode and open the file that you just cloned down.  
   Everything you change here will only be changed on your local copy, until you push it back up.
7. Open the only file in the folder, called README.md. This file is typically used to describe the project, any instructions to make it run, etc. In this tutorial we're just going to change it a little.
8. In README.md, delete everything (should only be one line), and write your name inside. Then make sure to save it.
9. Once the README.md file has been saved, once again go back to GitHub Desktop and you'll be shown what's been removed and added to the file. Make sure you're happy, because nothing has been saved on GitHub yet.
10. When you're happy, go to the bottom left of GitHub Desktop and click on the text bar that says "Update README.md". Type in "Wrote my name".  
    This line is a quick description of the commit, or a summary of what's been changed.  
    Click the blue "Commit to Main" button, then the "Push Origin" button on the top of the program.
11. Enter your Username and Password to sign in, then submit them. Your changes have now been pushed to GitHub. Go to GitHub in your browser and refresh the page. The title on the bottom of your page should have now changed to your name.

You've now created a repository, cloned it down, made a change, committed that change and pushed it back up to GitHub.

---

### Git Terms

<dl>
  <dt> Repository</dt>
  <dd>A file holding all of your code. Everyone can have a local copy on their own systems, with one stored safely on GitHub, that only you and anyone you choose can change.</dd>

  <dt>Clone</dt>
  <dd>Means copying a repository to your local system to let you change without making changes to the safe repository on GitHub.</dd>

  <dt>Commit</dt>
  <dd>Saving the changes that have been made, think of it as a stage of changes. It will look for anything that has been changed in the repository, package it up for you, ready to be pushed up to GitHub.</dd>

  <dt>Push</dt>
  <dd>The process of adding your commits to GitHub. Git will look for any commits that haven't already been pushed, then push up what remains.</dd>

  <dt>Pull</dt>
  <dd>Useful when working with others on the same repository. The pull function lets you update your local copy of the repository, if there are any changes to the copy on GitHub.</dd>

  <dt>Branch</dt>
  <dd>Beyond the scope of this tutorial, branches allow for you to work on your code and push it to GitHub, without making changes to any code that you know is working. 
  When you made your repository, you might've seen GitHub mention something called "Main Branch". This name was changed recently, so if you see references to "Master Branch", know that it means the "Main Branch".  
 You can make as many branches as you want, make sure the code works, then merge it into the Main Branch.</dd>

  <dt>Pull Request</dt>
  <dd>A pull request is when we want to pull the code of one branch into another.</dd>

![Git Branches](git-branches.png)

  <dt>RollBack</dt>
  <dd>Made a mistake and accidentally pushed it to GitHub? No problem, you can simply rollback your code to a state where</dd>
</dl>

---

[Click Here for a Git cheatsheet](https://education.github.com/git-cheat-sheet-education.pdf)




<div style="width: 100%">
<a href='intro_to_ide.md'><-- Previous Section: The Developer Environment</a>
<div align="right"><a  href='../week-2/README.md'>Next Section: Week 2 Introduction --></a></div>
</div>
