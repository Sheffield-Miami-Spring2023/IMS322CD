---
title: IMS322 Documentation - Spring 2023
---

# Arrays and Objects

[Home](index)

So far, we have only worked with variables in JavaScript that hold a single value - one number, one HTML element, or one string. There are many occasions where you may want to efficiently store two or more related values in a single variable. This is where Arrays and Objects can both  be useful.
<br><br>
## Arrays
An array is a variable specifically made to store sequences of related values. These values can be any  type of data - numbers, strings, and more.

To create an an array, declare a variable with your values separated by commas inside square brackets:
```
let myArray = [12, 34, 56, 78];
```

To read out a single value, refer to it by its location in the array, which is called the index. Locations in an array start at 0. For example, given `myArray` above:
```
myArray[0]
```` 
would return 12, while:
```
myArray[2]
```
would return 56.

Below are a few examples of practical uses for arrays.
<p class="codepen" data-height="520" data-default-tab="js,result" data-slug-hash="QWVrdGJ" data-editable="true" data-user="ersheff" style="height: 520px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/QWVrdGJ">
  IMS322-Arrays</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<br><br>
## Objects
Like arrays, objects are used to store multiple related values. However, instead of using nondescript index numbers, data in objects is stored and referenced using "keys":
```
let myObject = {
	key: value,
	key: value
}
```
The main advantage here is that keys can help provide some context or meaning for your data. For example, consider the parameters needed to draw a red circle in p5. You might store these parameters in single value variables like this:
```
let cX = 50;
let cY = 100;
let cD = 80;
let cCol = "red";
```
The same data can be stored in a single object:
```
let myCircle = {
	x: 50,
	y: 100,
	d: 80,
	col: "red"
}
```
While this is not necessarily more efficient (i.e. you may end up typing a similar amount of characters), it can be very helpful for mentally planning and conceptualizing your code. Each of those paramaters now have an implicit relationship with each other by being stored in the same object.

To retrieve a single value from an object, use dot notation in which the key follows the name of the object:
```
myObject.key;
```
For example, given `myCircle` above:
```
myCircle.col;
```
would return "red".

<p class="codepen" data-height="520" data-default-tab="js,result" data-slug-hash="poOVRYo" data-editable="true" data-user="ersheff" style="height: 520px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/poOVRYo">
  IMS322-Objects</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
