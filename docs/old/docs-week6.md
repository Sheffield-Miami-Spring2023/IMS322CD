---
title: IMS322 A&B Documentation - Fall 2022
---

[Back to schedule](index.md)  

# Week 6 - Handling Inputs 2 - 9/26-9/28

## More Controls
There are many different kinds of controls available beyond just buttons. A collection of control options is included in the example below. Most of them are created using different style attributes on the &lt;input&gt; element (<a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/select" target="_blank:">&lt;select&gt;</a> being a notable exception). You can find a reference list for all the input styles <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input" target="_blank">here</a>.  

When a text label with a description or instructions is required for your control, you should always use the <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/label" target="_blank">&lt;label&gt; element</a>. You can pair a label to a control by referencing the control's id in the label's "for" attribute.  

The <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/fieldset" target="_blank">&lt;fieldset&gt; element</a> can optionally be used to group similar controls together, like radio buttons and checkbox collections. Notice that the &lt;fieldset&gt; element has a default appearance - you can override these style properties in your CSS if desired.  

<p class="codepen" data-height="420" data-theme-id="dark" data-default-tab="html,result" data-slug-hash="yLjgoBN" data-editable="true" data-user="ersheff" style="height: 420px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/yLjgoBN">
  Week6-1-MoreControls</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>


## Submitting and handling data
Data input by the user can be handled on a case-by-case basis with event handlers. The specific event you are listening for will depend on the input type, but most often the "change" or "input" event will be the most appropriate.  

Much like button event handlers, an event listener with a corresponding function should be attached to the input element. However, in order to get the data input by the user, we want to look at the "value" attribute of the element.  

Remember that the format for adding event handlers is `element.addEventListener("event", function);` where:
- **element** is the variable that you have assigned to your HTML control element
- **event** is the type of event you are listening for, e.g. "click" or "change"
- **function** is the name of the function that you would like called when the event fires  

*(open the console to see the results for the following examples)*  

<p class="codepen" data-height="400" data-theme-id="dark" data-default-tab="html,result" data-slug-hash="Baxpmam" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/Baxpmam">
  Week6-1-MoreControls</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

You can optionally make a "submit" button to collect all of your input element values at the same time.

<p class="codepen" data-height="300" data-theme-id="dark" data-default-tab="html,result" data-slug-hash="GRdrOwd" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/GRdrOwd">
  Week6-3-HandlingData-Form</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>


## Getting and changing HTML attributes and CSS properties
We've already seen in the previous examples how the "value" attribute of an &lt;input&gt; element can be retrieved. There are other attibutes that you may want to retrieve or edit on-the-fly using JavaScript.  

<p class="codepen" data-height="500" data-theme-id="dark" data-default-tab="html,result" data-slug-hash="vYjgpzb" data-editable="true" data-user="ersheff" style="height: 500px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/vYjgpzb">
  Week6-4-Attributes</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

Styling can also be changed - most CSS properties are available as sub-properties of the general "style" attribute. Ususally, you'll need to change kebab-case to camelCase formatting in your JavaScript for multi-word CSS properties e.g. background-color becomes backgroundColor in JavaScript, font-size becomes fontSize, etc.  

<p class="codepen" data-height="400" data-theme-id="dark" data-default-tab="html,result" data-slug-hash="poVRaed" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/poVRaed">
  Week6-5-Styling</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>