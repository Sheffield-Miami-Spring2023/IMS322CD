---
title: IMS322 A&B Documentation - Fall 2022
---

[Back to schedule](index.md)  

# Week 8 - Conditionals and Comparisons - 10/3-10/5

## If statements
If statements (aka conditionals) are a way to evaluate data and make different decisions in your code based on the value of the data. The structure of a conditional is fairly straightforward:  
`if (condition) {`  
&nbsp;&nbsp;`//  block of code to be executed if the condition is true`  
`}`  
`else {`  
&nbsp;&nbsp;`//  block of code to be executed if the condition is false`  
`}`
<p class="codepen" data-height="660" data-theme-id="dark" data-default-tab="js,result" data-slug-hash="YzLjxge" data-editable="true" data-user="ersheff" style="height: 660px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/YzLjxge">
  Week8-1-Classes</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

## Comparison and logical operators
The comparison operators commonly used in conditionals are:
- `===` : equal to (notice the use of 3 equals signs)
- `!=` : not equal to (a ! can be used in front of most operators to mean "not")
- `>` : greater than
- `<` : less than

You can also use the following logical operators to evaluate multiple conditions at the same time:
- `&&` : and
- `||` : or

<p class="codepen" data-height="420" data-theme-id="dark" data-default-tab="js,result" data-slug-hash="XWqoxjQ" data-editable="true" data-user="ersheff" style="height: 420px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/XWqoxjQ">
  Week8-2-Logical</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

## Data-* attribute
Sometimes, the standard HTML attributes - e.g. value, type, src, etc. - may not be sufficient to organize and modify the content in your project. For example, think back to your profile questionnaire project: what if you wanted to search for profiles that meet certain criteria within that community?  

The data-* attribute provides a way to specify custom HTML attributes that better meet your needs. These attributes are not visible to the user but can be used to evaluate HTML content behind the scenes. Any label can be applied to the data-* attibute by replacing the * with your own criteria, e.g.:
- data-name
- data-age
- data-color

Custom data-* attirbutes can be especially useful when combined with conditionals. You can access these attributes within JavaScript with the format: `element.dataset.*`.

<p class="codepen" data-height="500" data-theme-id="dark" data-default-tab="html,result" data-slug-hash="gOzZBvG" data-editable="true" data-user="ersheff" style="height: 500px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/gOzZBvG">
  Week8-3-Dataset</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>