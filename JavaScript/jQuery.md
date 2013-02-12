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

### How do you reference the jQuery library?

    <script src="jquery-1.7.1.js"></script>

### Where should you reference the jQuery library in an HTML page in order to get the best performance of the page?

At the bottom of the page just before the closing body tag.

### What is the name and shortcut for the jQuery library function?

Name: jQuery  
Shortcut: $

### How do you prevent conflicts when you are using `$` in your own code or using another library that uses `$`?

Call `jQuery.noConflict()` to restore `$` to its original value.

### What are the 4 ways to invoke the jQuery method?

1. Pass a CSS selector (string) to it and it will return matching elements.  
Optionally, you can pass an element or a jQuery object as a second argument, and it returns matching descendants.

        var paragraphs = $("p");

2. Pass an element, document, or window object to wrap the object in a jQuery object.

        $(document)

3. Pass a string of HTML text and it will return a jQuery object representing the element or elements.  
Optionally, you can pass a document object as a second argument for the elements to be associated with.  
You can also pass the names and values of attributes to set on the newly created elements as a second argument.

        var img = $("<img/>", { src:url, alt:desc });

4. Pass a function and that function will be invoked when the document has been loaded and the DOM is ready.  

        jQuery(function() { // Invoked when document has loaded.
            // All jQuery code goes here.
        });
        
    Old Syntax:

        $(document).ready(myfunction);

### When does jQuery trigger functions registered through $()?

When the **DOMContentLoaded** event is fired, if supported. Otherwise, wehn the **load** event is fired.

### How do you get the set of `<div>` tags in a document?

    var divs = $("div");

### How do you get all elements with id="surname"?

    var surnames = $("#surname");
    
### How do you get all elements with the CSS class "warning"?

    var warnings = $(".warning");

### What is method chaining?

Method chaining is a technique where each method returns an object (usually the current object itself), allowing the calls to be chained together in a single statement.

### What does the following code do? `$("p.more").css("background-color", "gray").show("fast");`

    $("p.more").css("background-color", "gray").show("fast");

Highlights and quickly displays all hidden `<p>` tags that have the "more" CSS class.

### What does the following code do? `$("ul li").addClass("accent");`

    $("ul li").addClass("accent");

Adds the CSS class named "accent" to all unordered list items.

### What does the following code do? `$(".hide").click(function () { $(this).slideUp("slow"); });`


    $(".hide").click(function () { $(this).slideUp("slow"); });

Registers an event handler on all elements that have the "hide" CSS class.

### What are two things you should do to improve the performance of the jQuery library on production?

1. Use a minified version of jQuery
2. Use a CDN distributed version (such as from [Google](https://developers.google.com/speed/libraries/devguide#jquery))
