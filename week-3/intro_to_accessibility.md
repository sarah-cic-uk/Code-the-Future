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

To ensure applications are accessible we need to provide semantic information about components, structures, and expected behaviors, so that assistive technologies can provide relevant information to their users, where this isn't already provided by semantic mark up.

 The Accesible Rich Internet Application (ARIA) specification provides a series of roles and properties that can help with this. It helps defines accessible user interface elements which allow you to describe behaviors and structural information to assistive technologies in document-level markup.

### Aria Roles
This is an attribute you can add to a element to help clarify what the expected behaviour should be, semantic elements have a role already for example ```<p></p>``` has the role paragraph so it doesn't need a role adding to it. 

Most roles should no longer be used as browsers now support semantic HTML element with the same meaning. The roles without HTML equivalents, such as presentation, toolbar and tooltip roles, provide information on the document structure to assistive technologies such as screen readers as equivalent native HTML tags are not available.

There a variety of [aria roles](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles) available but some common ones include:

- **Alert**: Used to alert the user that something has changed on their page - screen readers will start reading the alert when it pops up.

- **Tab, tablist and tabpanel**: used when creating interactive tab groups.  

- **Tooltip**: A contextual text bubble that displays a description for an element that appears on pointer hover or keyboard focus

Example of setting a role, we have an input here that we want to add a tooltip to, we can set the role of a div to tooltip so assistive technologies know that is the usage of this element and give it an id so they know that this is what to use to describe the input

```
<label for="password">Password:</label>
<input aria-describedby="passwordrules" id="password" type="password" />
<div hidden role="tooltip" id="passwordrules">
  <p>
      Password Rules:
  </p>
  <ul>
    <li> Minimum of 8 characters</li>
    <li> Include at least one lowercase letter, one uppercase letter, one number and one special character</li>
    <li>Unique to this website</li>
  </ul>
</div>
```


### Aria States and Properties
[Aria States and Properties](https://www.w3.org/TR/wai-aria-1.0/states_and_properties) support the ARIA roles that exist on a page and can supply extra user interface information that is useful for assistive technologies. Whenever these states or properties change the assistive technology can pickup the update and alert the user that a change has occurred. 

 e.g. 'aria-disabled' is a state saying whether a particular item is interactive.

## Semantics
Structuring your web application in using semantic tags is one of the most important steps in creating an accessible application because they clearly describes elements meaning to both the browser and any assitive technologies being used.

Examples of non-semantic elements: ```<div> and <span>``` - They tell us nothing about its content.

Examples of semantic elements: ```<form>, <table>, and <article>``` - These clearly define its content.

Have a look at all the [semantic elements avaliable](https://www.w3schools.com/html/html5_semantic_elements.asp).


See [this page on HTML Semantics](http://web-accessibility.carnegiemuseums.org/foundations/semantic/) for more information. 

## Good Practice:
<!-- ToDo: discuss some good practices and tidy the below -->

**Aria-label**: can be used on any html element. Screen readers announce the label text when on the element e.g. reads the label instead of the button text. Use it in cases where a text label is not visible on the screen.

**Aria-labelledby**: allows label to be set based on other IDs. Role elements good to do with these e.g. radio group. Can concatenate several labels into one . Can be used on hidden elements. Always takes precedence. If there is visible text labeling the element, use aria-labelledby instead.

**Aria-describedby**: is used to indicate the IDs of the elements that describe the object. Similar to labelledby but gives additional info to help the user. e.g. helper text that isn't always visible
		
**Aria-owns**: When a parent/child relationship is evident on-screen, but it isn’t represented in the DOM, the aria-owns attribute can be used to establish that relationship in the accessibility layer.

Notes:
    Use Semantic HTML5 in Favour of ARIA
    Don’t Alter the Meaning of Semantic Elements with ARIA Roles
    Interactive ARIA Elements must be Accessible by all mediums, including mouse, keyboard and more!
    Over-using aria can be bad too!
    Always remember to update your labels when you change your UI!



## Activity

1. Download the Chrome Accessibility Plugins 

- [Screen Reader](https://chrome.google.com/webstore/detail/screen-reader/kgejglhpjiefppelpmljglcjbhoiplfn)

- [Aria DevTools Chrome Plugin](https://chrome.google.com/webstore/detail/aria-devtools/dneemiigcbbgbdjlcdjjnianlikimpck?hl=en/)

- [axe DevTools - Web Accessibility Testing](https://chrome.google.com/webstore/detail/axe-devtools-web-accessib/lhdoppojpmngadmnindnejefpokejbdd)

    You will have to enable these Plugins from the Extension menu if disabled. You can do this if you go to chrome://extensions/ and hit the toggle icon so that all the necessary plugins are blue.

There is also:

- [Google Dev Tools Lighthouse Accessibility Audit](https://developers.google.com/web/tools/lighthouse#devtools)

2. Open up different webpages and explore with the Dev Tools

    The best way to understand how the tools work is to open up a few websites and try interacting with the pages.

    Try viewing the pages both with the dev tools, and without, so you can get a feel for how content has been structured.

    You can use the **tab** button to cycle through the items shown on a page in the dev tools, use **enter** to select an option or fire a button and **Alt + tab** will let you move backwards. You can see some more examples of in-depth controls [here](https://webaim.org/techniques/keyboard/).

    Some example websites you can open up:
    - https://www.google.co.uk
    - https://www.myemergencydr.com/
    - https://www.internetrix.com.au/
    
3. Add more content to your webpage 

    In this section you can play around with different elements and see how to make them more accessibility friendly. Some examples of what you can:
    - Add a list of URLS to your webpage, maybe you could use a few semantic elements here like ```<nav></nav> and <ul></ul>```
    - Divide your content into multiple sections, using appropriate semantic tags like ```<header></header>, <section></section> and more```
    - See if you can find out how to mark up a photo using ```<figure></figure> and <figcaption></figcaption>```

4. Check your site using the accessibility tools
        
    - Go through the rest of your website using the accessibility tools and see where there are any accessibility issues. Using the resources already shared attempt to fix those issues.

## Resources

- [Public Sector Accessibility Requirements](https://www.gov.uk/guidance/accessibility-requirements-for-public-sector-websites-and-apps)

- [WAI Aria Recommendation](https://www.w3.org/TR/wai-aria-1.1/)

- [Aria Roles, States and Properties](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/ARIA_Techniques#landmark_roles)

- [W3 Schools Accessibility Documentation](https://www.w3schools.com/html/html_accessibility.asp)


<div style="width: 100%">
<a href='html_hyperlinks.md'><-- Previous Section: HTML Hyperlinks</a>
<div align="right"><a href='accessibility_tools_tips.md'>Next Section: Accessibility Tools --></a></div>
</div>



