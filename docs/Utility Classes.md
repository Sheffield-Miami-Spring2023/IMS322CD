---
title: IMS322 Documentation - Spring 2023
---

# Utility Classes

[Home](index)

Up until now, we have mostly talked about naming classes for styling with a "semantic" approach, meaning that a class is usually named for the content where it is being applied (e.g. main-section, album-art, volume-slider, etc.).

Utility classes are a different approach to class naming and CSS styling. They tend to have a single purpose and are named for *what they do*, rather than *what they're being applied to*. One way in which we've already applied the utility class approach is when using the class "flex-container" to style a flex box. Other examples of utiliy classes might be: bg-blue, large-font, etc. The semantic and utility approaches are most powerful when used in combination - remember that you can apply multiple classes to the same HTML element.
<p class="codepen" data-height="400" data-default-tab="html,result" data-slug-hash="mdLaaNP" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/mdLaaNP">
  IMS322-Utility-Classes</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

## Adding and removing classes
Although you can change individual style properties of elements directly from within JavaScript, sometimes it can be more practical to define style alterations in utility classes and use JavaScript to add and remove classes as needed. For example, having an "inactive" or "hidden" class to make an element look deactivated or invalid. Classes can be added or removed using `element.classList.add()` and `element.classList.remove()`. You can also toggle a class on or off using `element.classList.toggle()` - this approach is best when you simply need to alternate between 2 states.
<p class="codepen" data-height="400" data-default-tab="html,result" data-slug-hash="JjvwxGg" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/JjvwxGg">
  IMS322-ClassList</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

## Hiding inactive content
Think about some other ways that you can not just make content look inactive, but hide it entirely when it is not active...
<p class="codepen" data-height="400" data-default-tab="html,result" data-slug-hash="gOzZqGR" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/gOzZqGR">
  IMS322-Utility-Hide</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>