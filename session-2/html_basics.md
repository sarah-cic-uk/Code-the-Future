# Code the Future </>

## Session 2: HTML Basics

## What is HTML

HTML (Hypertext Markup Language) is the code that is used to structure a web page and how its content is displayed online and is known as the backbone of the internet.

HTML consists of a series of elements, which you use to enclose, or wrap, different parts of the content to make it appear a certain way, or act a certain way.

## The structure of a HTML page

    <!DOCTYPE html>
    <html>
        <head>
    	    <meta charset="utf-8">
    	    <title>My example page</title>
        </head>
        <body>
        </body>
    </html>

`<!DOCTYPE html>`

- This the HTML5 doctype, it is required at the top of every HTML document and it makes sure your document behaves correctly.

`<html></html>`

- The html element, also know as the root element, wraps all the content that is in the page.

`<head></head>`

- The head element, this is a container for all the stuff you want to include on the page that isn't the content you are showing. This includes things like keywords and a page description that you want to appear in search results, CSS to style our content, character set declarations, and more.

`<meta charset="utf-8">`

- This element sets the character set your document should use, here we set the charset="uft-8" which includes most characters from the vast majority of written languages.

`<title></title>`

- The title element. This sets the title of your page, which is the title that appears in the browser tab the page is loaded in.

`<body></body>`

- The body element. This contains all the content that you want to show to on your page, whether that's text, images, videos, or anything else.

## What does an HTML element look like

![html tag example](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/HTML_basics/grumpy-cat-small.png)

There are many different HTML elements that can be used for different things, some good resources to find out about different ones you can use are:

- [W3 Schools](https://www.w3schools.com/tags/default.asp)
- [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/HTML/Element)

## Common elements for marking up text

### Headings

Heading elements allow you to specify that certain parts of your content are headings — or subheadings. In the same way that a book has the main title, chapter titles, and subtitles. There are heading levels 1-6 that you can use throughout your page but you'll only want one `<h1>` which will be the main title of your page.

```
<h1>My main title</h1>
<h2>My top level heading</h2>
<h3>My subheading</h3>
<h4>My sub-subheading</h4>
<h5>My small subheading</h5>
<h6>My extra small heading</h6>
```

### Paragraphs

`<p>` elements are for containing paragraphs of text; you'll use these a lot when marking up regular content.

```
<p>This is a single paragraph</p>
```

### Lists

The most common list types are ordered and unordered lists:

1.  **Unordered lists** are for lists where the order of the items doesn't matter, such as a shopping list. These are wrapped in a `<ul>` element. These lists will show as bullet points.
2.  **Ordered lists** are for lists where the order of the items does matter, such as a recipe. These are wrapped in an `<ol>` element. These lists will show as numbered bullet points.

```
<p>My Shopping list</p>
<ul>
  <li>Pizza</li>
  <li>Bread</li>
  <li>Crisps</li>
</ul>


<p>The steps to follow to make toast are:</p>
<ol>
  <li>Get 2 slices of bread</li>
  <li>Put the bread in the toaster</li>
  <li>Press the toaster down</li>
</ol>

```

## Resources

- [W3 Schools](https://www.w3schools.com/tags/default.asp)
- [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/HTML/Element)

<div style="width: 100%">
<a href='README.md'><-- Previous section: Session 2 Introduction</a>
<div align="right"><a  href='dev_tools.md'>Next section: Chrome Dev Tools --></a></div>
</div>
