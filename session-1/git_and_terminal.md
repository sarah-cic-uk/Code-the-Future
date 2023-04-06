# Code the Future </>

## Session 1: Git & Terminal

### Content covered in this session

- Using Git in Terminal (Mac) / Cmd Prompt (Windows)

### Session goals

- Learn how to use Terminal
- Push code to a repo on GitHub using the terminal
- Trial Git GUI

## Terminal

### Mac

To open Terminal on Mac you can use the CMD+SPACE shortcut and type terminal in the search box.

Terminals can have different themes, the default being white with black text. Screenshots here are my own custom theme so don't worry if your terminal looks different!

Terminal:

![Terminal](../images/session1/terminal.png)

### Windows

I'd recommend downloading GitBash. This will provide a Mac style terminal for you to use on a windows machine.

Git Bash can be downloaded from https://git-scm.com/. There is a page with more information here: https://git-for-windows.github.io/.

### Some useful commands:

#### Terminal/Git Bash:

**clear** - clears all the text from the screen to start fresh (doesn't undo anything, just bumps it off the screen).
**pwd** - prints the working directory. Helps you navigate and know where you are in the file system!\
**ls** - lists all files in the folder you are sat in\
**mkdir** - creates a new folder. add the name of the new folder afterwards: `mkdir codeTheFuture`\
**cd** - change directory. `cd codeTheFuture` will move you into the folder called codeTheFuture\

#### Git:

**git clone** - this allows you to close a url from GitHub
**git add** - this adds your local files to the git staging area. `git add .` and `git add -A` are two different ways to add all files. `git add filename` will add a specific file (you may sometimes needs the full path e.g. `/codeTheFuture/filename`)\
**git commit -m "message"** - this command commits the changes with a useful message. make the message as useful as you can in case you need to refer back to what was in the commit at a later date!\
**git push** - this will push all the committed changes up to the repo. They will then be available for others to pull down and see.\
**git pull** - pulls down the latest code from the repo.\

---

## Activity

### Use Terminal to create a repo, pull and push up code

1. Open your terminal
1. create a new folder for the course: `mkdir codeTheFuture`
1. change into the new folder: `cd codeTheFuture`
1. Open github and create a new repo:

Navigate to the repositories tab and hit 'New':
![GitHub Dashboard](../images/session1/github_dashboard.png)

Create your repo with a README file:
![Create Repo](../images/session1/create_repo.png)

Now your repo exists, click the 'Code' button and select HTTPS (or SSH if you have set up an ssh key) and copy the url:
![Clone Repo URL](../images/session1/clone_url.png)

Next, return to your terminal and clone the repo using the url you have copied:
![Clone Repo In Terminal](../images/session1/clone.png)

1. move into your newly cloned repo: `cd code-the-future-demo` and list the files using `ls`. You should see your README.md
   ![Navigate into repo folder](../images/session1/open_repo_folder.png)

1. Open your repo folder in VScode and edit the README.md
1. Add your changes to the staging area: `git add .`
1. Commit your changes with a useful message: `get commit -m "updating readme"`
1. push the changes: `git push`
1. Navigate to the GitHub browser and look in your repo. You should see your changes!

---

## Git GUI

Have a play with Git GUI!

1. Make additional change in your VScode README.md
1. In terminal type `git gui`
1. Click the file you want to add on the left hand side - red lines have been removed, and green lines have been added.
1. Add a commit message into the box at the bottom
1. Hit Commit
1. Hit Push
1. Return to the browser and look for your changes

![Git Gui](../images/session1/gitgui.png)

<div style="width: 100%">
<a href='intro_to_github.md'><-- Previous section: Git & GitHub Install & Tutorial</a>
<div align="right"><a  href='../session-2/README.md'>Next section: Session 2 Introduction --></a></div>
</div>
