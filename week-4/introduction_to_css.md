# Code the Future </>

## Week 4: Basic CSS
## What is CSS?

* **CSS** = **C**ascading **S**tyle **S**heets
    * A styling language used for website layout and design
    * You can choose the fonts, colors, layout, etc. of a web page
        * It makes your web pages less bland and more attractive!!
    * This is **not** a Programming Language

## How to Use CSS with HTML

### Inline CSS
* Small segments of CSS written into the code in an HTML Element
* The style is only applied to a single element

    ``` html
    ...

    <p style="color:blue">
        Hello World!!
    </p>
    ```

### Internal CSS
* Using `<style>` tags within the header section of the HTML file
* The style is only applied in that single HTML file
      
    ```html
    ...
    <html>
        <head>

            <title>My First Website</title>

            <style type="text/css">

                h1 {
                    color: blue;
                }

            </style>

        </head>
        <body>
            <h1>This text is blue</h1>
        </body>
    </html>
    ```

### External CSS
* Linking an external (separate) `.css` file
* This can be re-used in one or more HTML files (when it is imported)  and it also enables separation of presentation and content
    
    ```html
    <!-- HTML File (index.html) -->
    ...

    <head>
    <title>My First Website</title>
    <link rel="stylesheet" type="text/css" href="myStyleSheet.css />
    </head>
    ```
      
    ```css
    /* CSS File located in the same directory as index.html (myStyleSheet.css) */
    p {
        color: blue;
    }
    ```

## CSS Syntax

CSS syntax consists of a plain text called a *Style Sheet* which are separated into blocks of code containing *rules*.

![img](../images/week4/css_format.png)

It has [*Selectors*](#selector) that declare the elements in the HTML Document where the style is applied. This is followed by a [*Declaration Block*](#declaration) enclosed by curly braces that contains one or more [*Declarations*](#declaration), separated by a semicolon. Each *Declaration* includes a [*Property*](#property), a colon, and its [*Value*](#value).

White spaces are ignored - declarations can be written in separate lines to make it more readable.

```css
p { 
    color: blue;
    font-weight: bold;
    font-size: 14px;
}
```

### Selector

* The selectors are used to target a specific element or range of elements, where a style is applied on a web page 
* There is a [wide range of selectors](../02-Advanced_CSS/README.md/#css-selectors-advanced) and each selector can have an `ID` and/or `Class` attributes.

    > **Class Attribute** <br/>
    This attribute allows you to define style rules that apply to *more than one element*.<br/>
    The example below shows a `class` called `blue-and-bold` applied to a paragraph `<p>` selector. <br/>
    ![img](../images/week4/class_separator_html.png)<br/>
    To declare rules in your CSS for that `class`, write a separator prefixed with a `"."`. The style defined here is applied to any HTML element with `class="blue-and-bold"`.
    ![img](../images/week4/class_separator_css.png)
    <br/><br/>
    **ID Attribute** <br/>
    This attribute only allows you to define style rules that apply to *a single element*. The `id` attribute is a unique idenfier within the document and cannot share the same `id` value in the same web page.<br/>
    The example below shows multiple Paragraph `<p>` elements with different `id`'s. <br/>
    ![img](../images/week4/id_separator_html.png)<br/>
    To declare rules in your CSS for each `id`, write a separator prefixed with a `"#"`.<br/>
    ![img](../images/week4/id_separator_css.png)<br/>

### Declaration

* The Selector is followed by a *Declaration Block*, enclosed with curly braces`{}`, that contains one or more *Declarations* or rules
* Each *Declaration* contains a [*Property*](#Property) and a [*Value*](#Value)

### Property

* Name of the attribute you want to style for example `border`, `color`, `background`, `position` etc.
* A property must have a Value

### Value

* This defines the Property or the values allocated for the Property

---

## Activity: Styling your HTML Page

In this exercise, you will add styling to your `index.html` page that you've created and updated in Weeks 2 and 3.  

1. Create a new file in the same location where you save your index.html and call it `mystylesheet.css`
2. Open this new file in Visual Studio Code and copy the following text:

    ```css
    .greentext {
        font-family: Arial, Helvetica, sans-serif;
        color: green;
    }
    ```
3. Open your `index.html` on Visual Studio Code and then add the following inside the `<head>`

    ```html
    <link rel="stylesheet" href="mystylesheet.css"/>
    ```
4. In the `index.html`, add two new paragraphs inside the `<body>` element, one with class `.greentext`
    ```
    <p>This is the first paragraph</p>
    <p class="greentext">This is another paragraph, which is green and using a different font</p>
    ```
5. Open `index.html` on a web browser and you should see changes in the font and the colour of the text of the second paragraph
6. Update the CSS to make some more changes to the page and style it however you want

---

## Web Browser Developer Tools

Modern web browsers have support for web developer tools (*devtools*) that will help designers/developers debug the front-end. This is covered in more detail in Week 2 or click on each link to learn more about the different devtools for each web browser: 

* [Firefox](https://developer.mozilla.org/en-US/docs/Tools)
* [Google Chrome](https://developer.chrome.com/docs/devtools/)
* [Internet Explorer and Microsoft Edge](https://docs.microsoft.com/en-us/previous-versions/windows/desktop/legacy/hh968260(v=vs.85))
* [Safari](https://support.apple.com/en-gb/guide/safari/sfri20948/mac)
* [Opera](https://dev.opera.com/extensions/dev-tools/)

For this example, we will use Chrome. To view the styles applied on the page, select an element and the styles defined for that element will be displayed in the tab called **Styles**.

![image](../images/week4/css_devtools.png)

---

## Useful Links

* [CSS Cheat Sheet](https://htmlcheatsheet.com/css/)
* [More CSS Tutorials in Tutorialspoint](https://www.tutorialspoint.com/css/index.htm)


<div style="width: 100%">
<a href='README.md'><-- Previous Section: Week 4 Introduction</a>
<div align="right"><a href='advanced_css.md'>Next Section: Advanced CSS --></a></div>
</div>