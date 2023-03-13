---
title: IMS322 Documentation - Spring 2023
---

# Introduction to p5

[Home](index)
<br><br>
## What is p5?
From the [p5 home page](https://p5js.org):

*"p5.js is a JavaScript library for creative coding, with a focus on making coding accessible and inclusive for artists, designers, educators, beginners, and anyone else! p5.js is free and open-source because we believe software, and the tools to learn it, should be accessible to everyone."*

In short, p5 simplifies drawing, animation, and interactivity in JavaScript. It does this primarily by providing predefined functions and variables that handle some of the more complex logic and calculations behind the scenes. For example, here is the JavaScript required to draw a circle:
<p class="codepen" data-height="520" data-default-tab="js,result" data-slug-hash="wvEyQXb" data-editable="true" data-user="ersheff" style="height: 520px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/wvEyQXb">
  IMS322-Vanilla-Circle</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
And here is essentially the same drawing using p5:
<p class="codepen" data-height="520" data-default-tab="js,result" data-slug-hash="qBMxQMp" data-editable="true" data-user="ersheff" style="height: 520px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/qBMxQMp">
  IMS322-p5-Circle</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

Artists and interaction designers use p5 for all kinds of projects. You can see a collection of example p5 projects in the [2022 Showcase](https://showcase.p5js.org/#/2022-All).

It is important to remember that p5 *is still just JavaScript*, meaning that everything else that you've learned so far in JavaScript, like arithmetic operations and if statements, still applies. Also, p5 functions can sit right alongside standard JavaScript variables, event listeners, and functions in the same project.
<br><br>
## Including the p5 library
Like external fonts and icons, your project needs access to the p5 library resources. The recommended way to include p5 in your project is to [download the p5.min.js file](https://p5js.org/download/) and upload it to your Repl. Then, you'll need to add a script tag in your HTML head BEFORE your main script.js tag that points to this file:
```
<script src="p5.min.js"></script>
```
This is the method that will be automatically applied in any provided Repl assignment templates. A general p5 Replit template that can be forked will also be posted to Canvas.
<br><br>
## The setup() and draw() functions
Every p5 sketch needs at least a `setup()` and `draw()` function. These functions have special meaning in p5:
- The `setup()` function runs once on load. It is intended to initialize settings before the `draw()` function runs.
- The `draw()` function runs continuously over and over, at a rate of 60fps by default.

Your `setup()` function should always include at least `createCanvas(w, h)`, where w is the width and h the height (in pixels) of your drawing canvas. "400, 400" tends to be the default size used most often in examples, but you can make this smaller or larger in either dimension if you would like.  

Your `draw()` function should always include `background(x)` at the very beginning of the function where "x" is a desired background color e.g. 0 for black, or an RGB value like (255, 0, 0). This background also serves to copmletely wipe the canvas clean at the beginning of every frame, kind of like those magnetic wipe-and-erase boards for kids.

Try changing the width and height values of the canvas and the color of the background in the example below.
<p class="codepen" data-height="520" data-default-tab="js,result" data-slug-hash="JjZPJae" data-editable="true" data-user="ersheff" style="height: 520px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/JjZPJae">
  IMS322-Setup-Draw</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<br><br>
## The Canvas
In p5, we'll be drawing shapes and images to a canvas. This canvas uses the familiar [Cartesian coordinate sytem](https://en.wikipedia.org/wiki/Cartesian_coordinate_system) where positions are specificed using a pair of numerical coordinates - x and y. However, in p5, the origin point of "0, 0" is the top left corner of the canvas, rather than the center. In the example below, you can move your cursor around inside of the canvas area to see the coordinates that correspond to its position.
<p class="codepen" data-height="520" data-default-tab="js,result" data-slug-hash="xxjowgB" data-editable="true" data-user="ersheff" style="height: 520px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/xxjowgB">
  IMS322-p5-Canvas</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<br><br>
## Basic Drawing
Drawing basic shapes, like circles and squares, is pretty straightforward. Each shape type has its own method that expects specific arguments to specify the position and dimensions. For example, [circles](https://p5js.org/reference/#/p5/circle) need an x position, y position, and diameter:
```
circle(x, y, d);
```
...while [lines](https://p5js.org/reference/#/p5/line) require a starting X, starting Y, ending X, and ending Y:
```
line(x1, y1, x2, y2);
```

You should expect to use the [p5 reference page](https://p5js.org/reference/) regularly to research and revisit these different drawing methods and predefined variables/values. Here are a few other important methods and variables to get you started:
```
mouseX; // a predefined variable that returns the x position of mouse relative to canvas

mouseY; // a predefined variable that returns the y position of mouse relative to canvas

width; // a predefined variable that returns the width of the canvas

height; // a predefined variable that returns the height of the canvas

text("string", x, y); // a method that prints a string of text on the canvas at an x, y location

fill(x); // a methid that sets the fill color for all following shapes and text, a single value will automatically be interpreted as grayscale (0 is black, 255 is white) 

fill(r, g, b); // fill color can also be specified with RGB, HEX, or CSS values (like "blue")
```

Notice the order of operations in the example below - the circle is blue because `fill("blue")` is called before it is drawn, but then `fill("green")` is called just before the square to change its fill color to green. Even though the examples that we've looked at so far have all appeared to be still, the `draw()` function will execute in a loop from top to bottom for every frame. This is partially why `background()` is the first thing in the `draw()` function - without it, you would see remnants of all the previous frames, which would cause problems once you start to move or animate shapes and graphics.
<p class="codepen" data-height="520" data-default-tab="js,result" data-slug-hash="zYJRePg" data-editable="true" data-user="ersheff" style="height: 520px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/zYJRePg">
  IMS322-p5-Basic-Drawing</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<br><br>
## Basic Animating
Understanding this periodic frame drawing is probably one of the more challenging aspects to master when getting started with p5 animation and interaction design. Since the frame is completely redrawn from scratch 60 times per second, you will need to consider how changing values can be stored and used and how they will be changed over time. For example, look at how the "circleX" variable is implemented below to change the position of the circle (you may need to refresh the page to restart the animation if you no longer see the circle). It starts at 0 and is incremented by 1 every frame with `circleX++`. Can you change the code to prevent the circle from disappearing off ths side of the screen? (hint: use an if statement)
<p class="codepen" data-height="520" data-default-tab="js,result" data-slug-hash="qBMxgVd" data-editable="true" data-user="ersheff" style="height: 520px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/qBMxgVd">
  IMS322-p5-Basic-Animating</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>