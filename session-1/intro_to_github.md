# Code the Future </>

## Session 1: Git & GitHub Install & Tutorial

### Content covered in this session

- What is Git and GitHub?
- How to install Git

### Session goals

- Learn what Git/GitHub are, and how they're used
- Have Git installed on your local system

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
In this course we're going to be using VScode to interact with GitHub but there are alternatives which some developers prefer such as using Terminal or GitHub Desktop (a user friendly program that will let you use git and GitHub without needing to touch the command line).

---

### Install Tutorial

#### Sign up to GitHub

Open a browser:

1. Navigate to "https://github.com",
2. Enter a unique username, your email address and a memorable password. (You'll need to remember these if you want to sign in with GitHub Desktop in the optional lesson),
3. Verify that you're not a robot,
4. Click "Create Account",
5. Your GitHub account setup is now complete.

---

### Git Terms

<dl>
  <dt><b> Repository </b></dt>
  <dd>A repository contains all of your project's files and each file's revision history. Everyone can have a local copy on their own systems, with one stored safely on GitHub, that only you and anyone you choose can change.</dd>

  <dt><b> Clone </b></dt>
  <dd>Means copying a repository to your local system to let you change without making changes to the safe repository on GitHub.</dd>

  <dt><b> Commit </b></dt>
  <dd>Saving the changes that have been made, think of it as a stage of changes. It will look for anything that has been changed in the repository, package it up for you, ready to be pushed up to GitHub.</dd>

  <dt><b> Push </b></dt>
  <dd>The process of adding your commits to GitHub. Git will look for any commits that haven't already been pushed, then push up what remains.</dd>

  <dt><b> Pull </b></dt>
  <dd>Useful when working with others on the same repository. The pull function lets you update your local copy of the repository, if there are any changes to the copy on GitHub.</dd>

  <dt><b> Branch </b></dt>
  <dd>Beyond the scope of this tutorial, branches allow for you to work on your code and push it to GitHub, without making changes to any code that you know is working.
  
  When you made your repository, you might've seen GitHub mention something called "Main Branch". This name was changed recently, so if you see references to "Master Branch", know that it means the "Main Branch".

 You can make as many branches as you want, make sure the code works, then merge it into the Main Branch.</dd>

  <dt><b> Pull Request </b></dt>
  <dd>A pull request is when we want to pull the code of one branch into another.</dd>   
  <br/>

   
<img src="https://raw.githubusercontent.com/sarah-cic-uk/Code-the-Future/main/images/session1/git-branches.png" alt="Git Branches" width="80%">


  <br/>

  <dt><b> Rollback </b></dt>
  <dd>Made a mistake and accidentally pushed it to GitHub? No problem, Git lets you rollback to the previous commit where everything was working properly so that those instances of the code can be deployed for the website and you (or your peers) don't face any problems. And during that time, you can fix the issue, and when it works properly, you can again deploy the new feature.</dd>
</dl>

---

### Resources

<ul>
<li><a href='https://education.github.com/git-cheat-sheet-education.pdf' target='_blank' title="Git cheatsheet">Git cheatsheet</a></li>
</ul>

<div style="width: 100%">
<a href='intro_to_ide.md'><-- Previous section: The Developer Environment</a>
<div align="right"><a  href='first_repo.md'>Next section: Create your first repo--></a></div>
</div>
</div>
