---
title: IMS322 A&B Documentation - Fall 2022
---

[Back to schedule](index.md)  

# Week 5 - Handling Inputs 1 - 9/19-9/21

## Imperative controls (buttons)

The buttons in the example below don't actually do anything, they are simply provided to demonstrate some different ways that buttons can be created and styled.

<p class="codepen" data-height="400" data-theme-id="dark" data-default-tab="html,result" data-slug-hash="VwxjXvX" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/VwxjXvX">
  Week5-1-Buttons</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>


## Functions
Functions are a fundamental part of JavaScript. They can be used to reduce repetition and create structure and organization. You will be writing functions to determine what happens in response to a user input, whether a button click or dropdown select menu.  

There are multiple ways to define functions, but we will focus on using *declaration* notation. With this method, the word *function* is a special keyword that indicates the start of a function declaration. Then, like with variables, you provide a name for the function, followed by parentheses. If your function is reliant on some incoming data, your function declaration should include a variable in the parentheses, which can then be used inside of the function itself. Finally, your actual function code is written inside curly brackets.   

<p class="codepen" data-height="600" data-theme-id="dark" data-default-tab="js" data-slug-hash="mdLExwa" data-editable="true" data-user="ersheff" style="height: 600px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/mdLExwa">
  Week5-2-Functions</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>


## Event listeners
Events are fired in response to an action or change. This can include:
- clicking a button
- selecting an item from a dropdown menu
- entering text into a text field
- resizing a window
- and many more!

In JavaScript, we use event handlers to determine a) what kind of event we are listening for and b) what we want to happen in response to that event. The simple use of an event handler listening for a click is:  
`element.addEventListener("click", functionName)`   
where the element will usually be a variable name.  

To get an element (e.g. a button) and assign it to a variable, use:  
`let myElement = document.getElementById("id-of-element")`

<p class="codepen" data-height="400" data-theme-id="dark" data-default-tab="js,result" data-slug-hash="vYjKRdQ" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/vYjKRdQ">
  Week5-3-EventListeners</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>