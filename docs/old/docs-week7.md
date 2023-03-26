---
title: IMS322 A&B Documentation - Fall 2022
---

[Back to schedule](index.md)  

# Week 7 - Arrays & Loops - 10/3-10/5

## Arrays

Sometimes, you will need to store values in groups. Perhaps you have a list of mutiple items to display on a page, or are give a dataset with values that must be tallied.  

An array is a type of variable specifically made to store sequences of values. An array is declared just like a single value variable with the keyword `let`. When assigning multiple values to an array, separate them with commas inside square brackets: `let myArray = [12, 34, 56, 78];`. You can also declare an empty array with just brackets: `let emptyArray = [];`. To read out a single value, refer to it by the index number (its location within the array), starting at 0. For example, given myArray above, `myArray[2]` would return 56.

<p class="codepen" data-height="250" data-theme-id="dark" data-default-tab="js" data-slug-hash="BaxmjQQ" data-editable="true" data-user="ersheff" style="height: 220px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/BaxmjQQ">
  Week7-Arrays</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>


### Properties and Methods

We have already been using both properties and methods in previous examples and assignments. For example, `element.innerText` is a property of HTML elements, while `element.addEventListener()` is a method. Essentially, properties are characterstics of an object (e.g. a stored number or string associated with the object, kind of like metadata), while methods are actions that can be performed (e.g. a function that belongs to an object). Notice that both the property and method are refernced using dot notation - appended to the element with a period. Methods add parentheses at the end (which makes sense given that functions are defined using parentheses).  

Arrays have a few useful properties and methods, which you can see demonstrated in the example below.

<p class="codepen" data-height="590" data-theme-id="dark" data-default-tab="js" data-slug-hash="LYmOGbo" data-editable="true" data-user="ersheff" style="height: 440px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/LYmOGbo">
  Week7-2-ArrayProperties</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>


## For loops

A for loop is useful any time you need to run a section of code a certain number of times. For most jobs, you will likely construct your for loop as such:  
`for (let i = 0; i < 5, i++) {`  
&nbsp;&nbsp;`// do this 5 times }`  
`}`

...where `i` is a counter variable that increments each time the code is run until it reaches 5.

<p class="codepen" data-height="200" data-theme-id="dark" data-default-tab="js" data-slug-hash="KKRyVyQ" data-editable="true" data-user="ersheff" style="height: 200px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/KKRyVyQ">
  Untitled</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

For example, if you want to get all of the values out of an array individually, you can log them to the console one at a time. We do this by treating the counter variable `i` as the index for the array.

<p class="codepen" data-height="260" data-theme-id="dark" data-default-tab="js" data-slug-hash="wvjPMye" data-editable="true" data-user="ersheff" style="height: 260px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/wvjPMye">
  Week7-4-ForLoopArray</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

Arrays are an example of something that is an "iterable" - this means that we can iterate over all of the values of an array with the simpler `for..of` loop.

<p class="codepen" data-height="250" data-theme-id="dark" data-default-tab="js" data-slug-hash="GRdOodN" data-editable="true" data-user="ersheff" style="height: 250px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/GRdOodN">
  Week7-5-ForOf</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>