## FAQ

*The full assignment description is provided below - however, you are only responsible for the HTML and CSS content for this submission.*

*For this final version of the assignment, all steps in the Procedure must be completed. You can copy-paste the `<body>` element's content and `style.css` file from your CSS-only Repl.*

### Description
A basic FAQ (Frequently Asked Questions) page with at least 4 Question-Answer pairs. This assignment should use JavaScript to show/hide each Answer and change the Indicator button to indicate open/closed states (both with transitions).

*FYI - There is an HTML element called `<details>` that functions as a disclosure widget without any JavaScript. However, this approach does not provide a means to animate the open/close transition.*

Examples:
- [Nintendo Switch FAQ page](https://www.nintendo.com/switch/faq/)
- [Cards Against Humanity support page](https://www.cardsagainsthumanity.com/support)
- [Miami University - Dining Services Students' FAQ page](https://www.miamioh.edu/campus-services/dining/about/frequently-asked-questions/student-faq/index.html)
<br><br>
### Procedure
1. Build out the structure of your HTML. A single Question-Answer pair has been provided for you in `<article>` tags. You can start by duplicating the contents of the first `<article>` until you have 4 total. Then, replace the placeholder content with your own.  The actual content of the Questions and Answers is up to you - either copy-paste from an existing FAQ or make up your own around a common theme/topic.
2. Style your CSS accordingly:
	1. Create contrast between the Question and Answer elements. This can be done with `background-color`, `font-weight`, `color`, or whatever properties you'd prefer.
	2. Decide on the presentation of your open/close Indicator and its position in relation to the Question. This includes:
		1. Adjusting the style of the `<button>` element to match the Question styling (e.g. remove `border`, change `background-color`, etc.).
		2. Choosing a symbol/icon (to replace the placeholder "Indicator" text).
		3. Finalizing a position to the left or right of the Question text. The recommended approach here it to turn the outer Question `<div>` into a flexbox with `display:flex;` in your CSS. This will put the Indicator button and Question text side-by-side. Additional details, such as spacing and alignment, can be adjusted to taste.
3. Use JavaScript to implement an open/close state change for each individual Question-Answer pair when its corresponding Indicator button is pressed. This interaction should incorporate the following changes:
	1. Modify the Indicator button to show its current state. The exact approach is up to you -  possibilities include swapping out the character/icon with the `innerText` property or rotating the symbol.
	2. Show/hide the Answer text. The most straightforward approach here is to set the `height ` style property of the Answer element to `0` with `overflow: hidden`, which will prevent the text from spilling over. **Do not use `display: none` as this will disable the transition animation.**
	3. You will need some method to check the current state of each Answer so that you can alternate between open and closed properties. You may create separate variables like `isOpen1`, `isOpen2`, etc that can be set to `true` or `false` as needed. Or, you can check the currently applied style properties each time.
4. After you have the basic JavaScript functionality, you should revisit your CSS and adjust as needed. If you haven't already, you will need to add a transition time for the Indicator and Answer elements. Any other layout or spacing issues should also be cleaned up.
<br><br>
### Submission
1. Click the "Submit" button in the upper-right corner of Replit when you are finished. This will notify the instructor of your submission time. You may click "Resubmit" as many times as you'd like to submit changes/updates - however, keep in mind that this will also change the timestamp on your submission.
2. Submit the URL from your Repl's Webview tab to the associated Canvas assignment. This will ensure that it gets marked off of your Canvas to-do list.
<br><br>
### Grading
Please see the Assignment Rubric in Canvas for grading criteria.