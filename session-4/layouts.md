# Code the Future </>

## Session 4: Layouts

## Layout in CSS

There are different ways to align elements on the page easier and are used to make the best use of space within your webpage.

Here we will be going over the three ways that this can be done.

### Float

- These properties can be used to specify how an element should float and which elements and where it can float beside a cleared element.
- The `float` is used to position and format a content and can have one of the following:
  - `left` or `right` - element floats to the left or right of its container
  - `none` - the default value; the element is displayed by does not float
  - `inherit` - the element inherit the float value of its parent
- This method requires more effort.

### Flexbox

CSS Flexible Layout Module (Flexbox) is a new technique to improve the way the element are laid out on a page by managing alignments of items, directions, and order in the container. This avoids the use of floats.

  <img src="https://raw.githubusercontent.com/sarah-cic-uk/Code-the-Future/main/images/session4/flexbox_components.png" alt="flexbox components" width="80%">


Main Components of a Flexbox are:
  - _Flex Container_ - it groups the Flex Items
  - _Flex Items_ - it is contained in a Flex Container
  - _Main Axis_ - how the items are laid out across the page (from left to right)
  - _Cross Axis_ - how the items are laid out from top to bottom

You can define a value for the following properties for the Flex Container:
  - `display: flex || inline-flex` to make the container flexible
  - `flex-direction: row || row-reverse || column || column-reverse` to defined the direction that the container wants to set for the flex items
  - `flex-wrap: nowrap || wrap` to define whether it should be displayed on a single or multiple lines
  - `flex-flow: row wrap` combining the direction and the wrap
  - `justify-content: flex-start || flex-end || center || space-between || space-around || space-evenly` align the elements along the main axis of the container
  - `align-items: stretch || flex-start || flex-end || center || baseline` align the element along the cross axis of the container
  - `align-content: stretch || flex-start || flex-end || center || space-between || space-around` similar to align-items but used if it has extra space in the cross axis   

You can define the following properties for the Flex Items:
  - `order: 0 || [number]` helps add an ordering of the items
  - `align-self: auto || stretch || flex-start || flex-end || center || baseline` for aligning individual flex items
  - `flex-grow: 0 || [number]`, `flex-basis: auto || [length]`, `flex-shrink: 1 || [number]` change the size of the flex items
- For more information, checkout <a href='https://css-tricks.com/snippets/css/a-guide-to-flexbox/' target='_blank'>Complete Guide to CSS Flexbox</a>

### CSS Grid

Another modern technique to improve the way the element are laid out on a page which does not make use of floats. Unlike CSS Flexbox, CSS Grid is two-dimensional layout - you can divide rows and columns simultaneously.

  <img src="https://raw.githubusercontent.com/sarah-cic-uk/Code-the-Future/main/images/session4/grid_components.png" alt="grid components" width="80%">


Main components of a Grid are:

  - _Grid Containers_ - it groups the Grid items
  - _Grid Items_ - what is inside the Grid container
  - _Column Axis_ - vertical direction
  - _Row Axis_ - horizontal direction
  - _Grid Lines_ - horizontal and vertical lines that separate rows and columns in a Grid container

More complete information about CSS Grids can be found in <a href='https://css-tricks.com/snippets/css/complete-guide-grid/' target='_blank'>Complete Guide to CSS Grid</a>

<div style="width: 100%">
<a href='introduction_to_css.md'><-- Previous section: Introduction to CSS</a>
<div align="right"><a href='advanced_css.md'>Next section: Advanced CSS --></a></div>
</div>
