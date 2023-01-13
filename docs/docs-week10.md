---
title: IMS322 A&B Documentation - Fall 2022
---

[Back to schedule](index.md)  

# Week 10 - Introduction to p5 - 10/24-10/26

## What is p5?
From the <a href="https://p5js.org" target="_blank">p5 home page</a>:

*"p5.js is a JavaScript library for creative coding, with a focus on making coding accessible and inclusive for artists, designers, educators, beginners, and anyone else! p5.js is free and open-source because we believe software, and the tools to learn it, should be accessible to everyone."*

In short, p5 simplifies JavaScript drawing and animation. Artists and interaction designers use p5 for all kinds of projects. You can see a collection of example p5 projects in the <a href="https://showcase.p5js.org/#/2021-All" target="_blank">2021 Showcase.</a>  

It is important to remember that p5 IS STILL JavaScript, meaning that everything else that you've learned so far in JavaScript still applies. P5 is just a library of helpful drawing, animation, and other multimedia functionaility IN ADDITION to everything that vanilla JavaScript can do. You can also use p5 within a plain HTML, CSS, and JS project.

## Including the p5 library
Like external fonts and icons, your project needs access to the p5 library resources. The recommended way to include p5 in your project is to <a href="https://p5js.org/download/" target="_blank">download the p5.min.js file</a> and upload it to your Repl. Then, you'll need to add a script tag in your HTML head BEFORE your main script.js tag that points to this file:  
`<script src="p5.min.js"></script>`  
This is the method that will be automatically applied in any provided Repl assignment templates. A general p5 template that can be forked will also be posted to your Replit team.

## The canvas
In p5, we'll be drawing shapes and images to a canvas. This canvas uses a familiar <a href="https://en.wikipedia.org/wiki/Cartesian_coordinate_system" target="_blank">Cartesian coordinate sytem</a> where positions are specificed using a pair of numerical coordinates (x, y). However, in p5, the origin "0, 0" is the top left corner of the canvas, rather than the center. In the example below, you can move your cursor around inside of the canvas area to see the coordinates that correspond to its position.

<p class="codepen" data-height="540" data-theme-id="dark" data-default-tab="result" data-editable="true" data-slug-hash="xxjowgB" data-editable="true" data-user="ersheff" style="height: 540px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/xxjowgB">
  Week10-1-Canvas</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

## The setup() and draw() functions
Every p5 sketch needs at least a setup() and draw() function. These functions have special meaning in p5:
- The setup() function runs once on load. It is intended to initialize settings before the draw() function runs.
- The draw() function runs continuously over and over, at a rate of 60fps by default.

Your setup() function should always include at least `createCanvas(w, h)`, where w is the width and h the height (in pixels) of your drawing canvas. "400, 400" tends to be the default size used most often in examples, but you can make this larger in either dimension if you would like.  

Your draw() function should almost always include a `background(x)` at the very beginning of the function where "x" is a desired background color (e.g. 0 for black, or an RGB value). This also serves to copmletely wipe the canvas clean at the beginning of every frame.

<p class="codepen" data-height="540" data-default-tab="js,result" data-slug-hash="JjZPJae" data-editable="true" data-user="ersheff" style="height: 540px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/JjZPJae">
  Week10-2-BG</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

## Basic drawing and animating
Drawing basic shapes, like circles and squares, is pretty straightforward. Each shape type has its own method that expects arguments to specify the position and dimensions (you should expect to use the <a href="https://p5js.org/reference/" target="_blank">p5 reference page</a> regularly to find these methods). The fill color is white by default, but you can change that will the `fill()` method.  

Notice the order of operations in the example below - the circle is blue because `fill("blue")` is called before it is drawn, but then `fill("green")` is called before the square to change its fill color to green. The draw() function will execute from top to bottom for every frame (which, remember, is 60 times per second by default).

<p class="codepen" data-height="540" data-default-tab="js,result" data-slug-hash="gOKYRZa" data-editable="true" data-user="ersheff" style="height: 540px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/gOKYRZa">
  Week10-3-</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

Understanding this periodic frame drawing is probably one of the more challenging aspects to master when getting started with p5 animation and interaction design. Since the frame is completely redrawn from scratch 60 times per second, you will need to consider how changing values can be stored and used. For example, look at how the "d" variable (short for diameter) is implemented below to change the size of the expanding circle.

<p class="codepen" data-height="540" data-default-tab="js,result" data-slug-hash="PoaYjMz" data-editable="true" data-user="ersheff" style="height: 540px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/PoaYjMz">
  Week10-4-Animating</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

## Other special and useful variables and functions
- <a href="https://p5js.org/reference/#/p5/width" target="_blank">width</a> - system variable that stores the width of the drawing canvas, this value is set by the first parameter of the createCanvas() function
- <a href="https://p5js.org/reference/#/p5/mouseX" target="_blank">height</a> - system variable that stores the height of the drawing canvas, this value is set by the second parameter of the createCanvas() function
- <a href="" target="_blank">mouseX</a> - always contains the current horizontal position of the mouse, relative to (0, 0) of the canvas
- <a href="https://p5js.org/reference/#/p5/mouseY" target="_blank">mouseY</a> - always contains the current vertical position of the mouse, relative to (0, 0) of the canvas
- <a href="https://p5js.org/reference/#/p5/mousePressed" target="_blank">mousePressed()</a> - a function that runs whenever the mouse is pressed, can be used to help create mouse-based interactions
- console.log() - works just like console.log() in vanilla JavaScript
- Many more documented in the <a href="https://p5js.org/reference/" target="_blank">p5 Reference</a>