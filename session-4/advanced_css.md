# Code the Future </>

## Session 4: Advanced CSS

## More CSS Selectors and More Advanced Concepts

**Pseudo-Classes**

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

**Universal Selector**
  - This acts as a wildcard that matches to all available elements and it is denoted by an `*`.
  - This is used to apply a specific style on every element on a page.
    ```css
    /* makes all the text to use Arial or any sans-serif text available and to to be 15px */
    * {
      font: 15px Arial, sans-serif;
    }
    ```
**Inheritance**

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

**Measurement Units**

  | Absolute        | Relative |
  | --------------- | -------- |
  | Pixel (px)      | em       |
  | Inch (in)       | rem      |
  | Centimeter (cm) | vm       |
  | Millimeter (mm) | vh       |
  | Points (pt)     | %        |

  - **Absolute** - fixed units; always going to be the same regardless of the screen size
  - **Relative** - the elements are scaled based on the rendering mediums

## CSS Preprocessors

CSS has limitations and it is hard to maintain - since it's not a programming language, it cannot define variables, nesting selectors, expressions, functions etc. **CSS Preprocessors** address these. Some of the most popular ones are:

<ul>
<li><a href='https://lesscss.org/' target='_blank'>Less</a></li>
<li><a href='https://sass-lang.com/' target='_blank'>Sass (Syntactically Awesome Style Sheets)</a></li>
<li><a href='https://medium.com/@jgoz/sassy-css-scss-quick-guide-b38f51c6868a' target='_blank'>Scss (Sassy CSS)</a></li>
<li><a href='https://stylus-lang.com/' target='_blank'>Stylus</a></li>
</ul>

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

**Bootstrap**

  - This is the most popular and (arguably) the best CSS framework.
  - It comes with pre-defined components - which are built using HTML, SASS, and JavaScript and has a large community support.
  - It provides a very detailed documentation with layouts that are easy to understand.
  - Check out <a href='https://getbootstrap.com/' target='_blank'>https://getbootstrap.com/</a> for more information and also see some live-demos.

  Example Setup for using Bootstrap followed below:

  - Add this script section to your page. It's blank inside as the src of the scripts is being hosted by Bootstrap

  ```html
  <script
    src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha3/dist/js/bootstrap.bundle.min.js"
    integrity="sha384-ENjdO4Dr2bkBIFxQpeoTz1HIcje39Wm4jDKdf19U8gI4ddQ3GYNS7NTKfAdVQSZe"
    crossorigin="anonymous"
  ></script>
  ```

  - In you `<head></head>` section add this part inside. this sets up a link to the styling elements/css files hosted by Bootstrap.

  ```html
  <link
    href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha3/dist/css/bootstrap.min.css"
    rel="stylesheet"
    integrity="sha384-KK94CHFLLe+nY2dmCWGMq91rCGa5gtU4mk92HdvYe+M/SXH301p5ILy+dN9+nJOZ"
    crossorigin="anonymous"
  />
  ```

  - Next you can add this html inside your `<body></body>` section to try out this little navigation pill bar.

  ```html
  <ul
    class="nav nav-pills nav-fill gap-2 p-1 small bg-primary rounded-5 shadow-sm"
    id="pillNav2"
    role="tablist"
    style="
        --bs-nav-link-color: var(--bs-white);
        --bs-nav-pills-link-active-color: var(--bs-primary);
        --bs-nav-pills-link-active-bg: var(--bs-white);
      "
  >
    <li class="nav-item" role="presentation">
      <button
        class="nav-link active rounded-5"
        id="home-tab2"
        data-bs-toggle="tab"
        type="button"
        role="tab"
        aria-selected="true"
      >
        Home
      </button>
    </li>
    <li class="nav-item" role="presentation">
      <button
        class="nav-link rounded-5"
        id="profile-tab2"
        data-bs-toggle="tab"
        type="button"
        role="tab"
        aria-selected="false"
      >
        Profile
      </button>
    </li>
    <li class="nav-item" role="presentation">
      <button
        class="nav-link rounded-5"
        id="contact-tab2"
        data-bs-toggle="tab"
        type="button"
        role="tab"
        aria-selected="false"
      >
        Contact
      </button>
    </li>
  </ul>
  ```

    <img src="https://raw.githubusercontent.com/sarah-cic-uk/Code-the-Future/main/images/session4/Pill-navbar.png" alt="pill navbar" width="80%">


What the above peice of code is doing is mainly setting classes that are being set or edited with CSS that is coming from Bootstrap, similar to how we have shown you to select the classes you added to certain elements.

Reference to the page of usable Bootstrap classes: <a href='https://getbootstrap.com/docs/5.3/getting-started/introduction/' target='_blank'>https://getbootstrap.com/docs/5.3/getting-started/introduction/</a>

**Tailwind CSS**

  - This is highly customisable to provides the building blocks instead of pre-defined components.
  - You get a set of CSS Helper Classes which can be used to create your own custom design.
  - Checkout <a href='https://tailwindcss.com/' target='_blank'>https://tailwindcss.com/</a> for more information and also <a href='https://github.com/tailwindlabs/tailwindcss' target='_blank'>Tailwind CSS Github Page</a>.

**Materialize CSS**

  - Fully responsive front-end framework and it has a shallow learning curve - it has a comprehensive documentation.
  - It provides free <a href='https://themeselection.com/20-top-premium-free-material-design-admin-template/' target='_blank'>Materialize Admin Templates</a>.
  - Check out <a href='https://materializecss.com/' target='_blank'>https://materializecss.com/</a> for more information.

**Material Design Lite**

  - Based on Material Design created by Google, and it can be used with <a href='https://en.wikipedia.org/wiki/Elm_(programming_language)' target='_blank'>Elm</a>, a language for Graphical User Interfaces.
  - It provides an out-of-the-box solution that can also be customised.
  - Check out <a href='https://getmdl.io/components/index.html' target='_blank'>https://getmdl.io/components/index.html</a> for more information.

**Foundation**
  - Advanced front-end CSS Framework which is built with HTML, CSS, SASS, and JavaScript.
  - This uses a mobile-first approach and typically used for larger web application.
  - Check out <a href='https://get.foundation/' target='_blank'>https://get.foundation/</a> for more information.

---

## Example finished activity

You can browse the files that have been updated in this folder and try to follow the folder structure going forward.<br>
<a href='https://raw.githubusercontent.com/sarah-cic-uk/Code-the-Future/main/session-4/example-finished-activities-session4/index.html' target='_blank'>Finished Examples</a>

If you get stuck or would like some inspiration on what to add to you page, you can check out the <a href='https://raw.githubusercontent.com/sarah-cic-uk/Code-the-Future/main/session-4/example-finished-activities-session4/index.html' target='_blank'>index file</a> for the updated code, here for the <a href='https://raw.githubusercontent.com/sarah-cic-uk/Code-the-Future/main/session-4/example-finished-activities-session4/html/formSuccess.html' target='_blank'>success form page</a>, and here for the new <a href='https://raw.githubusercontent.com/sarah-cic-uk/Code-the-Future/main/session-4/example-finished-activities-session4/style/myStyleSheet.css' target='_blank'>stylesheet</a> we have created.

For the advanced CSS you can follow these links ot the files created in the folder.
<ul>
<li><a href='https://raw.githubusercontent.com/sarah-cic-uk/Code-the-Future/main/session-4/example-finished-activities-session4/html/flexbox.html' target='_blank'>Flexbox Example</a></li>
<li><a href='https://raw.githubusercontent.com/sarah-cic-uk/Code-the-Future/main/session-4/example-finished-activities-session4/html/grid_sample.html' target='_blank'>Grid Example</a></li>
<li><a href='https://raw.githubusercontent.com/sarah-cic-uk/Code-the-Future/main/session-4/example-finished-activities-session4/style/layout_stylesheet.css' target='_blank'>Flex and Grid Stylesheet</a></li>
</ul>


## Useful Links

<ul>
<li><a href='https://htmlcheatsheet.com/css/' target='_blank'>CSS Cheat Sheet</a></li>
<li><a href='https://www.tutorialspoint.com/css/index.htm' target='_blank'>More CSS Tutorials in Tutorialspoint</a></li>
<li><a href='https://www.w3schools.com/cssref/default.asp' target='_blank'>CSS Reference @ W3 Schools</a></li>
</ul>

<div style="width: 100%">
<a href='layouts.md'><-- Previous section: Layouts in CSS</a>
<div align="right"><a href='session4-activities.md'>Next section: Session 4 Activities --></a></div>
</div>
