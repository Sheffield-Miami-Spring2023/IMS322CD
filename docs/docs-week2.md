---
title: IMS322 A&B Documentation - Fall 2022
---

[Back to schedule](index.md)

# Week 2 - Responsive Web Design - 8/29-8/31

Read the <a href="https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Responsive_Design#responsive_design" target="_blank">section on Responsive Design</a> (RWD) in the MDN Web Docs.  

We will focus on the 3 techniques listed in that article: fluid grids, fluid images, and media queries.


## Relative units
Read the sections on "Absolute length units" and "Relative length units" on <a href="https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Values_and_units#numbers_lengths_and_percentages" target="_blank">MDN</a>.  

You do not need to memorize every possible relative unit, but knowing a few of them is key to getting started with RWD and being consistent with spacing and sizing. In particular, I would recommend regularly using the following:
- ch: width of a text character
- rem: height of the font size relative to the root element
- %: percentage/fraction relative to the parent element

It is completely fine to continue using absolute units like px, so long as it is done with intent and does not detract from the overall responsiveness of your design. For example, I will often still use px when sizing borders.

<p class="codepen" data-height="400" data-theme-id="dark" data-default-tab="html,result" data-slug-hash="zYWbvrL" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/zYWbvrL">
  Week2-1-Relative-Units</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

What effects do these relative units actually have? The ch and rem units, if used correctly, can be handy to ensure that padding or fixed sizing for any element will always be relative to the text content inside or around it. If you adjust the size of the preview panel, you'll notice that all of the elements with widths specified as percentages fluidly adjust to maintain their relative proportions (resizing the preview may work best if you click the "Edit on CodePen" link to open the pen in a separate editor). Of particular interest is the second dog photo - it is inside of a <section> element (blue background) that has a width of 50% relative to the <body>, while the image iteself also has a width of 50%. However, the image width is relative to its parent container, so it is 50% of the <section>.  

Percentages are *absolutely crucial* when developing pages with fluid grids and fluid images.  

-----

## Aspect ratio and object fit
One of the worst things that you can do to a lovely image is destroy its aspect ratio. Phones and professional cameras commonly shoot at 4:3 or 3:2. This can certainly be changed in cropping, but ultimately your goal should always be to try and prevent any squishing or stretching.  

Take a look at the multiple versions of the black dog photo below. The first one is destroyed because I've combined a relative unit (%) for the width and an absolute unit (px) for the height. As the size of the preview panel is changed, the picture becomes more or less distorted as its width changes while its height stays the same.  

An easy way to fix this is to only specific one dimension or the other. In the second version, I've only specified the width - the height automatically respects the image aspect ratio, and the overall size still adjusts relative to the parent element.  

If you need one dimension of an image to be absolute and/or will not be able to pre-process (crop) all of your images to ensure they have the same aspect ratio, you can try the <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/object-fit" target="_blank">object-fit</a> property to fill its bounding box without unwanted distortion, as seen in the third photo.  

<p class="codepen" data-height="400" data-theme-id="dark" data-default-tab="html,result" data-slug-hash="qBovObg" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/qBovObg">
  Week2-1-Relative-Units</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

-----

## Flexbox
Flexbox is one of the indispensible tools to achieve the "fluid grids" part of RWD. In short, a flexbox is a flexible layout method in which a container and its items (children) can automatically adjust to the size of the parent. It can also be very handy for alignment - specifically, centering content both horizontally and vertically, even if it is only one item.  

![Flex Container](images/01-container.svg)
![Flex Items](images/02-items.svg)

This first example demonstrates:
- The display property of the container set to "flex" to create a flexbox row
- The gap property of the container (space between items)
- The align-items property of the container (vertical alignment)
- The justify-content property of the container (horizontal spacing and alignment)

Try adjusting the size of the preview and changing some of the values specified for some CSS properties - in particular, the width of the flex items (again, this may work best if you click the "Edit on CodePen" link to open the pen in a separate editor).  

<p class="codepen" data-height="400" data-theme-id="dark" data-default-tab="html,result" data-slug-hash="MWVxamV" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/MWVxamV">
  Week2-3-Flexbox1</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

A couple of additional properties are demonstrated in the next example, namely:
- Giving flex items different flex property values to adjust their relative proportions
- Changing the flex-direction to "column" (row is the default)  

<p class="codepen" data-height="400" data-theme-id="dark" data-default-tab="html,result" data-slug-hash="WNzmEGK" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/WNzmEGK">
  Week2-4-Flexbox2</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

In general, flexbox is thought of as one-dimensional, either rows or columns. However, you can create a more sophiticated layout by embedding flexboxes within each other.  

<p class="codepen" data-height="400" data-theme-id="dark" data-default-tab="html,result" data-slug-hash="wvmOqeX" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/wvmOqeX">
  Week2-5-Flexbox3</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

Again, there are way too many flexbox properties to memorize them all. <a href="https://css-tricks.com/snippets/css/a-guide-to-flexbox/" target="_blank">This article on CSS-Tricks</a> is an excellent reference. For now, understanding the properties demonstrated in the examples above and outlined in the bullet points will likely be all you need for some time.  

*<a href="https://css-tricks.com/snippets/css/complete-guide-grid/" target="_blank">CSS Grid</a> is an even more powerful way to design fluid grid layouts. It is a bit more complicated than flexbox, so we will likely not spend any class time looking at it. However, you are welcome to check into it if you have the time and can incorporate CSS Grid in your asssignments if you become comforable using it.*

-----

## Media queries

Media queries can be used to modify CSS properties depending on the characteristics of the display or device. The last flexbox example above actually includes an extremely common application of media queries: changing the flex-direction of a flex container from row to column when the window gets narrow (and vice versa). However, any CSS property can be changed with a media query.  

<p class="codepen" data-height="400" data-theme-id="dark" data-default-tab="html,result" data-slug-hash="wvmOqQQ" data-editable="true" data-user="ersheff" style="height: 400px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/wvmOqQQ">
  Week2-6-Media-Queries</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>

The general format for a screen-sized based media query is:  

`@media (max-width: 600px) {`  
&nbsp;&nbsp;`stuff that changes goes here`  
`}`  

...where the width value is the display size threshold at which the changes will happen.  

*From Week 2 on, you will be expected to include a media query in every assignment that adjusts content for mobile vs. desktop displays. You are only required to have one that addresses phone-sized screens, but you are welcome to include multiple media queries if you want to try and improve layouts on additional device sizes.*

-----

## Responsive Design Mode (developer tools)
Responsive Design Mode is a function of your browser that makes responsive design easier. Specifically, it simulates specific device display sizes and orientations to help you evaluate media query adjustments, element sizes, and layout flow and organization. While simply adjusting the size of your browser window will sometimes be sufficient, Repsonsive Design Mode is a much more accurate, flexible, and reliable way to accomplish this. Make sure you know how to activate Responsive Design Mode in your specific browser.  


![RDM in Firefox](images/RDM.png)
Example of Responsive Design Mode in Firefox, set to display size of iPhone 12/13 Mini.