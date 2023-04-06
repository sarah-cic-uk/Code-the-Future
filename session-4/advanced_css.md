# Code the Future </>

## Session 4: Advanced CSS

## More CSS Selectors and More Advanced Concepts

- **Pseudo-Classes**

  - This can be used to style an element based on something other than the structure of the document.

    ```css
    /* Makes all unvisited links purple with no text decoration (i.e. not underlined)*/
    a:link {
    	color: purple;
    	text-decoration: none;
    }

    /* Makes all visited links gray and with a line through */
    a:visited {
    	color: gray;
    	text-decoration: line-through;
    }

    /* Makes links purple and bold when hovered over */
    a:hover {
    	color: purple;
    	font-weight: bold;
    }
    ```

- **Universal Selector**
  - This acts as a wildcard that matches to all available elements and it is denoted by an `*`.
  - This is used to apply a specific style on every element on a page.
    ```css
    /* makes all the text to use Arial or any sans-serif text available and to to be 15px */
    * {
    	font: 15px Arial, sans-serif;
    }
    ```
- **Inheritance**

  - Properties (e.g. color, font size) are inherited by the descendants of the elements those styles are applied to.

    ```css
    /* you can apply something like this to your CSS if you want all the text on the page to be green and use a specific font*/
    p,
    div,
    h1,
    h2,
    h3,
    ul,
    ol,
    dl,
    li {
    	font-family: Arial, Helvetica, sans-serif;
    	color: green;
    }

    /* alternatively, using inheritance, you can simply use: */
    body {
    	font-family: Arial, Helvetica, sans-serif;
    	color: green;
    }
    ```

- **Measurement Units**

  | Absolute        | Relative |
  | --------------- | -------- |
  | Pixel (px)      | em       |
  | Inch (in)       | rem      |
  | Centimeter (cm) | vm       |
  | Millimeter (mm) | vh       |
  | Points (pt)     | %        |

  - **Absolute** - fixed units; always going to be the same regardless of the screen size
  - **Relative** - the elements are scaled based on the rendering mediums

## Layout in CSS

There are different ways to align elements on the page easier and the most flexible way.

### Float

- These properties can be used to specify how an element should float and which elements and where it can float beside a cleared element.
- The `float` is used to position and format a content and can have one of the following:
  - `left` or `right` - element floats to the left or right of its container
  - `none` - the default value; the element is displayed by does not float
  - `inherit` - the element inherit the float value of its parent
- This method requires more effort.

### Flexbox

CSS Flexible Layout Module (Flexbox) is a new technique to improve the way the element are laid out on a page by managing alignments of items, directions, and order in the container. This avoids the use of floats.

![image](../images/session4/flexbox_components.png)

- Main Components of a Flexbox are:
  - _Flex Container_ - it groups the Flex Items
  - _Flex Items_ - it is contained in a Flex Container
  - _Main Axis_ - how the items are laid out across the page (from left to right)
  - _Cross Axis_ - how the items are laid out from top to bottom
- You can define a value for the following properties for the Flex Container:
  - `display: flex || inline-flex` to make the container flexible
  - `flex-direction: row || row-reverse || column || column-reverse` to defined the direction that the container wants to set for the flex items
  - `flex-wrap: nowrap || wrap` to define whether it should be displayed on a single or multiple lines
  - `flex-flow: row wrap` combining the direction and the wrap
  - `justify-content: flex-start || flex-end || center || space-between || space-around || space-evenly` align the elements along the main axis of the container
  - `align-items: stretch || flex-start || flex-end || center || baseline` align the element along the cross axis of the container
  - `align-content: stretch || flex-start || flex-end || center || space-between || space-around` similar to align-items but used if it has extra space in the cross axis
- You can define the following properties for the Flex Items:
  - `order: 0 || [number]` helps add an ordering of the items
  - `align-self: auto || stretch || flex-start || flex-end || center || baseline` for aligning individual flex items
  - `flex-grow: 0 || [number]`, `flex-basis: auto || [length]`, `flex-shrink: 1 || [number]` change the size of the flex items
- For more information, checkout [Complete Guide to CSS Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)

### CSS Grid

Another modern technique to improve the way the element are laid out on a page which does not make use of floats. Unlike CSS Flexbox, CSS Grid is two-dimensional layout - you can divide rows and columns simultaneously.

![image](../images/session4/grid_components.png)

- Main components of a Grid are:

  - _Grid Containers_ - it groups the Grid items
  - _Grid Items_ - what is inside the Grid container
  - _Column Axis_ - vertical direction
  - _Row Axis_ - horizontal direction
  - _Grid Lines_ - horizontal and vertical lines that separate rows and columns in a Grid container

- More complete information about CSS Grids can be found in [Complete Guide to CSS Grid](https://css-tricks.com/snippets/css/complete-guide-grid/)

## CSS Preprocessors

CSS has limitations and it is hard to maintain - since it's not a programming language, it cannot define variables, nesting selectors, expressions, functions etc. **CSS Preprocessors** address these. Some of the most popular ones are:

- [Less](https://lesscss.org/)
- [Sass (Syntactically Awesome Style Sheets)](https://sass-lang.com/)
- [Scss (Sassy CSS)](https://medium.com/@jgoz/sassy-css-scss-quick-guide-b38f51c6868a)
- [Stylus](https://stylus-lang.com/)

## Responsive Web Design

Responsive Web Design allows to display web pages based on the device the user is using. The web page components are adjusted based on the screen size to provide an optimal user experience.

### CSS Media Queries

Media queries looks at the capability of the device and it can be used to check things like:

- Viewport width and height
- Device width and height
- Orientation of the device (portrait or landscape)
- Resolution

The syntax contains a _media type_ which can contain one or more expressions that resolves to either true or false.

```css
@media not|only mediatype and (expressions) {
  CSS-Code;
}

/* an example */
@media screen and (min-width: 800px) {
  body {
    background-color: blue;
  }
}
```

It is also possible to use a different stylesheet for different media. The different types are `all`, `print`, `screen`, and `speech`. This can be added inside the `<head>` element of the HTML Page.

```html
<link
	rel="stylesheet"
	media="mediatype and|not|only (expressions)"
	href="screen.css"
/>
```

### CSS Frameworks

CSS Frameworks provide an abstraction for common web designs and makes it easier for developers to implement the styling and "responsiveness" of their web pages as well enables cross-browser functionality. A CSS Framework is a collection of CSS Stylesheets that are ready to use - helps you save time as you don't have to create the styling from scratch. Here are some examples:

- **Bootstrap**

  - This is the most popular and (arguably) the best CSS framework.
  - It comes with pre-defined components - which are built using HTML, SASS, and JavaScript and has a large community support.
  - It provides a very detailed documentation with layouts that are easy to understand.
  - Check out [https://getbootstrap.com/](https://getbootstrap.com/) for more information and also see some live-demos.

- **Tailwind CSS**

  - This is highly customisable to provides the building blocks instead of pre-defined components.
  - You get a set of CSS Helper Classes which can be used to create your own custom design.
  - Checkout [https://tailwindcss.com/](https://tailwindcss.com/) for more information and also [Tailwind CSS Github Page](https://github.com/tailwindlabs/tailwindcss).

- **Materialize CSS**

  - Fully responsive front-end framework and it has a shallow learning curve - it has a comprehensive documentation.
  - It provides free [Materialize Admin Templates](https://themeselection.com/20-top-premium-free-material-design-admin-template/).
  - Check out [https://materializecss.com/](https://materializecss.com/) for more information.

- **Material Design Lite**

  - Based on Material Design created by Google, and it can be used with [Elm](<https://en.wikipedia.org/wiki/Elm_(programming_language)>), a language for Graphical User Interfaces.
  - It provides an out-of-the-box solution that can also be customised.
  - Check out [https://getmdl.io/components/index.html](https://getmdl.io/components/index.html) for more information.

- **Foundation**
  - Advanced front-end CSS Framework which is built with HTML, CSS, SASS, and JavaScript.
  - This uses a mobile-first approach and typically used for larger web application.
  - Check out [https://get.foundation/](https://get.foundation/) for more information.

---

## Example finished activity

You can browse the files that have been updated in this folder and try to follow the folder structure going forward.<br>
<a href='./example-finished-activities-session4'>Finished Examples</a>

If you get stuck or would like some inspiration on what to add to you page, you can check out the [index file](example-finished-activities-session4/index.html) for the updated code, here for the [success form page](example-finished-activities-session4/html/formSuccess.html), and here for the new [stylesheet](example-finished-activities-session4/style/myStyleSheet.css) we have created.

For the advanced CSS you can follow these links ot the files created in the folder.<br>
[Flexbox Example](example-finished-activities-session4/html/flexbox.html)<br>
[Grid Example](example-finished-activities-session4/html/grid_sample.html)<br>
[Flex and Grid Stylesheet](example-finished-activities-session4/style/layout_stylesheet.css)<br>

## Useful Links

- [CSS Cheat Sheet](https://htmlcheatsheet.com/css/)
- [More CSS Tutorials in Tutorialspoint](https://www.tutorialspoint.com/css/index.htm)
- [CSS Reference @ W3 Schools](https://www.w3schools.com/cssref/default.asp)

<div style="width: 100%">
<a href='introduction_to_css.md'><-- Previous section: Introduction to CSS</a>
<div align="right"><a href='session4-activities.md'>Next section: Session 4 Activities --></a></div>
</div>
