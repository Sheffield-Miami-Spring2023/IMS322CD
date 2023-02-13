---
title: IMS322 A&B Documentation - Fall 2022
---

[Back to schedule](index.md)

# Introduction to JavaScript - 9/12-9/14

Read the following sections from [Chapter 1 of Eloquent JavaScript](https://eloquentjavascript.net/01_values.html):
- Values
- Numbers
- Arithmetic
- Strings  

And the following from <a href="https://eloquentjavascript.net/02_program_structure.html" target="_blank">Chapter 2</a>:
- Expressions and Statements
- Bindings
- Binding Names

## The JavaScript console
To log something to the console, all you need is the `console.log()` function. Anything inside of the parentheses will be displayed in the console.    

The console is found in your browser's developer tools. The location for this is different in each browser, but one way to open the developer tools is by right-clicking on a site and choosing "Inspect" - the console should be one of the tabs at the top of the developer tools panel.  

Some online development environments, like CodePen and Replit, have their own built-in console:
- In CodePen, there is a console button in the lower-left corner of the editor window - you will need to open the embedded example in a new editor in order to see this (by clicking "Edit/Fork on CodePen").
- In Replit, there is a wrench icon in the upper-right corner of the preview window that toggles the developer tools.
The output of these Replit/CodePen consoles will also be mirrored in the browser console.  

Try changing the `console.log()` message in the example below to see the updated output logged to the console - **remember, you must have the console open to see the results.**  

<p class="codepen" data-height="200" data-theme-id="dark" data-default-tab="js" data-slug-hash="MWGWQaE" data-editable="true" data-user="ersheff" style="height: 200px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/MWGWQaE">
  Week4-1-JS-Console</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>


## Values, types, and operators
JavaScript is a "weakly typed" language, which means that you do not specify what kind (or type) of data you are working with. Instead, types are implied or inferred based upon the content. The most basic data types are:
- Numbers - Just what it sounds like, any value with or without a decimal point e.g. 10, 5.872, 1,000,000, etc.
- Strings - A representation of text, generally written with quotes (single, double, or backticks). This obviously involves mostly words and sentences, but even a number is converted to a string if it has quotes around it e.g. "8".
- Booleans - True or false, yes or no, on or off. You can literally set a boolean using the true or false keyword, but most often you will encounter booleans as the result of some other operation (more on that later).  

You can dive right into manipulating these values using common arithmetic operators - +, -, *, and /. However, when working with strings, the + operator is for "string concatenation" - basically, just gluing the strings together, as you'll see in the example below.  

<p class="codepen" data-height="200" data-theme-id="dark" data-default-tab="js" data-slug-hash="mdLJgRq" data-editable="true" data-user="ersheff" style="height: 200px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/mdLJgRq">
  Week4-2-JS-Values</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>


## Variables
Being able to create, organize, and manipulate data is fundamental to any programming language. Often, you will find yourself in situations where some data either needs to be reused frequently or change in accordance with user input. This is where variables come into play. Essentially, any piece of data can be assigned to a variable, and then the variable can be inserted into the operations that you would like to perform with that data.  

Variables are declared in JavaScript with the keyword "let".

<p class="codepen" data-height="400" data-theme-id="dark" data-default-tab="js" data-slug-hash="LYmYdoL" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/LYmYdoL">
  Week4-3-Variables</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>


## JavaScript conventions e.g. indentation, brackets, camelCase, etc.
JavaScript has some slightly different style conventions than HTML and CSS:
- Comments
  - Single-line comments are created with a double-slash //
  - Multi-line comments are created with opening and closing slash-asterisk pairs, much like in CSS. /* */
- camelCase
  - Use camelCase when naming things in JavaScript. Start with a lowercase letter, then capitalize the first letter of each additional word in a multi-word name.
  - It will be very common to see a combination of kebab-case (when referrfing to HTML elements) and camelCase in your JavaScript code.
- Indentation
  - Like CSS, anything inside of curly brackets should be indented one level from its parent block.
- Semicolons
  - End each statement in JavaScript with a semicolon.
  - Your code will often still work if you omit semicolons, but getting into the habit of using them will prevent problems with edge cases in the future.

<p class="codepen" data-height="400" data-theme-id="dark" data-default-tab="js" data-slug-hash="BaxaYao" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/BaxaYao">
  Week4-4-JS-Conventions</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>