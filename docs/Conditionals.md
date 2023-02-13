---
title: IMS322 Documentation - Spring 2023
---

# Conditionals

[Home](index)

Start by reading the section "Conditional Execution" from [Chapter 2 of Eloquent JavaScript](https://eloquentjavascript.net/02_program_structure.html).
<br><br>
## If Statements
If statements provide a way to evaluate data and make different decisions in your code based on the value of the data. The structure of a conditional is fairly straightforward:
```
if (condition to be evaluated) {  
  //  block of code to be executed if the condition is true  
}  
else { 
  //  block of code to be executed if the condition is false 
}
```

<p class="codepen" data-height="400" data-default-tab="js,result" data-slug-hash="YzLjxge" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/YzLjxge">
  IMS322-If-Statements</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<br><br>
## Comparison and Logical Operators
The comparison operators commonly used in conditionals are:
- `===` : equal to (notice the use of 3 equals signs)
- `!=` : not equal to (a ! can be used in front of most operators to mean "not")
- `>` : greater than
- `<` : less than

You can also use the following logical operators to evaluate multiple conditions at the same time:
- `&&` : "and" which will only evaluate as `true` if all conditions are met
- `||` : "or" which will evaluate as `true` if any conditions are met
<p class="codepen" data-height="400" data-default-tab="js,result" data-slug-hash="XWqoxjQ" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/XWqoxjQ">
  IMS322-Logical-Operators</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>