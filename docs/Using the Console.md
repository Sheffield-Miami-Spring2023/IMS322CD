---
title: IMS322 Documentation - Spring 2023
---

# Using the Console

[Home](index)

The console is found in your browser's developer tools - it is likely one of the tabs at the top of the developer tools panel. To log something to the console, all you need is the `console.log()` function.

The console has many uses - notably, as a means to check values, troubleshoot, and investigate errors. For example, you can put a `console.log()` line at various points throughout your code to see how far it runs before encountering an error. FYI, when an error is logged to the console, it will usually include a line number to help you identify the source of the error (e.g. something like ".../script.js:18" at the end of the error message indicates a problem on line 18).  

Some online code editors, like CodePen and Replit, have their own built-in consoles. These will generally be much cleaner and easier to work with when working within these environments; however, any messagesthey post will also appear in the browser's console.  
- In CodePen, there is a console button in the lower-left corner of the editor window - you will need to open the embedded example in a new editor in order to see this (by clicking "Edit on CodePen").
- In Replit, there is a wrench icon in the upper-right corner of the preview window that toggles the developer tools.

Try changing the `console.log()` message in the example below to see the updated output logged to the console - **remember, you must have the console open to see the results.**  
<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="MWGWQaE" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/MWGWQaE">
  IMS322-Using-the-Console</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

See if you can fix the problem in the next example by investigating the error reported by the console.
<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="zYJORdV" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/zYJORdV">
  IMS322-Console-Error</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>