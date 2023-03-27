---
title: IMS322 Documentation - Spring 2023
---

# Managing States

[Home](index)

One of the more challenging aspects in p5 - or any coding language, library, or environment, for that matter - is managing the state of multiple elements. For example, if there are several shapes in a p5 canvas, how can you keep track and/or change the position of all of them? How can you move them all in different directions at the same time? How can you determine which one  is being hovered over or clicked? Ultimately, this can be accomplished through a combination of arrays and objects.
<br><br>
## Array Methods
Arrays can be manipulated on the fly using array methods. There are several different array methods (you can find a reference list in the left sidebar [here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)), but the ones that will be most useful for us at this time are `array.push()`, `array.pop()`, and `array.splice().`

`array.push()` can be used to add elements to the end of an existing array. This example below also introduces the `mousePressed()` function in p5 which, as its name suggests, runs every time the mouse is pressed.
<p class="codepen" data-height="520" data-default-tab="js,result" data-slug-hash="LYJaYLj" data-editable="true" data-user="ersheff" style="height: 520px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/LYJaYLj">
  IMS322-Array-Push</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

`array.pop()` does the opposite - it removes the last element from an existing array.
<p class="codepen" data-height="520" data-default-tab="js,result" data-slug-hash="LYJaYad" data-editable="true" data-user="ersheff" style="height: 520px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/LYJaYad">
  IMS322-Array-Pop</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

Often, you will need to remove an element from somewhere in the middle of array. In these cases, `array.splice()` is used. The arguments passed to `array.splice()` are the index number of the item that you want to remove followed by the number of items that you are removing (often just 1). For example, `array.splice(3, 1)` will remove the 4th item from the array (the one with an index of 3).
<p class="codepen" data-height="520" data-default-tab="js,result" data-slug-hash="Jjazjqp" data-editable="true" data-user="ersheff" style="height: 520px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/Jjazjqp">
  IMS322-Array-Splice</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<br><br>
## Objects in Arrays
Arrays can hold more then just numbers and strings - they can also hold objects. Remember that objects can store the characteristics, or "properties", of things like shapes in p5:
```
let myCircle = {
	x: 40,
	y: 80,
	d: 20
}
```

By combining array methods with objects, we can keep track of several new shapes. For example, creating a circle with a new position and random size each time the mouse is pressed and then pushing it into an array. It's important to remember in this case that the array does not store the `circle()` p5 function itself, but rather just the *properties* of each circle. The `circle()` function still needs to be called in the `draw()` function.
<p class="codepen" data-height="520" data-default-tab="js,result" data-slug-hash="wvEOBMB" data-editable="true" data-user="ersheff" style="height: 520px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/wvEOBMB">
  IMS322-Objects-In-Arrays</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<br><br>
## Storing and Changing Object Properties
In p5, the canvas is refreshed 60 times per second (framerate of 60fps). The canvas is wiped clean at the beginning of every `draw()` function, and then all of the shapes are redrawn. This means that the object representing each shape might need to store more than just its position and size - it can also store things like color, direction of movement, speed of movement, or anything, really. The specific properties that are stored will be determined by the specific needs of your project.
<p class="codepen" data-height="520" data-default-tab="js,result" data-slug-hash="zYJbxzW" data-editable="true" data-user="ersheff" style="height: 520px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/zYJbxzW">
  IMS322-Storing-Object-Properties</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>