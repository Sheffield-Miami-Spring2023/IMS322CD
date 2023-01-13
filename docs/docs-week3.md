---
title: IMS322 A&B Documentation - Fall 2022
---

[Back to schedule](index.md)

# Week 3 - Going Further With CSS - 9/5-9/7

Before we get started with JavaScript next week, we're going spend a little more time with CSS. A few of the techniques covered below are simply matters of convenience and consistency, though some will help you make your sites a bit more dynamic before implementing genuine interactivity.

## Incorporating external fonts

There are a handful of <a href="https://developer.mozilla.org/en-US/docs/Learn/CSS/Styling_text/Fundamentals#web_safe_fonts" target="_blank">"web-safe fonts"</a> like Arial and Helvetica that you can generally assume will be available on every user's system. If you would like to incorporate additional external fonts, a simple way to do so is to use one provided through a <a href="https://developer.mozilla.org/en-US/docs/Glossary/CDN" target="_blank">Content Delivery Network</a> or CDN. These servers store copies of data (like fonts) and make them available at the time the site is requested. You can access CDN resources with link tags.  

The example below incorporates fonts from <a href="https://fonts.google.com" target="_blank">Google Fonts</a> and <a href="https://fonts.adobe.com/?ref=tk.com">Adobe Fonts</a>. Notice that the Google Fonts CDN setup actually uses 3 link tags - these are provided to you when you select a font from their collection.

<p class="codepen" data-height="400" data-theme-id="dark" data-default-tab="html,result" data-slug-hash="qBowmBR" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/qBowmBR">
  Week3-1-External-Fonts</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

---

## CSS variables

In order to maintain consistency and easily try multiple styling options, you can define one or more <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties" target="_blank">CSS variables</a> (aka custom properties) at the top of your stylesheet. The basic definition of these variables is very simple - simply declare values in the :root selector starting each one with "&#8208;&#8208;". Then, throughout the rest of your styling, apply the custom property using "var(&#8208;&#8208;property-name)". Changing the value where the variable is defined will then propagate through every instance where it has been used.  

<p class="codepen" data-height="400" data-theme-id="dark" data-default-tab="html,result" data-slug-hash="gOeyWpK" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/gOeyWpK">
  Week3-2-CSS-Variables</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

---

## Pseudo-classes

A <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes" target="_blank">pseudo-class</a> refers to a special state of an element, e.g. when a button is being clicked (:active) or hovered over (:hover). Adding the pseudo-class to a selector allows you to apply additional styling when the element is in that state.  

There are many pseudo-classes defined at the link provided above, some more esoteric than others. Hover and active are the most useful for our purposes in this class, but some others can help apply styling to specific elements in a large group (e.g. a list).  

<p class="codepen" data-height="400" data-theme-id="dark" data-default-tab="html,result" data-slug-hash="ExEJmyg" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/ExEJmyg">
  Week3-3-Pseudo-Classes</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

---

## CSS transforms and transitions

You are already familiar with adjusting an element's position using margin properties. The <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/transform" target="_blank">transform</a> property can also do this (and more) with some added flexibility. I find transform especially powerful when applied using a pseudo-class and combined with a <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/transition" target="_blank">transition</a> duration. With transform, you can easily move, scale, or skew an element out and back to its default position, an approach that works especially well for interactivity and dynamic behaviors.  

<p class="codepen" data-height="400" data-theme-id="dark" data-default-tab="html,result" data-slug-hash="abYgaJR" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/abYgaJR">
  Week3-4-Transforms</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

## CSS animations

If you have ever used video editng software before (like Final Cut Pro or Adobe Premiere), you are likely familiar with the concept of keyframes. In short, keyframes define starting and ending values for things that should happen over time, like fades or wipes.  

<a href="https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Animations/Using_CSS_animations" target="_blank">CSS animations</a> are defined using a @keyframes sequence and then applied to an element with the animation-name property. Unforuntately, unlike pseudo-class transitions, animations run automatically when the page is rendered, so they cannot easily be applied or re-run in response to a user's input. However, you can specify different timing functions, iteration counts, and delays.  

<p class="codepen" data-height="400" data-theme-id="dark" data-default-tab="html,result" data-slug-hash="BargOvR" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/BargOvR">
  Week3-5-Animation</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>