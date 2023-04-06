# Green Coding

## What is it?

Green coding is a term recently popularized for its environmental intentions and refers to programming code that is written to produce algorithms that have minimal energy consumption.

- Structural considerations - encompass the energy measures related to code blocks (units of code).
- Behavioural considerations - the energy consumption that is related to user scenarios such as sending an email or checking your Twitter feed.

The more visitors a site has the bigger its carbon footprint, and so green coding can have a large impact on heavy footfall websites. Amazon get 9 billion hits a day!

## Ways to implement green coding in HTML

**Reduce your image size!**\
If you show images on your site, make sure the original image is the size you want it shown on the page. Storing a large image and shrinking it using CSS is more intensive and can greatly increase your site size and loading times.

**Lazy load your images!**\
If your page has 10 images on and loads them all when you first visit the page it involves a lot of network calls and a long loading period (remember visitors get impatient after only a few seconds and will leave a site if it loads to slowly!).

Lazy loading only loads the images on the screen at that time. As the user scrolls it will load the next images.

In HTML we can do this using the loading attribute:

```
<img loading="lazy" src=images/catPic.jpg alt="a cat picture" />
```

**Replace you GIFs with MP4!**\
GIFs are not carbon friendly. For example, a 600kb gif can be replaced by a 40kb MP4. An MP4 is streamed so is also useful if the GIF you want is a 20 minute long loop as it only streams what is being watched; if a user leaves after 20 seconds they only pay the carbon cost for those 20 seconds!

To do this we can use the video tag with certain attributes:

```
<video autoplay loop muted playsinline src="images/catWalking.mp4>
```

**Avoid overuse of web fonts!**\
Web fonts from somewhere like Google Fonts (https://fonts.google.com/) allow you to embed fonts in the browser that aren't natively supported. These fonts need to be downloaded by the user to allow them to view the page. Built in CSS fonts don't need to be downloaded and so have no carbon cost.

## Useful info

https://shouldiuseacarousel.com/ \
https://principles.green/

<div style="width: 100%">
<a href='README.md'><-- Previous section:  Session 6 Introduction</a>
<div align="right"><a href='hosting_on_git.md'>Next section: Hosting on Git--></a></div>
</div>
