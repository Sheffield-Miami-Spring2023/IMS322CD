---
title: IMS322 Documentation - Spring 2023
---

# JavaScript - Jumping Right In

[Home](index)

JavaScript is the programming language of the web. It adds interactivity and dynamic behaviors to HTML and CSS. With JavaScript, you can accept input from a user and modify page contents in response.

Just like CSS, you must have a reference to your JavaScript file in the `<head>` of your HTML. Assuming a standard file name of "script.js," that reference should look something like this:

```
<script src="script.js" defer></script>
```

The "defer" attribute is important when the `<script>` tag is placed in the `<head>` - it ensures that the JavaScript does not execute until after the rest of the page has finished loading.

There are 3 steps to basic interactivity in JavaScript:
1. Reference an HTML element: What element is the user interacting with, or what element do you want to change in response to an event?
2. Add an event listener to that element: What kind of interactive event are you listening for?
3. Define a function: What do you want to happen when the specified event occurs?
<br><br>
## Referencing an Element
There are multiple ways to reference an HTML element outside of the HTML document itself. In CSS, we generally use class selectors when indicating which elements we want to style. For example, given this `<p>` element:

```
<p class="main-text">Lorem ipsum dolor sit.</p>
```

You would use this CSS to make the text red:

```
.main-text {
	color: red;
}
```

For JavaScript, we will primarily use the id attribute to reference an HTML element. 

HTML:
```
<p class="main-text" id="first-paragraph">Lorem ipsum dolor sit.</p>
```

JavaScript:
```
document.getElementById("first-paragraph");
```

Notice a couple of things about the previous line:
- It starts with `document`, which is the main object that represents your web page. If you want to access any element in an HTML page, you always start with accessing the document object.
- `getElementById` is a method of the document. It does exactly what it says: gets an element from the HTML that has the matching id provided in parantheses. From this, we can also assume that any HTML element that will be used as part of an interaction should be given an id.
- Anything named with multiple words in JavaScript, like `getElementById`, uses the camelCase convention: start lowercase, capialize each successive word, no spaces or hyphens.
- However, things that were named in the HTML first, like the `first-paragraph` id, still use the kebab-case convention.
- In JavaScript, a statement ends with a semi-colon. Modern JavaScript is pretty forgivable about missing semi-colons, but you'll still want to get in the habit of using them.

How can you know for sure that you are referencing the right HTML element? You can check by logging it to the console

```
console.log(document.getElementById("first-paragraph");
```

The console is part of your browser's developer tools. See if you can find it - what do you see there?
<p class="codepen" data-height="400" data-default-tab="html,result" data-slug-hash="vYaPjvj" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/vYaPjvj">
  IMS322-Console-Log</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
Given the example code embedded above, try changing the contents within the parantheses of `console.log();` Here are a few to get you started:
- `console.log("Hello, world!");`
- `console.log(10);`
- `console.log(10+10);
- `console.log("10" + "10");`

Now make some new HTML elements with different id attributes and try referencing them within the parentheses of `console.log();`. Here's one to get you started:

In HTML:
```
<h1 id="my-element">Hello, world!</h1>
```

In JavaScript:
```
console.log(document.getElementById("my-element");
```


## Event Listeners
Events are fired in response to an action or change. This can include:
- clicking a button
- selecting an item from a dropdown menu
- entering text into a text field
- resizing a window
- and many more

In JavaScript, we use event listeners (or handlers) to indicate:
- What type of event are we listening for?
- What we want to happen in response to that event?

For example: an event handler listening for a click is:

```
document.getElementById("id-of-element").addEventListener("click", function);  
```

The first parameter inside of the parantheses after `addEventListener` indicates the type of event we are listening for, in this case a `"click"`. The second paramater is the name of a function that will run in response to the event being fired. We will investigate naming and writing functions in the next section.

### Assigning Elements to Variables
That event listener line is getting pretty long. Wouldn't it be nice if there was some kind of shorthand to accomplish the same thing? That's where variables come in handy.

To assign an element it to a variable, use:

```
let myElement = document.getElementById("id-of-element");
```

The `let` keyword indicates that you are defining a variable. The name of the variable, in this case `myElement`, can be whatever you want, though it should be short, descriptive, and follow the camelCase convention. 

Now, the much shorter variable name can be used in place of the longer element reference, so:

```
document.getElementById("id-of-element").addEventListener("click", function);
```

becomes:
```
myElement.addEventListener("click", function);
```

<p class="codepen" data-height="400" data-default-tab="html,result" data-slug-hash="oNMVVOb" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/oNMVVOb">
  IMS322-Event-Listeners</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<br><br>
## Writing Functions
Similar to variables, functions can be considered a type of shorthand for a longer section of code that may or may not be reused several times throughout the project.

To define a function, start with the `function` keyword followed by a memorable name:

```
function myAmazingFunction() {
	// stuff happens here
}
```

A function can consist of one or several lines. So far, all we really know how to do is log information to the console. Try practicing modifying the function below with multiple `console.log` messages.
<p class="codepen" data-height="400" data-default-tab="html,result" data-slug-hash="MWBxRwR" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/MWBxRwR">
  IMS322-Functions</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<br><br>
## Changing Style Properties
In order to achieve some type of dynamic visual feedback in response to a user's input, we'll need to modify the style properties of one or HTML elements. Style properties for an element can be accessed with `myElement.style.property` where property is the name of a familiar CSS property. Some examples:
- `myElement.style.color = "white"` sets text color to white.
- `myElement.style.backgroundColor = "blue"` sets background color to blue.
- `myElement.style.height = "100px"` sets element height to 100px.

This can also be used to read an elements style property - notice the `console.log` line inside of the function below.

Try changing different style properties of the color swatch element in this embedded example. FYI, you'll often need to change multi-word CSS kebab-case properties to camelCase in JavaScript e.g. background-color becomes backgroundColor in JavaScript, font-size becomes fontSize, etc. 
<p class="codepen" data-height="400" data-default-tab="html,result" data-slug-hash="OJwqGXv" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/OJwqGXv">
  IMS322-Changing-Style-Properties</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<br><br>
## Toggling States
We've seen how to change a style property in response to a button press. But what if you want to change back? In this case, we'll need some method of checking the current state of the element. The logic for toggling back and forth between two states would look something like this:
- If currently in state A, change to state B.
- Else, change to state A.
Implied in the "else" in the second line is the statment "if currently not in state A".

In JavaScript, we can use an if statement to execute code based on our desired conditions:
```
if (property === stateA) {
	// do stuff to change to state B
}
else {
	// do stuff to change to state A
}
```

Notice that a triple equals sign is used for the comparison part of the if statement, while a single equals sign is used to assign/change properties. 
<p class="codepen" data-height="400" data-default-tab="html,result" data-slug-hash="wvxOZqE" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/wvxOZqE">
  IMS322-Changing-Style-Properties</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>