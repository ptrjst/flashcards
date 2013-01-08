jQuery
=======

jQuery is a JavaScript library that simplifies common tasks such as finding/manipulating the elements of a document and using Ajax to make dynamic HTTP requests.  

The jQuery library focuses on queries, typically using CSS selectors to identify elements within the document.

### What is jQuery?

jQuery is a JavaScript library that simplifies common tasks such as finding/manipulating the elements of a document and using Ajax to make dynamic HTTP requests.

### What are some distinct features of jQuery?

* CSS selector syntax used for referring to elements in the document
* Efficient query method for finding the set of document elements that match a CSS selector
* Set of methods for manipulating selected elements
* Functions for operating on a group of elements, rather than one at a time
* Method chaining

### What is the name and shortcut for the jQuery library function?

Name: jQuery
Shortcut: $

### How do you get the set of `<div>` tags in a document?

    var divs = $("div");


### What does the following code do? `$("p.more").css("background-color", "gray").show("fast");`

    $("p.more").css("background-color", "gray").show("fast");

Highlights and quickly displays all hidden `<p>` tags that have the "more" class.
