---
title: IMS322 Documentation - Spring 2023
---

# Coding Conventions

[Home](index)
<br><br>
## General
- Be consistent with your indentation. Use the tab key at the start of each sub element. The text editor and browser do not care about empty space in your code, but consistent indentation improves readability and makes troubleshooting much easier.
<br><br>
## HTML
- Use comments as needed to clarify and organize: `<!-- This is an HTML comment -->`
- Try to practice "semantic HTML" - this means using descriptive tags whenever possible. For example: `<header>`, `<nav>`, `<main>`, `<section>`, or `<footer>` instead of just `<div>`. You can read more about semantic HTML on this [W3 Schools page](https://www.w3schools.com/html/html5_semantic_elements.asp).
<br><br>
## CSS
- Use comments as needed clarify and organize: `/* This is a CSS comment */`
- Apply styles using **classes** instead of element or id.
- Write all classes using the "kebab-case" convention: all lowercase, individual words separated by hyphens. For example: `headshot-photo`, `primary-button`, etc.
- Give your classes descriptive rather than generic names. Something like `product-photo` or `flex-container` instead of just `image1` or `parent`.
- Remember that you can apply multiple classes to a single element! For example, if you want to define a common size and border for all buttons, but you want to use different colors to indicate their function, an individual button's class attribute in HTML might look something like: `class="all-buttons primary-button"`.
- Be consistent with units and values within your project. For example, do not switch back and forth between hex and RGB color values.
<br><br>
## JavaScript
-   Use comments as needed clarify and organize: `// This is a JS comment`
-   Write all variable and function names using the "camelCase" convention: start lowercase, capitalize each successive word, no spaces or hyphens. For example: `myVariable`, `primaryButton`, etc.