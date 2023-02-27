---
title: IMS322 Documentation - Spring 2023
---

# More Input Types

[Home](index)
<br><br>
HTML provides several types of input types and controls that you can choose from to best address your needs. As you've seen with some `<input>` types like text, number, and range, data can generally be handles by examining the element's data attribute in JavaScript.

In the examples below, pay close attention to the use of the "change" event in the attached event listenere. Remember, there are 3 types of events that we have used so far:
- "click" - fires on a click, best for buttons
- "change" - fires when a user has finished changing an input e.g. pressed "return" or clicked away from the input
- "input" - fires continuously while an input is being modified, good for sliders
<br><br>
## `<input type="date">`
Pretty self-explanatory - an input that presents the user with a calendar interface to choose a date.
<p class="codepen" data-height="400" data-default-tab="html,result" data-slug-hash="GRXNBbL" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/GRXNBbL">
  IMS322-Input-Date</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<br><br>
## `<input type="radio">`
Radio buttons are presented as a list of options from which only one can be selected at a time - best for multiple choice style questions or prompts. Notice the use of the `<label>` element to display the text for each option. Also, the value attribute of each choice is set independently of its display text in the associated `<label>`. Radio buttons are grouped together by giving them all the same name attribute and placing them in a `<fieldset>` element.

Something that can get kind of messy with radio buttons is figuring out how to retrieve a value from only one of the options. The `<fieldset>` element helps with part of this problem as we can attach one event listener to it rather than making multiple for all of the individual `<input>` elements. Figuring out which of the options was checked is a little tricky. For this, we're using the generic `document.querySelector()` method which can look for elements by using attributes other than their id - in this case, whether or not they are currently checked.
<p class="codepen" data-height="400" data-default-tab="html,result" data-slug-hash="abaBayj" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/abaBayj">
  IMS322-Input-Radio</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<br><br>
## `<select>`
The `<select>` element is kind of an outlier when it comes to HTML-based inputs. It does not use the `<input>` tag; rather, it has its own unique tag. Beyond that, its functionality is similar to the radio button in that it only allows a user to make one choice from a prefilled list of options. It is generally the more straightforward implementation of this input style if it is not necessary to present all available options at the same time.
<p class="codepen" data-height="400" data-default-tab="html,result" data-slug-hash="KKxNxOQ" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/KKxNxOQ">
  IMS322-Input-Select</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>