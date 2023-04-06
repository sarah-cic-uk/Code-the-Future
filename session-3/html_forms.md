# Code the Future </>

## Session 3: HTML Forms

## W3: Text input, forms, validation

## HTML Form

HTML Form is a document which stores information from a user using interactive controls. It is used to collect some data from the user.
An HTML form can contains elements such as check box, input box, radio buttons, submit buttons etc to gather different kinds of information such as username, password, contact number and email id.

For example: When a user wants to purchase items from an online shop, he/she usually has to fill forms with the shipping address and credit/debit card details.

A sample HTML form look like below:

![form.png](../images/form.png)

The HTML `<form>` element is used to create an HTML form for user input:

`<form></form>`

`<form> ` has the following attributes which can be set:

- **accept-charset**: Specifies the character encodings used for form submission
- **action**: Specifies where to send the form-data when a form is submitted
- **autocomplete**: Specifies whether a form should have autocomplete on or off
- **enctype**: Specifies how the form-data should be encoded when submitting it to the server (only for method="post")
- **method**: Specifies the HTTP method to use when sending form-data
- **name**: Specifies the name of the form
- **novalidate**: Specifies that the form should not be validated when submitted
- **rel**: Specifies the relationship between a linked resource and the current document
- **target**: Specifies where to display the response that is received after submitting the form

The HTML `<form>` element can contain one or more of the following form elements:

<table style="border-collapse: collapse;
    border-spacing: 0;
    width: 100%;
    display: table;
    border: 1px solid #ccc;">
<tbody><tr>
<th>Tag</th>
<th>Description</th>
</tr>
<tr>
<td>&lt;form&gt;</a></td>
<td> Defines an HTML form for user input</td>
</tr>
<tr>
<td>&lt;input&gt;</a></td>
<td>Defines an input control</td>
</tr>
<tr>
<td>&lt;textarea&gt;</a></td>
<td>Defines a multiline input control (text area)</td>
</tr>
<tr>
<td>&lt;label&gt;</a></td>
<td>Defines a label for an &lt;input&gt; element</td>
</tr>
<tr>
<td>&lt;fieldset&gt;</a></td>
<td>Groups related elements in a form</td>
</tr>
<tr>
<td>&lt;legend&gt;</a></td>
<td>Defines a caption for a &lt;fieldset&gt; element</td>
</tr>
<tr>
<td>&lt;select&gt;</a></td>
<td>Defines a drop-down list</td>
</tr>
<tr>
<td>&lt;optgroup&gt;</a></td>
<td>Defines a group of related options in a drop-down list</td>
</tr>
<tr>
<td>&lt;option&gt;</a></td>
<td>Defines an option in a drop-down list</td>
</tr>
<tr>
<td>&lt;button&gt;</a></td>
<td>Defines a clickable button</td>
</tr>
<tr>
<td>&lt;datalist&gt;</a></td>
<td>Specifies a list of pre-defined options for input controls</td>
</tr>
<tr>
<td>&lt;output&gt;</a></td>
<td>Defines the result of a calculation</td>
</tr>
</tbody></table>

## HTML Input element

The HTML `<input>` element is a fundamental element used to create fields in a form to collect user input. Here's some sample HTML code which creates a name field.

```
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<title>My login page</title>
</head>
<body>
<h2>Login Page</h2>
  <form  action="./formSuccess.html">
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname" value=""><br>
  <label for="lname">Last name:</label><br>
  <input type="text" id="lname" name="lname" value="">
  <input type="submit" value="Submit">
</form>
</body>
</html>

```

The output of the code snippet looks like this.

![sampleform.png](../images/sampleform.png)

The HTML `<input>` element is the most used form element. An `<input>` element can be displayed in many ways, depending on the type attribute.
In the example above it is a single-line text input field.

Here are some more examples:

<table style="border-collapse: collapse;
    border-spacing: 0;
    width: 100%;
    display: table;
    border: 1px solid #ccc;">
 <tbody><tr>
  <th>Type</th>
  <th>Description</th>
 </tr>
 <tr>
  <td>&lt;input type="text"&gt;</td>
  <td>Displays a single-line text input field</td>
 </tr>
 <tr>
  <td>&lt;input type="radio"&gt;</td>
  <td>Displays a radio button (for selecting one of many choices)</td>
 </tr>
 <tr>
  <td>&lt;input type="checkbox"&gt;</td>
  <td>Displays a checkbox (for selecting zero or more of many choices)</td>
 </tr>
 <tr>
  <td>&lt;input type="submit"&gt;</td>
  <td>Displays a submit button (for submitting the form)</td>
 </tr>
 <tr>
  <td>&lt;input type="button"&gt;</td>
  <td>Displays a clickable button</td>
 </tr>
 </tbody>
 </table>

`<input>` field must have a name attribute. Without the name attribute the value of the input field will not be sent.

The `<input type="submit">` defines a button for submitting the form data to a form-handler.
The form-handler is typically a script on the server which processes the input data.
The form-handler is specified in the form's action attribute.

In the above code example the `<label>` tag defines a label for form elements. The "for" attribute of the `<label>` tag should be equal to the "id" attribute of the `<input> ` element to bind them together.

`<input>` attributes

  <table style="border-collapse: collapse;
    border-spacing: 0;
    width: 100%;
    display: table;
    border: 1px solid #ccc;">
 <tbody><tr>
  <th>Attribute</th>
  <th>Description</th>
 </tr>
 <tr>
  <td>checked</td>
  <td>Specifies that an input field should be pre-selected when the page loads (for type="checkbox" or type="radio")</td>
 </tr>
 <tr>
  <td>disabled</td>
  <td>DSpecifies that an input field should be disabled</td>
 </tr>
 <tr>
  <td>max</td>
  <td>Specifies the maximum value for an input field</td>
 </tr>
 <tr>
  <td>maxlength</td>
  <td>Specifies the maximum number of character for an input field</td>
 </tr>
 <tr>
  <td>min</td>
  <td>Specifies the minimum value for an input field</td>
 </tr>
  <tr>
  <td>pattern</td>
  <td>Specifies a regular expression to check the input value against</td>
 </tr>
 <tr>
  <td>readonly</td>
  <td>Specifies that an input field is read only (cannot be changed)</td>
 </tr>
  <tr>
  <td>required</td>
  <td>Specifies that an input field is required (must be filled out)</td>
 </tr>
  <tr>
  <td>size</td>
  <td>Specifies the width (in characters) of an input field</td>
 </tr>
 <tr>
  <td>step</td>
  <td>Specifies the legal number intervals for an input field</td>
 </tr>
 <tr>
  <td>value</td>
  <td>Specifies the default value for an input field</td>
 </tr>
 </tbody>
 </table>

## Activity

1. Create a user registration form. The registration form should:

   - open up the "./formSuccess.html" page on submission
   - contain four text fields - User Name, Email, Password and Confirm password (note type="password" for fields you want to mask)
   - contain one button - Register
   - All text fields must be mandatory
   - User Name field must not allow more than 10 characters

   As part of this task you should create a file called formSuccess.html in the same folder as your index.html with the following content:

   ```
   <!DOCTYPE html>
   <html>
     <head>
       <meta charset="utf-8">
       <title>Form Submission</title>
     </head>
     <body>
       <h1>Form Submitted Successfully</h1>
     </body>
   </html>
   ```

2. If time play around with the different input options available and attributes available.

## Resources

- [W3 Schools](https://www.w3schools.com/html/html_forms.asp)
- [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/form)

<div style="width: 100%">
<a href='html_images_tables.md'><-- Previous section: HTML Images and Tables</a>
<div align="right"><a href='html_hyperlinks.md'>Next section: HTML Hyperlinks --></a></div>
</div>
