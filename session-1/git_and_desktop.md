# Code the Future </>

## Session 1: Using Git via GitHub Desktop

### Content covered in this session

- GitHub Desktop

### Session goals

- Pull and push code usin GitHub Desktop

### Installing GitHub Desktop?

#### Windows

Open a browser:

1. Visit "desktop.github.com",
2. Click "Download for WIndows (64bit)",
3. When prompted, click "Run",
4. Allow the installation to download and install,
5. Once the installation completes, GitHub Desktop will launch.

#### Mac

Open a browser:

1. Visit "desktop.github.com",
2. Click "Download for macOS",
3. In your computer's Downloads folder, double-click the GitHub Desktop zip file,
4. After the file has been unzipped, double-click GitHub Desktop,
5. Once the installation completes, GitHub Desktop will launch.

#### GNU/Linux

Currently, GitHub Desktop doesn't support any GNU/Linux distribution, so you'll be required to use the Git CLI (Command Line Interface).

#### Creating your repo from the desktop app

1. Once you're on the start screen, click "Create a New Repository on your hard drive...".
2. Fill in the fields with the information about your new repository. (I'd suggest checking the "Initialize this repository with a README" box).
3. Click "Create Repository".
4. If it's all working correctly, you'll have a button within the program to "publish repository". Click this, and it'll make sure your repository is registered with GitHub.
5. Open up VSCode (or your IDE of choice) and open the folder for your new repository.
6. Open the only file in the folder, called README.md. This file is typically used to describe the project, any instructions to make it run, etc. In this tutorial we're just going to change it a little.
7. In README.md, delete everything (should only be one line), and write your name inside. Then make sure to save it.
8. Once the README.md file has been saved, once again go back to GitHub Desktop and you'll be shown what's been removed and added to the file. Make sure you're happy, because nothing has been saved on GitHub yet.
9. When you're happy, click on the text bar that says "Update README.md". Type in "Wrote my name".  
   This line is a quick description of the commit, or a summary of what's been changed.
10. Click the "Commit to Main" button, then the "Push Origin" button within the program.
11. Head back to the GitHub website and take a look at your new repository, from here you should be able to see your name.

#### Creating the repo in Github and linking to it through the desktop

#### From the website

1. Once logged in, click the "New" button on the left side of the screen.
2. Give a name to this repository and be sure to check the box titled "Add a README file".
   This will ensure that you can easily clone down the repository.
3. Click "Create Repository".  
   Your repository is now created, and can be changed however you want.
   Everything saved here is backed up on GitHub, safe if you accidentally delete it on your personal computer.  
   Scroll down the page and you should see the title of your repository, our goal is to change this.
4. Click the "Code" button and take a look at the dropdown. Copy the link that is shown and head back to GitHub Desktop.
5. Under file, choose "Clone Repository" and go to the URL tab. Paste in the link you copied, choose where you want to save your repository, and finally click clone.
6. Open VSCode (or your IDE of choice) and open the file that you just cloned down.  
   Everything you change here will only be changed on your local copy, until you push it back up.
7. Open the only file in the folder, called README.md. This file is typically used to describe the project, any instructions to make it run, etc. In this tutorial we're just going to change it a little.
8. In README.md, delete everything (should only be one line), and write your name inside. Then make sure to save it.
9. Once the README.md file has been saved, once again go back to GitHub Desktop and you'll be shown what's been removed and added to the file. Make sure you're happy, because nothing has been saved on GitHub yet.
10. When you're happy, click on the text bar that says "Update README.md". Type in "Wrote my name".  
    This line is a quick description of the commit, or a summary of what's been changed.  
    Click the "Commit to Main" button, then the "Push Origin" button within the program.
11. Enter your Username and Password to sign in, then submit them. Your changes have now been pushed to GitHub. Go to GitHub in your browser and refresh the page. The title of your page should have now changed to your name.



<div style="width: 100%">
<a href='intro_to_github.md'><-- Previous section: Git & GitHub Install & Tutorial</a>
<div align="right"><a  href='git_branches_and _conflicts.md'>Next section: Git branches & conflicts --></a></div>
</div>
</div>
