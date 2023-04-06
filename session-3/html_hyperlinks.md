# Code the Future </>

## Session 3: HTML Hyperlinks

<h2 id=html-links> HTML Links</h2>
HTML links, or hyperlinks, allow you to navigate to another location by simply clicking on some anchor. These are particularly useful to jump to specific sections on a webpage, email addresses, other web pages, or anything else a URL can address.

To define a hyperlink, we use the `<a>` tag, also known as the anchor element. Content that is wrapped within this tag becomes the anchor and so should indicate the location of that link's destination. An important attribute of the `<a>` tag is `<href>`, which references the URL that the hyperlink points to.

### Examples

In this example you will see a few different ways that you can implement hyperlinks.

- To link to a location on the same page through some text given some set id, eg. <a href=#html-links>HTML Links</a>

```
<a href=#html-links>HTML Links</a>
```

- To link to another webpage though an image, eg.
  <a href="https://www.ibm.com/employment/ciceurope/uk-en"> <img src="../images/ibm-logo.png" alt="IBM logo" height=50> </a>

```
<a href="https://www.ibm.com/employment/ciceurope/uk-en"> <img src="../images/ibm-logo.png" alt="IBM logo" height=50> </a>
```

- To link to an email address and phone number, eg. <a href="mailto:jane@ibm.co.uk"> Email </a> and <a href="tel:07123456789"> Phone </a>

```
<a href="mailto:jane@ibm.co.uk"> Email </a>
```

```
<a href="tel:07123456789"> Phone </a>
```

For more documentation on ways to create HTML links, you can look at the resources <a href="#Resources">below</a>.

## Multiple Pages

Having looked at how to link to other webpages, let's now look at how we can add multiple pages to our website.

So far, we have built a basic single page HTML website with an `index.html` file as your homepage. In order to create additional pages, we must create a project where we have multiple HTML pages. It is good practice to structure your project where your `index.html` file is your homepage and the main directory that reads from subdirectory HTML files. This is not necessary but will keep your project well organised.

### Example

Here, we have an example of a structure, where we have a "Home", an "About me" and a "Contact" page:

<img src="../images/html-pages.png" alt="HTML website structure">

HTML pages that branch off from the `index.html` page still follows the same structure that we have learnt in this course. Since the `index.html` page is our homepage, we want to be able to navigate to these additional pages that we add. As we have just learnt, these can be done through hyperlinks:

```
<a href="html/about.html">About Me</a>
```

## Activity

In this activity, you are going to grow your website from a single page to multiple pages!

1. Create more pages to your website - these can contain anything you like eg. countries you've visited, favourite restaurants, your bucket list.
2. Modify your `index.html` page to direct to your new pages.

<i>Note</i> You will need to refresh your browser tab to see any changes that you make to your HTML files.

## Example finished activity

You can browse the files that have been updated in this folder and try to follow the folder structure going forward.<br>
<a href='./example-finished-activities-session3'>Finished Examples</a>

If you get stuck or would like some inspiration on what to add to you page, you can check out the example finished activity for the updated code [index file](example-finished-activities-session3/index.html) and the newly created [success form page](example-finished-activities-session3/html/formSuccess.html) for the hyperlink section.

<h2 id=Resources>Resources</h2>

- [MDN Web Docs - HTML Links](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a)

<div style="width: 100%">
<a href='html_forms.md'><-- Previous section: HTML Forms</a>
<div align="right"><a href='../session-4/README.md'>Next section: Session 4 Introduction --></a></div>
</div>
