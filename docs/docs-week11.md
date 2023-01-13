---
title: IMS322 A&B Documentation - Fall 2022
---

[Back to schedule](index.md)  

# Week 11 - More with p5 - 10/31-11/2

## Objects
Objects are another type of data in JavaScript. Like arrays, they are meant to store multiple related values. However, instead of using index numbers, data in objects is stored in "key: value" pairs. Dot or bracket notation can be used to reference individual values:  

`let myObject = {`  
&nbsp;&nbsp;`key: value`  
`}`  

`myObject.key` or `myObject[key]` (returns value)  

One advantage of objects over arrays is that the values can be given contextual meaning - it is much easier and organizationally relevant to refer to a value by a descriptive key rather than an arbitrary index number. An analogy that is often used to describe the usefulness of objects is that of a car - if "car" if the object, then properties like model, year, and color can be stored as values:  

`let myCar = {`  
&nbsp;&nbsp;`make: "Toyota",`  
&nbsp;&nbsp;`model: "Yaris",`  
&nbsp;&nbsp;`year: 2010,`  
&nbsp;&nbsp;`color: "silver"`  
`}`  

In the first example below, you can see how an object might be used to store and recall the values associated with a specific circle in p5.
 
<p class="codepen" data-height="540" data-theme-id="dark" data-default-tab="js,result" data-slug-hash="abKvYZO" data-editable="true" data-user="ersheff" style="height: 540px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/abKvYZO">
  Week11-1-Objects</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

Remember that arrays can store just about anything, not just numbers and strings. If we store objects in an array, then we can create a running "memory" of objects. For example, the sketch below creates a new rising circle at each click location. Having a way to redraw all of the circles "in memory" with every frame is one way to keep track of the changing locations of a collection of shapes, even when the entire frame is erased 60 times per second.

<p class="codepen" data-height="540" data-theme-id="dark" data-default-tab="js,result" data-slug-hash="wvXKmWj" data-editable="true" data-user="ersheff" style="height: 540px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/wvXKmWj">
  Week11-2-Objects2</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

## Managing Flow with If Statements
As you work in p5, you'll likely get the hang of creating static or single-state sketches relatively quickly - there are only so many different ways to draw and animate circles, squares, triangles, and jpegs! In order to design something with some progression or narrative flow, you'll need a way to a) keep track of the current state of the sketch, and b) organize the code that describes different states into discrete sections.  

The example below demonstrates how to accomplish this with if statements. There are no new data types or methods in this sketch - rather, it's an illustration of how to apply basic techniques to accomplish this goal. An array stores the names of different "states" that our sketch will step through - in this case, different times of day. The if and else if statements each hold the properties associated with these different scenes and then set values based on which condition is met. Finally, a simple incrementer in the mousePressed() function steps through the different states in the array each time the mouse is pressed.

<p class="codepen" data-height="540" data-theme-id="dark" data-default-tab="js,result" data-slug-hash="BaVorYP" data-editable="true" data-user="ersheff" style="height: 540px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/BaVorYP">
  Week11-3-Flow</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

## Working with Media
The following example shows how to incorporate images, sound, and webcam video into a p5 sketch. Due to limitations with CodePen and embedding of p5, a link to a Repl is provided. Note: audio does not work in Chrome (use Safari or Firefox if working with audio).  

 <a href="https://replit.com/@sheffie/p5-Media#script.js" target="_blank">p5 Media Example (on Replit)</a>