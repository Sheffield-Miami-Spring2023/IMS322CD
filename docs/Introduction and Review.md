---
title: IMS322 Documentation - Spring 2023
---

# Introduction and Review

[Back to schedule](index.md)
<br><br>
## Using an Online Code Editor (Replit)
This semester, we will be using an online code editor called [Replit](https://replit.com) for all coding coursework. Replit is where you will accept and submit all coding assignments and do in-class group exercises in a shared editor. This greatly simplifies several aspects of developing HTML, CSS, and JavaScript, including setup, previewing, troubleshooting, submitting, and collaborating.
<br><br>
## Using The Embedded Examples
Another online code editor, [CodePen](https://codepen.io/), was used to develop the embedded examples throughout this documentation. You should be able to edit the embedded CodePen examples directly within these pages and see the live preview update as you change the code. If you would like to reuse any of the CodePen example code elsewhere, simply copy-paste the content into your own Repl. Anything in the CodePen HTML should be put inside the `<body>` when used elsewhere.
<br><br>
## Review HTML
As you might recall, HTML stands for "HyperText Markup Language" and is where the **content** of a web page is written.

### Basic Elements (Tags)
HTML is organized using tags to partition content, put elements in a heirarchy and, in some cases, apply default styling.  
<p class="codepen" data-height="400" data-default-tab="html,result" data-slug-hash="JjLxzRz" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/JjLxzRz">
  IMS322-HTML-Tags</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
If you would like to know more about the many different HTML tags or need to find a particular one, see this [MDN Web Docs HTML elements reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Element).
<br><br>
## Review CSS
Cascading Style Sheets, or CSS, are where you describe the styling or presentation of your HTML content. This is usually done in an external stylesheet e.g. a style.css file. Don't forget that you need to reference this file in `<link>` tags in the `<head>` of your HTML document (this is done for you in Replit templates and assignments used for class).

### CSS selectors
In order to apply styling from your CSS file, you need to indicate which elements you want to work with using selectors. The three basic selectors are **element**, **class**, and **id**. For consistency, you should try to use class as much as possible for all of your styling in coursework.
<p class="codepen" data-height="400" data-default-tab="html,result" data-slug-hash="GRxeRgg" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/GRxeRgg">
  IMS322-CSS-Selectors</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

### Common CSS properties
There are far too many CSS properties to demonstrate or memorize them all. Make sure you have a good grasp on some of the basic ones like `background-color`, `color`, `padding`, `border`, etc, and use this [MDN Web Docs CSS reference](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference) if you need to find others.
<p class="codepen" data-height="400" data-default-tab="html,result" data-slug-hash="WNzmNwj" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/WNzmNwj">
  IMS322-CSS-Properties</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

### Box model
The [CSS Box Model](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Box_Model/Introduction_to_the_CSS_box_model) describes how content, padding, borders, and margin all relate to each other.
<p class="codepen" data-height="400" data-default-tab="html,result" data-slug-hash="vYRPYXY" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/vYRPYXY">
  IMS322-CSS-Box-Model</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>