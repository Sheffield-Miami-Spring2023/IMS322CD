---
title: IMS322 Documentation - Spring 2023
---

# More Functions

[Home](index)
<br><br>
Functions are a fundamental part of JavaScript. They can be used to reduce repetition and create structure and organization.

The word *function* is a reserved keyword that indicates the start of a function definition. Like variables, you provide a name for the function. This name should be descriptive of the "function" of the function.

```
function nameOfMyFunction() {
	// stuff goes here
}
```

While we will mostly write functions to be used in event listeners, you can use them any time to help clarify the organization of your code or reduce repetition.

```
// this uses the function in an event listener
element.addEventListener("click", nameofMyFunction);

// this calls the function immediately
nameOfMyFunction();

// this defines the function
function nameOfMyFunction() {
	// stuff goes here
}
```

If your function is reliant on some incoming data, its definition can include a variable in the parentheses, which can then be used locally inside of the function itself. Then, each time the function is called, a different value can be passed in.

```
passItIn(10);

function passItIn(x) {
	// if x is used here, it will be equal to 10
	// for example, this will log the value 14 to the console
	console.log(x+4);
}
```

This can greatly improve the flexibility and efficiency of your code. Try changing the values that are being passed into the `doubleIt()` and `congrats()` functions below.
<p class="codepen" data-height="400" data-default-tab="js,result" data-slug-hash="mdLExwa" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/mdLExwa">
  IMS322-More-Functions</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

