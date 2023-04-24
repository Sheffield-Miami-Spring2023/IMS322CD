---
title: IMS322 Documentation - Spring 2023
---

# Single Page Navigation

[Home](index)

## Page anchors and smooth scrolling

The `<a>` element can be used for more than just linking to external websites. You can also provide an id for an element further down the page as the href attribute of that `<a>` tag, which will cause the page to scroll down to that location. By default, this will happen with an immediate (and somewhat disorienting) "snap". Adding the `scroll-behavior: smooth;` property to the body causes the scroll location to transition smoothly, which is not only more visually appealing, but can help the user better orient themselves within the document.

<p class="codepen" data-height="540" data-theme-id="dark" data-default-tab="html,result" data-slug-hash="mdKwYWJ" data-editable="true" data-user="ersheff" style="height: 540px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/mdKwYWJ">
  Week13-1-Smooth</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

## Sticky elements

An header, title, or nav element can be given the appearance of being fixed in place with the `position: sticky;` property. When combined with `top: 0;`, this will cause the element to be stuck to the top of the window as you continue to scroll down. You can see this in action across multiple sections in the course syllabus on Canvas.  

In the examples below, the sticky property has been combined with page links/anchors and smooth scrolling to give ensure that the navigation element always remains visible, even when moving up or down the page. This also eliminates the need for separate links that go back to the top since the link back to the first section is always visible.  

One small caveat with sticky positions: "a sticky element 'sticks' to its nearest ancestor that has a 'scrolling mechanism'". This might require you to slightly modify the structure of your HTML to get the intended behavior. This is why an extra `<div>` element has been wrapped around everythign else in the examples below - it changes the parent/sibling relationship of the `nav` and `main` elements in the first example, `aside` and `section` elements in the second.  

Top navbar implementation:

<p class="codepen" data-height="580" data-theme-id="dark" data-default-tab="html,result" data-slug-hash="KKeqLqy" data-editable="true" data-user="ersheff" style="height: 580px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/KKeqLqy">
  Week13-2-Sticky</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

Sidebar implementation:

<p class="codepen" data-height="640" data-theme-id="dark" data-default-tab="html,result" data-slug-hash="VwdWOQw" data-editable="true" data-user="ersheff" style="height: 640px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/VwdWOQw">
  Week13-3-Sticky2</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

## Tabbed interface

While there are many examples of tabbed interfaces available online with different approaches, a fairly simple implementation can be achieved with thoughtful styling. In the example below, the tabs are `<button>` elements that have a border radius applied only to the top corners. Since they have the same background color as the main sections, it gives the appearance of the button being a tab that is attached to the top of the content. From there, the JavaScript simply adds and removes the `.active-button` and `.active-section` classes. Inactive sections are hidden by setting the display property to `none`, while the button states are visually indicated through background color.

<p class="codepen" data-height="480" data-theme-id="dark" data-default-tab="html,result" data-slug-hash="abKwrKx" data-editable="true" data-user="ersheff" style="height: 480px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/abKwrKx">
  Week13-4-Tabs</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

## iframe

Using an iframe is probably the quickest and most convenient way to embed existing projects in a new site. An iframe is basically a window within a window that can display a different web page. However, iframes can be fickle when it comes to presenting embedded content seamlessly. It is sometimes difficult to size the iframes appropriately according to the source content (i.e. to prevent a border or scrollbars within the iframe). One way to prevent this is to set the width and height large enough in the CSS through trial and error. It's also possible to use JavaScript to get the content size of the source and update the iframe accordingly, but solutions vary by browser and may not be reliable.

<p class="codepen" data-height="520" data-default-tab="html,result" data-slug-hash="oNaZWeZ" data-editable="true" data-user="ersheff" style="height: 520px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/oNaZWeZ">
  IMS322-iframes</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
