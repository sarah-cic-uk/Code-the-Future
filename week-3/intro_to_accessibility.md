# Code the Future </>

## Week 3: Accessibility

## Accessibility
In this section we are going to talk about why you need to strive to make accessible applications, how to make your applications more accessibile and explain some good practices you can follow.

So what do we mean when we say 'accessible'? It means making your web or mobile applications in such a way so that it can be used by as many people as possible.

This includes making your content and design clear and simple enough so that most people can use it without needing to adapt it, while supporting those who do need to adapt things.

This includes supporting those with: 
- impaired vision
- motor difficulties
- cognitive impairments or learning disabilities
- deafness or impaired hearing. 

**Apps should be designed with accessibility in mind from the very beginning!**

Why?? Because over 1 billion people have disabilities... That's 1/7th of the population!

Making your website more accessible not only benefits those who need the additional support but generally means the websites are easier to use and gain higher rankings on search engines. It's a win-win all round! Not to mention that in certain cases (like in the public sector) it is a legal requirement for websites to meet certain accessibility requirements e.g. [WCAG](https://www.gov.uk/service-manual/helping-people-to-use-your-service/understanding-wcag).

## Common Assistive Technologies

- Text-to-speech: Reads out textual information from a page to the user
- Voice Command: Lets the user control the application using their voice
- Colour Contrasting: Reads out textual information from a page to the user

## Aria

To ensure applications are accessible we need to provide semantic information about components, structures, and expected behaviors, so that assistive technologies can provide relevant information to their users. The Accesible Rich Internet Application (ARIA) specification provides a series of roles and properties that can help with this. It helps defines accessible user interface elements which allow you to describe behaviors and structural information to assistive technologies in document-level markup.

### Aria Roles
This is an attribute you can add to a element to help clarify what the expected behaviour should be. There a variety of [aria roles](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles) available but a few of the most common ones include:

- **Alert**: Used to alert the user that something has changed on their page - screen readers will start reading the alert when it pops up.

- **Button**: Should be used when we expect the user to interact with the element via a click and expect a response

- **Dialog**: Used to mark a dialog/window that separates content from the rest of the page and are generally placed on top of the rest of the page content

- **Form**: A [landmark](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/ARIA_Techniques#landmark_roles) role used to identify a group of elements that together create a form.

- **List**: Used to identify a list of items e.g. a menu. Usually used in with the listitem role, which is used to identify a list item contained inside the list.

- **ListItem**: Used to identify an item inside a list of items e.g. a submenu or button.

- **Navigation**: A landmark role that identifies a group of links that are used to naviage aroound a website.

Example of setting a role

```<li role="menuitem">Exit</li>```


### Aria States and Properties
[Aria States and Properties](https://www.w3.org/TR/wai-aria-1.0/states_and_properties) support the ARIA roles that exist on a page and can supply extra user interface information that is useful for assistive technologies. Whenever these states or properties change the assistive technology can pickup the update and alert the user that a change has occurred. 

 e.g. 'aria-disabled' is a state saying whether a particular item is interactive.

## Semantics
Structuring your web application is a good starting point towards good accessibility practices.

See [this page on HTML Semantics](http://web-accessibility.carnegiemuseums.org/foundations/semantic/) for more information. 

## Good Practice:
<!-- ToDo: discuss some good practices and tidy the below -->

**Aria-label**: can be used on any html element. Screen readers announce the label text when on the element e.g. reads the label instead of the button text. Use it in cases where a text label is not visible on the screen.

**Aria-labelledby**: allows label to be set based on other IDs. Role elements good to do with these e.g. radio group. Can concatenate several labels into one . Can be used on hidden elements. Always takes precedence. If there is visible text labeling the element, use aria-labelledby instead.

**Aria-describedby**: similar to labelledby but gives additional info to help the user. e.g. helper text that isn't always visible
		
**Aria-owns**: tells screen reader than one element is a child of another

Notes:

    None of the above should be used for non interactive elements like divs or spans
    Recommended for form inputs
    Some interactive items like buttons don??t need it
    Over-using can be bad too
    Remember to update your labels when you change your UI!


## Activity

1. Download the Chrome Accessibility Plugins 

- [Screen Reader](https://chrome.google.com/webstore/detail/screen-reader/kgejglhpjiefppelpmljglcjbhoiplfn)

- [Aria DevTools Chrome Plugin](https://chrome.google.com/webstore/detail/aria-devtools/dneemiigcbbgbdjlcdjjnianlikimpck?hl=en/)

- [Visual Aria Chrome Plugin](https://chrome.google.com/webstore/detail/visual-aria/lhbmajchkkmakajkjenkchhnhbadmhmk)

    You will have to enable these Plugins from the Extension menu if disabled. You can do this if you go to chrome://extensions/ and hit the toggle icon so that all the necessary plugins are blue.


2. Open up different webpages and explore with the Dev Tools

    The best way to understand how the tools work is to open up a few websites and try interacting with the pages.

    Try viewing the pages both with the dev tools, and without, so you can get a feel for how content has been structured.

    You can use the **tab** button to cycle through the items shown on a page in the dev tools, use **enter** to select an option or fire a button and **Alt + tab** will let you move backwards. You can see some more examples of in-depth controls [here](https://webaim.org/techniques/keyboard/).

    Some example websites you can open up:
    - https://www.google.co.uk
    - https://www.myemergencydr.com/
    - https://www.internetrix.com.au/

3. Improve your current code so it is more Accessibility Friendly

    - Add Aria elements to your login form

        ```
        <!DOCTYPE html>
        <html>
        <head>
        <meta charset="utf-8">
        <title>My login page</title>
        </head>
        <body>  
        <h2>Login Page</h2>
        <form role="form" action="/action.js">
            <label for="first name">First name:</label><br>
            <input type="text" id="fname" name="fname" value=""><br>
            <label for="last name">Last name:</label><br>
            <input type="text" id="lname" name="lname" value="">
            <input type="submit" value="Submit">
        </form> 
        </body>  
        </html>
        ```

        In the above we need to add the 'form' role to the overall container for the form. Labels provide a value which can be read out and assist screen readers. 

        For buttons and form input elements with the 'submit' type, the 'value' field is used to provide the label value.

    - Add a new search field to your form with a hidden label
        
         You can find some examples [here](https://www.w3.org/WAI/tutorials/forms/labels/).

    - Go through the rest of your website using the accessiibility tools and see where there are any accessibility content gaps. Using the resources already shared attempt to fix those issues.
    
4. Add more content to your webpage 

    In this section you can play around with different elements and see how to make them more accessibility friendly. Some examples of what you can:
    - Add a list of URLS to your webpage to make a navigation menu
    - Divide your content into multiple sections
    - Add a dialog/alert and ensure the content is picked up when it opens
    - Add multiple related images and make them into a group which only gets picked up once by screen readers. You can use the 'img' role for this.


## Resources

- [Public Sector Accessibility Requirements](https://www.gov.uk/guidance/accessibility-requirements-for-public-sector-websites-and-apps)

- [WAI Aria Recommendation](https://www.w3.org/TR/wai-aria-1.1/)

- [Aria Roles, States and Properties](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/ARIA_Techniques#landmark_roles)

- [W3 Schools Accessibility Documentation](https://www.w3schools.com/html/html_accessibility.asp)


<div style="width: 100%">
<a href='html_hyperlinks.md'><-- Previous Section: HTML Hyperlinks</a>
<div align="right"><a href='accessibility_tools_tips.md'>Next Section: Accessibility Tools --></a></div>
</div>