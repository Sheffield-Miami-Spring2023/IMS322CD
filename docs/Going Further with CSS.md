---
title: IMS322 Documentation - Spring 2023
---

# Going Further With CSS

[Home](index.md)

Before getting into JavaScript, we're going spend some time with more advanced CSS properties. A few of the techniques covered below are simply matters of convenience and consistency, though some will help you make your sites a bit more dynamic before implementing genuine interactivity.
<br><br>
## CSS Variables

In order to maintain consistency and easily try multiple styling options, you can define one or more [CSS variables](https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties) (aka custom properties) at the top of your stylesheet. The basic definition of these variables is very simple - declare values in the `:root` selector starting each one with "--". Then, throughout the rest of your CSS file, you can apply this custom property using "var(--property-name)". Changing the value at the top where the variable is originally defined will then propagate through every instance where it has been used. Although it is not always shorter, you can think of it as a kind of shorthand - using "var(--red)" instead of `#FF3344`.
<p class="codepen" data-height="400" data-theme-id="dark" data-default-tab="html,result" data-slug-hash="gOeyWpK" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/gOeyWpK">
  IMS322-CSS-Variables</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<br><br>
## Pseudo-classes
A [pseudo-class](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes) refers to a special state of an element, e.g. when a button is being clicked (`:active`) or hovered over (`:hover`). Adding the pseudo-class to a selector allows you to apply additional styling when the element is in that state.

There are many pseudo-classes defined at the link provided above, some more esoteric than others. `Hover` and `active` are probably the most useful for our purposes in this class, but some others can help apply styling to specific elements in a large group (e.g. a list).  
<p class="codepen" data-height="400" data-theme-id="dark" data-default-tab="html,result" data-slug-hash="ExEJmyg" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/ExEJmyg">
  IMS322-Pseudo-Classes</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<br><br>
## CSS Transforms and Transitions
You are already familiar with adjusting an element's position using properties like `margin`. The <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/transform" target="_blank">transform</a> property can also do this (and more) with some added flexibility. I find transform especially powerful when applied using a pseudo-class and combined with a <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/transition" target="_blank">transition</a> duration. With transform, you can easily move, scale, or skew an element out and back to its default position, an approach that works especially well for interactivity and dynamic behaviors.  
<p class="codepen" data-height="400" data-theme-id="dark" data-default-tab="html,result" data-slug-hash="abYgaJR" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/abYgaJR">
  IMS322-Transforms</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<br><br>
## CSS Animations
If you have ever used video editng software before (like Final Cut Pro or Adobe Premiere), you are likely familiar with the concept of keyframes. In short, keyframes define starting and ending values for things that should happen over time, like fades or wipes.  

<a href="https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Animations/Using_CSS_animations" target="_blank">CSS animations</a> are defined using a @keyframes sequence and then applied to an element with the animation-name property. Unforuntately, unlike pseudo-class transitions, animations run automatically when the page is rendered, so they cannot easily be applied or re-run in response to a user's input. However, you can specify different timing functions, iteration counts, and delays.  
<p class="codepen" data-height="400" data-theme-id="dark" data-default-tab="html,result" data-slug-hash="BargOvR" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/BargOvR">
  IMS322-Animation</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>