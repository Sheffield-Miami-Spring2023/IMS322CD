---
title: IMS322 Documentation - Spring 2023
---

# Variables and Values

[Home](index)

Start by reading the following sections from [Chapter 1 of Eloquent JavaScript](https://eloquentjavascript.net/01_values.html):
- Values
- Numbers
- Arithmetic
- Strings
<br><br>
## Values, Types, and Operators
JavaScript is a "weakly typed" language, which means that you do not specify what kind (or type) of data you are working with. The most basic data types in JavaScript are:
- Numbers: Just what it sounds like, any value with or without a decimal point e.g. 10, 5.872, 1,000,000, etc.
- Strings: A representation of text, generally written with quotes (single, double, or backticks). This obviously involves mostly words and sentences, but even a number is converted to a string if it has quotes around it e.g. "8".
- Booleans: Simple true or false, yes or no, on or off. You can literally set a variable to a boolean using the `true` or `false` keyword, but often you will encounter booleans as the result of a conditional "if" statement (more on that later).  
You manipulate these values using common arithmetic operators - +, -, \*, and /. However, note that when working with strings, the + operator is for "concatenation" - basically, just gluing the strings together, as you'll see in the example below.
<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="mdLJgRq" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/mdLJgRq">
  IMS322-Values-Types-Operators</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<br><br>
## Variables
Being able to create, organize, and manipulate data is fundamental to any programming language. Often, you will find yourself in situations where some data either needs to be reused frequently or changed in accordance with user input. This is where variables come into play. 

You've already seen how a variable can act as a sort of shorthand in order to reference the same element without needing to write out the entire `document.getElementById("id-of-element)"` bit every time.

For example, this will assign the variable `playButton` to an element...
```
let playButton = document.getElementById("play-button)";
```
...which makes additional operations using the element easier later on.
```
playButton.addEventListener("click", function);
playButton.style.backgroundColor = "blue";
```

Rather than calling it "shorthand", it would be more accurate to say that the variable *represents* the data that it is assigned to, whether that be a number, string, HTML element, or something else. Once a piece of data is assigned to a variable, then the variable can be inserted into the operations that you would like to perform with that data.
<p class="codepen" data-height="400" data-default-tab="js,result" data-slug-hash="LYmYdoL" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/LYmYdoL">
  IMS322-Variables</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>