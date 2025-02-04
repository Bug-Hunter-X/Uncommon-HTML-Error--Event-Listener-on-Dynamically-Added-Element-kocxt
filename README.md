# Uncommon HTML Error: Event Listener on Dynamically Added Element

This repository demonstrates a common error when working with dynamically added elements in HTML and JavaScript.  The issue arises when trying to attach an event listener to an element that hasn't yet been fully integrated into the Document Object Model (DOM).

**The Problem:**

The `bug.html` file shows an attempt to add a click event listener to a dynamically created `<div>` element.  However, because the event listener is attached *before* the element is added to the DOM using `document.body.appendChild()`, the event listener is never triggered when the `<div>` is clicked.

**The Solution:**

The `bugSolution.html` file presents the corrected approach.  The event listener is attached *after* the element has been successfully added to the DOM, ensuring that the event listener functions correctly.

This example highlights the importance of DOM timing and order of operations when working with dynamic elements and event listeners.