---
title: IMS322 Documentation - Spring 2023
---

# Handling Inputs

[Home](index)

Broadly, we can classify controls into two categories - those that require handling data, and those that do not. For example, a button does not ask the user for any input values or text - they click, something happens, end of story.
<p class="codepen" data-height="400" data-default-tab="js,result" data-slug-hash="qBMbNpz" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/qBMbNpz">
  IMS322-Handling-Inputs-Button</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

However, for other controls like sliders or text entry fields, the resulting action is usually dependent on the data provided at the time of the interaction.
<p class="codepen" data-height="400" data-default-tab="js,result" data-slug-hash="RwYrRya" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/RwYrRya">
  IMS322-Handling-Inputs-Slider</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

For these types of inputs, the specific event you are listening for will depend on the input type, but most often the "change" or "input" event will be the most appropriate (as opposed to the "click" event we use for buttons). Much like button event handlers, an event listener with a corresponding function should be attached to the input element. However, in order to get the data input by the user, we want to look at the `value` attribute of the element.
<p class="codepen" data-height="400" data-default-tab="js,result" data-slug-hash="zYJrBQV" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/zYJrBQV">
  IMS322-Handling-Inputs-More</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

The value attribute also works in reverse - very handy when you want a control to update based on some other data!
<p class="codepen" data-height="400" data-default-tab="js,result" data-slug-hash="bGxEweK" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/bGxEweK">
  IMS322-Handling-Inputs-Setting-Value</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

