## Expo Gallery
**Expo Due Date: Wednesday 5/3 by 2:30pm (no exceptions)**
**Final Revision Due Date: Wednesday 5/10 by midnight**

*You will be working in the same Replit project for both the "flow" and "final" submissions of this project. The due date in Replit will be set to 4/30 for the flow version, changed to 5/3 for the expo submission deadline, then finally changed to 5/10 for the final revision.*

### Description
For this project, you will be creating a gallery of your P5 Poem plus at least 2 of your other assignments from the semester. Eligible assignments are:
- Assignment 1 - FAQ
- Assignment 2 - Music Player
- Assignment 3 - Profile Page
- Assignment 4 - Data Visualization
You will be expected to fix and improve the assignments that you choose (see details below), so take this into consideration when making your choices.
<br><br>
### Requirements
- P5 Poem plus 2 or more assignments presented in a cohesive gallery/portfolio manner on a single page The specific mechanism by which this is accomplished is up to you, though here are some suggestions:
	- Show/hide sections using a top nav bar or sidebar
	- Smooth scrolling to different sections using a top nav bar or sidebar
	- A carousel-like component with left-right navigation buttons in which each "slide" includes section content
- Collecting all of your content into a single Replit project will be challenging. Again, there are multiple ways to accomplish this, including:
	- Move the HTML content from the individual `<body>` elements of each assignment into their own separate elements in the Project 2 `<body>`. This may produce a very dense HTML document, but will also probably be the method that results in the most cohesive presentation.
	- Similarly, you can move all of the CSS content from the individual `style.css` files into different CSS files with different names in the Project 2 Replit. This will require linking all of these new CSS files individually in the HTML head. The downside of this approach is that you must be absolutely certain that all of your CSS selectors (e.g. class names) from the different assignments are unique - otherwise, they will conflict with each other!
	- You can look into using `<iframe>` containers to embed the individual projects all on the same page. This is probably the most straightforward approach; however, this still needs to look seamless and will require additional styling of the `<iframe>` containers to prevent unwanted borders and scrollbars.
- Your name should be visible at all times e.g. in a sidebar, sticky header or footer, etc.
- Any errors, inconsistencies, or layout issues from your original submission should be fixed as necessary. Additionally, each individual component must include the following improvements or modifications:
	- **Assignment 1 - FAQ**
		- Ensure that the page loads with all answers hidden.
		- Add at least 3 pieces of supplemental content in appropriate locations that support the theme of you FAQ e.g. a product photo, general product description, company contact info or address, company logo, etc.
	- **Assignment 2 - Music Player**
		- Fix current time (mm:ss) readout so that the seconds display has a leading zero when needed e.g. 1:08.
		- Make the volume slider functional.
		- Add seek behavior to the playback progress slider.
		- If your original submission used the provided sample audio, it must be replaced with the song that corresponds with your original design.
	- **Assignment 3 - Profile Page**
		- Only one section, the questionnaire or profile, should be visible at a time. Questionnaire visibility should be toggled by the "Submit" button. A "back" or "edit" button should be provided in the profile section to go back to the questionnaire.
		- Data collection and bio update should still occur with a single "Submit" button (but NOT using the `<form>` element or `<input type="submit">`).
		- Controls with default styling (e.g. checkboxes, sliders, radio buttons) should be customized to better suit the questionnaire layout and styling (e.g. change background color, size, etc).
	- **Assignment 4 - Data Visualization**
		- If needed, replace your dataset with one that shows sufficient variation/progression between data points (you don't want all of your data points to look almost identical). This can be accomplished with a dataset that has more variation between points or just includes more data points over a longer time period.
		- Add a summary paragraph and descriptions that support the data. This should be done in HTML/CSS, not on the P5 canvas.
		- Provide a link to your data source (make sure that it is anonymized if you are using your own survey).
	- **Project 1 - P5 Poem**
		- Canvas centered in body.
		- A canvas size that is 800px wide. This may also require updating position and/or size parameters in your `script.js`.
<br><br>
### Submission
1. Work within the Expo Gallery assignment in your Team (class section) on Replit.
2. Click the "Submit" button in the upper-right corner of Replit when you are finished. This will notify the instructor of your submission time. You may click "Resubmit" as many times as you'd like to submit changes/updates - however, keep in mind that this will also change the timestamp on your submission.
3. Submit the URL from your Repl's Webview tab to the associated Canvas assignment. This will ensure that it gets marked off of your Canvas to-do list.
4. **These galleries will be shown publicly at the ETBD Student Expo on 5/3. Failure to have a presentable submission ready for the expo will result in an automatic 25% penalty.**
5. **After the Expo, you will have until Wednesday 5/10 by midnight to make revisions before final grading.**
  <br><br>
### Grading
Please see the Project 2 Rubric in Canvas for grading criteria.


Rubric:
General (10)
- All sections are present, refined, and include all improvements/modifications from the project description
- All sections are present, but some improvements/modifications have not been implemented
- One or more sections are missing/broken and/or no improvements/modifications have been implemented

Navigation (10)
- Navigation between sections is clear, effective, and well-implemented
- Navigation between sections is a bit awkward and/or confusing
- Navigation is broken and/or missing

Coding (10)
- There are no errors caused by the project code in the console, code is well-organized with consistent naming, spacing, and indentation
- There are some errors caused by the project code in the console and/or issues with the code organization, but the project still works
- There are many errors in the console and/or code preventing the project from running without additional modifications

Content and polish (10)
- All assets (e.g. images and sound) are high quality, color palette and other graphic content are thoughtfully designed and incorporated
- Some assets are low quality, color pallete and other graphic content is inconsistent, haphazard, or demonstrates little consideration for the overall presentation
- All assets are low quality or missing, color pallete and other graphic content is non-existent, glitchy, inappropriate, or completely unrelated to the content