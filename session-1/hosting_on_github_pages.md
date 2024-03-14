# Code the Future </>

## Session 1: Hosting on GitHub Pages

### Content covered in this session

- What is GitHub Pages
- Setting up your repository
- Hosting repository

### Session Goals

- Learn about GitHub Pages
- Configure your Repository to work with Pages
- See your repository being hosted

### What is GitHub Pages

GitHub Pages is a static site hosting service that takes HTML, CSS, and JavaScript files straight from a repository on GitHub, optionally runs the files through a build process, and publishes a website. This gives us a way to be able to host websites for free within our accounts for a single site.

**What is the difference between GitHub and GitHub Pages?**

The purpose of GitHub Pages is to provide the GitHub user a way to create personal websites for themselves and websites for their projects / repositories. For each registered GitHub account (representing a user or an organization) you can register one User Page, but an unlimited Project pages.

GitHub pages can be used to host more complex projects that might use a framework such as React, VueJS or Angular, but would require a bit more setup for us to achieve, but would be great to research in your own time if you are interested.

### Setting up your repository

To set up our repository there are a couple things to look out for:

- The name of the Repository
- The structure of content in the repository

First off with the repository that name, there is a certain convention you must use so that GitHub pages can properly be hosted. This convention is `{_your GitHub username_}.GitHub.io` e.g., `joe.blogs.github.io` or `persion142.github.io`. The username section must be spelled exactly how your username is so that it can link you user with the repository and host the page correctly. If the repository you have made doesn't follow this you can change the name of an existing repository to match this is you wanted.

First go to the Settings section of your repository.

<img src="https://raw.githubusercontent.com/sarah-cic-uk/Code-the-Future/main/images/session1/settings.png" alt="repository" width="80%">

Second edit the Repository name under the general settings tab to match the naming convention needed.

<img src="https://raw.githubusercontent.com/sarah-cic-uk/Code-the-Future/main/images/session1/Repo-name.png" alt="repository" width="80%">

Second is the structure of the page. below is an example of the structure.

<img src="https://raw.githubusercontent.com/sarah-cic-uk/Code-the-Future/main/images/session1/folder-structure.png" alt="repository" width="80%">

Here we can see what is needed at what is called the top we want our index.html and README.md file, below this we would want to create folders for the other pages, the style, and images we would use within out webpage.

**_THE BASE FILE NEEDS TO BE NAMED/KEPT AS `index.html`_**

The reason that this file needs to stay named the way it is, is because GitHub Pages will try and look for this this file first to host it. If it can't find an index.html file it will look for a README.md file to host, if neither file is found it will not be hosted correctly.

### Hosting your Repository

Once all your files are correctly setup and are named correctly, we can start hosting our website.

Firstly, go to your repository on GitHub.com and click on the settings section at the top.

<img src="https://raw.githubusercontent.com/sarah-cic-uk/Code-the-Future/main/images/session1/settings.png" alt="repository" width="80%">

Next on the left hand side you want to click on Pages under the Code and automation tab.

<img src="https://raw.githubusercontent.com/sarah-cic-uk/Code-the-Future/main/images/session1/setting-sections.png" alt="repository" width="50%">

Then once located on that page you want to keep the source as `Deploy from a branch`, under that we set the branch settings. Set the left box (The branch box) `as main` and set the next box along to `/(root)`, and click on `Save`.

Below is an image of the settings you should have in the pages section. [If you have a custom domain sorted already you can use this custom domain name.](#using-a-custom-domain-name)

<img src="https://raw.githubusercontent.com/sarah-cic-uk/Code-the-Future/main/images/session1/pages-settings.png" alt="repository" width="80%">

After a few minutes your page should now be hosted on GitHub pages ready for you to share. Once the page is done you will have section at the top that will appear showing you the name of the page and if you want to stop hosting it.

<img src="https://raw.githubusercontent.com/sarah-cic-uk/Code-the-Future/main/images/session1/site-url.png" alt="repository" width="80%">

When progressing through the course any changes you push to your repository will trigger a build to run in the backgroun and deploy your site with the updated code.

## Using a custom domain name

You can just leave your website at that address (it'll give you some serious street cred in the developer world), but if you have a custom domain you would like to use, it is very simple to make GitHub redirect your page.

1. Log in to your domain registrar and find where to change your host records. If you don't know, you can usually Google "(domain registrar) change host records", and your registrar will have an explainer telling you how to do it.
2. Change your domain's A Record to 204.232.175.78. This is GitHub's IP address, which allows GitHub to resolve your URL and serve the correct files.
3. In your website's directory folder on your computer, create a file called "CNAME". On the first line, type your domain name. Save the file.
4. In your GitHub application, you should see the file in the left column. Make sure it is checked and enter your commit message. Have it say something like "Adding CNAME file."
5. Click "Sync branches."

It can take as long as 48 hours for your domain to resolve to your GitHub page. However, it is usually pretty quick, so check back in an hour or so.

## References

- [Basic Tutorial](https://pages.GitHub.com/)
- [VueJS Framework Tutorial](https://learnvue.co/articles/deploy-vue-to-GitHub-pages)

<div style="width: 100%">
<a href='intro_to_github.md'><-- Previous section: Introduction to Git & GitHub</a>
<div align="right"><a  href='../session-2/README.md'>Next section: Session 2 Introduction --></a></div>
</div>
