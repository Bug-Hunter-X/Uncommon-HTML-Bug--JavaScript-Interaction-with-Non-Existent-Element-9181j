# Uncommon HTML Bug: JavaScript Interaction with Non-Existent Element

This repository demonstrates a subtle bug in HTML where JavaScript attempts to interact with an element that doesn't exist in the DOM.  The bug causes unexpected behavior and highlights the importance of robust error handling in JavaScript when dealing with dynamic content.

## The Bug

The `bug.html` file contains a simple HTML structure with a `<div>` element with the id "myDiv".  The JavaScript code attempts to modify the content of a non-existent element ("nonExistentDiv") and hides the existing "myDiv" element.  The error of trying to access a non-existent element is silently ignored by the browser.

## The Solution

The `bugSolution.html` file demonstrates the corrected code. Before manipulating an element, it checks for its existence using `document.getElementById()`.  If the element does not exist, an appropriate message or alternative action is performed.  This helps prevent unexpected behavior and silent failures.

## How to reproduce the bug

1. Open `bug.html` in a web browser.
2. Observe that the text within the div with id "myDiv" is initially visible but then disappears.  The console will show no error message although the javascript is attempting to modify a non-existent element.