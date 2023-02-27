## Profile Page

**The full assignment description is provided below - however, you are only responsible for the HTML and CSS content for this submission.**

**For this final version of the assignment, all steps in the Procedure must be completed. You can copy-paste the `<body>` element's content and `style.css` file from your CSS Repl.**

### Description
This assignment includes 2 parts built using HTML, CSS, and JS:
- A questionnaire for gathering profile information.
- A profile page that is automatically populated using the information entered in the questionnaire.
These two parts should be developed in tandem and presented on a single page (though not necessarily simultaneously, more details below). While it is not required to design distinct desktop and mobile layouts, the questionnaire and profile page should work well at both desktop (approx. 800px) and mobile (approx. 420px) window widths.
<br><br>
### Procedure
1. Imagine a fictional social site built for a community of like-minded individuals with a specific niche interest or hobby. You will be designing your questionnaire and profile page to suit the interests of this community. Some ideas:
	1. Lizard terrarium owners.
	2. Regional sandwich enthusiasts.
	3. American hurling athletes.
	4. Earthworm photographers.
	5. Anything else you might think of!
2. Build out the structure of your HTML with the following:
	1. For the questionnaire:
		1. Text input field(s) for first and last name.
		2. An `<input type="date">` element to enter birthdate or a different relevant date e.g. "lizard adoption day."
		3. An `<input type="radio">` or `<select>` element to choose from a prefilled list of options that are relevant to the community. 
		4. At least 2 other pieces of information gathered using appropriate input types.
	2. For the profile page:
		1. A generic profile pic. This can be prefilled and does not need to be gathered in the questionnaire.
		2. Displays for all of the information gathered in the questionnaire. These can be prefilled with placeholder text during the development phase.
3. Style your CSS accordingly:
	1. Design a layout for your inputs, text, and image for both parts. Remember that both parts will be presented as a single page. The specific mechanism for this is up to you, though the recommended options are:
		1. Side-by-side (or top-bottom when in mobile view).
		2. One at a time, with visibility handled by JavaScript.
		3. Advanced: Using a modal (popup) for the questionnaire - this will not be covered in class, but there are many examples online.
	2. Implement general styling (e.g. color scheme and fonts) appropriate to the community's interests.
	3. Liberal usage of flexboxes is **highly** recommended.
	4. Depending on your specific layout, a media query **may be required** to ensure that your layout works well on both desktop (approx. 800px) and mobile (approx. 420px) displays. Don't forget to open your browser's Responsive Design Mode to test this!
4. Use JavaScript to implement the following behaviors:
	1. A "submit" button that initiates the following:
		1. Gathers all user-entered information in one step and populates the profile page.
		2. Toggles visibility for questionnaire and profile sections (if needed).
		3. *Note: Do not use the `<input type="submit">` element for this as it is intended for scenarios that submit data to a server. A standard `<button>` will do just fine.*
5. After you have added JavaScript functionality, you should revisit your CSS and adjust as needed.
<br><br>
### Submission
1. Click the "Submit" button in the upper-right corner of Replit when you are finished. This will notify the instructor of your submission time. You may click "Resubmit" as many times as you'd like to submit changes/updates - however, keep in mind that this will also change the timestamp on your submission.
2. Submit the URL from your Repl's Webview tab to the associated Canvas assignment. This will ensure that it gets marked off of your Canvas to-do list.
<br><br>
### Grading
Please see the Assignment Rubric in Canvas for grading criteria.