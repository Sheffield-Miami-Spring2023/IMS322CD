---
title: IMS322 A&B Documentation - Fall 2022
---

[Back to schedule](index.md)  

# Week 1 - Introduction and Review - 8/22-8/24

## Using an online code editor (Replit and CodePen)
This semester, we will be using two online code editors for all coursework - Replit and CodePen. These online editors greatly simplify several aspects of writing HTML, CSS, and JavaScript, including setup, previewing, sharing, and collaborating. They aren't always the best option for serious development work, but are well-suited for learning, experimenting, and prototyping.  

[Replit](https://replit.com) is where you will accept and submit all assignments and do in-class group exercises using a shared editor. Once you've created an account and joined the course team, you will be able to see and accept upcoming assignments. Direct links to will also be available in Canvas. Week 1's assignment will be an introduction to this process.  

[CodePen](https://codepen.io) "pens" can be embedded in a web page as an HTML/CSS/JavaScript editor with a preview panel. Examples in the weekly readings for this class will use CodePen since the embedded pens can be edited with live updates right on the page. FYI, the HTML editor in CodePen only focusses on the content that goes in the <body> tags, so you won't see the content that goes in the <head> tags that you might usually expect.  

*If you are using Safari on a Mac, you will need to disable the <a href="https://support.apple.com/guide/safari/prevent-cross-site-tracking-sfri40732/mac" target="_blank">"Prevent cross-site tracking"</a> option in preferences to enable live updates when editing embedded CodePen examples.*  

You are *required* to have a Replit account for this class. A CodePen account is optional but recommended since it will allow you to "fork" example code into a new "pen" in your account without needing to copy-paste.  

Both Replit and CodePen allow users to login using a GitHub account. You can create a GitHub account if you want to simplify that process and think you might use GitHub in the future. Otherwise, signing up for Replit and/or CodePen using your miamioh email account is fine.

-----


## Review HTML
As you might recall from IMS222, HTML stands for "HyperText Markup Language" and is where the CONTENT of a web page is written.


### Basic elements (tags)
HTML is organized using tags to partition content, put elements in a heirarchy and, in some cases, apply default styling.  

<p class="codepen" data-height="400" data-theme-id="dark" data-default-tab="html,result" data-slug-hash="JjLxzRz" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/JjLxzRz">
  Week1-1-HTML-Tags</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>


### Semantic HTML
Whenever possible, it is good practice to use HTML tags that reflect their content. For example, the <header> denotes content that is usually placed at the top of the page. This is called <a href="https://www.youtube.com/watch?v=HJ0-fUJ-2F0&t=165s" target="blank">semantic HTML."</a>

While a website can be built entirely using the generic <div> tag, semantic HTML helps not only to better organize and identify content, but also improves accessibility by providing context for screen readers. There are many other ways to improve accessibility that will not necessarily be covered in this class - however, incorporating semantic HTML is a good first step.  

In the example below, you can see that semantic HTML tags don't always affect the visual styling of the content. Nevertheless, they provide meaning both for the developer writing HTML and for screen readers that help visually-impaired visitors navigate your site.

<p class="codepen" data-height="400" data-theme-id="dark" data-default-tab="html,result" data-slug-hash="qBogvRG" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/qBogvRG">
  Week1-1-HTML-Tags</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

If you would like to familiarize yourself with the full collection of HTML tags, check out <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element" target="_blank">this MDN Web Docs reference</a>. You don't need to know them all, but the reference can also be used to see if any elements you've used in the past <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element#obsolete_and_deprecated_elements" target="_blank">have been deprecated</a>. For now, the tags shown in the embedded examples above will go a long way.

-----


## Review CSS
Cascading Style Sheets are where you describe the styling or presentation of your HTML content. While CSS can be written directly in your HTML document as either an <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/style" target="_blank">attribute</a> or inside <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/style" target="_blank">&lt;style&gt; tags</a>, almost all of the CSS that you write for this class should be in an external stylesheet e.g. a style.css file. Don't forget that you need to <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/link" target="_blank">link your external document</a> in the <head> of your HTML document (this is done for you in Replit and CodePen examples).


### CSS selectors
In order to apply styling from your CSS file, you need to indicate which elements you want to work with using selectors. The three basic selectors are type (element), class, and id.

<p class="codepen" data-height="400" data-theme-id="dark" data-default-tab="html,result" data-slug-hash="GRxeRgg" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/GRxeRgg">
  Week1-3-CSS-Selectors</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

There are many other ways to select elements in CSS with varying levels of specificty, but you should be able to do everything that you need in this class using type, class, and id selectors.


### Common CSS properties
There are way too many CSS properties to demonstrate or memorize them all. Make sure you have a good grasp on some of these basic ones, and keep <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/Reference" target="_blank">this reference</a> handy if you need to look up others.

<p class="codepen" data-height="400" data-theme-id="dark" data-default-tab="html,result" data-slug-hash="WNzmNwj" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/WNzmNwj">
  Week1-4-CSS-Properties</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>


### Box model
The <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Box_Model/Introduction_to_the_CSS_box_model" target="_blank">CSS Box Model</a> describes how content, padding, margin, and borders interact. Padding is inside the border, while margin is on the outside.

<p class="codepen" data-height="400" data-theme-id="dark" data-default-tab="html,result" data-slug-hash="vYRPYXY" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/vYRPYXY">
  Week1-5-CSS-Box-Model</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>