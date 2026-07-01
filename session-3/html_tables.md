# Code the Future </>

## Session 3: HTML Tables

## HTML Tables

HTML tables allow you to display information, or tabular data, in organised rows and columns. In order to display data in a table, there are a number of tags that are necessary:

<table style="width:100%" border="true">
  <tr>
    <th>Tag</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>&lttable&gt&lt/table&gt</td>
    <td>Defines a table. This tag needs to be wrapped around all of the table's contents and tags to ensure that they are formatted as a table.</td>
  </tr>
  <tr>
    <td>&lttr&gt&lt/tr&gt</td>
    <td>Defines a row of the table. This tag needs to be wrapped around the all of the content for every row that is defined.</td>
  </tr>
  <tr>
    <td>&ltth&gt&lt/th&gt</td>
    <td>Defines the header of a row. By default, the text in this tag is bold and centered.</td>
  </tr>
  <tr>
    <td>&lttd&gt&lt/td&gt</td>
    <td>Defines the contents of the table.</td>
  </tr>
    <tr>
    <td>&ltcaption&gt&lt/caption&gt</td>
    <td>(Optional) Defines the caption of the table. This tag needs to immediately follow the &lttable&gt tag.</td>
  </tr>
</table>

### Example

In this example, we have a basic table with three columns, a row defining the headers and two rows defining some data for types of dogs.

```
<table>
  <caption>Types of Dogs</caption>
  <tr>
    <th>Name</th>
    <th>Age</th>
    <th>Breed</th>
  </tr>
  <tr>
    <td>Loxie</td>
    <td>1</td>
    <td>Poodle</td>
  </tr>
  <tr>
    <td>Pippa</td>
    <td>8</td>
    <td>Yorkshire Terrier</td>
  </tr>
</table>
```

## Activity

In this activity, we are going to be building upon your webpage that you started about yourselves. Add these HTML elements and you'll start to see your webpage develop more character!

In your `index.html` file, add the following to your webpage:

1. An image of yourself, or something you love, to go alongside the text you previously inputted.
2. A table containing anything you'd like! This could be hobbies, pets, children, favourite foods etc.

<i>Note</i> You will need to refresh your browser tab to see any changes that you make to your `index.html` file.

## Resources

<ul>
<li><a href='https://www.w3schools.com/html/html_tables.asp' target='_blank' title="W3 Schools - Tables">W3 Schools - Tables</a></li>
</ul>

<div style="width: 100%">
<a href='html_images.md'><-- Previous section: HTML Images</a>
<div align="right"><a href='html_forms.md'>Next section: HTML Forms --></a></div>
</div>
