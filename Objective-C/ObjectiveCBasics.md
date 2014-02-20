Objective-C Basics
==================

### How much of C is available in Objective-C?

All of it. Objective-C is a strict superset of C. Everything you can do in C, you can do in Objective-C. It adds new syntax for class, methods, etc. 

### How do you include a library at the top of a file?

Old way:

    #import <Foundation/Foundation.h>

New way:

    @import Foundation

This new feature is called Modules or "semantic import".

### Do all objects live in the heap?

Yes. In Objective-C, all objects live in the heap and we have pointers to them. The language handles the allocation and freeing of this memory automatically.

Properties
----------

### What is a property?

A property is the combination of a getter method and a setter method in a class to provide access to an instance variable.

### Weak vs. strong properties

This is how Objective-C knows when to free the memory for an object.

Pointer properties must be strong.

Strong means keep the memory for the thing this points to as long as I or anyone else has a strong pointer to it (automatic eference counting). As soon as there are no strong pointers to it, the memory will get reclaimed.

Weak means keep it in memory as long as someone has a strong pointer to it. Then it gets set to nil.

### What does the property attribute `strong` mean?

This property is a strong (owning) reference to an object.

### What does the property attribute `weak` mean?

This property is a weak (nonowning) reference to an object.

### What does the property attribute `assign` mean?

This property's setter method simply assigns the property's variable to whatever is passed in, and performs no memory management.

### What does the property attribute `copy` mean?

This property's setter copies any object passed to it, creating a duplicate object.

### What does the property attribute `readwrite` mean?

This property generates both getter and setter methods.

### What does the property attribute `readonly` mean?

This property does not generate a setter method, rendering the property read-only by other classes.

### What does the property attribute `nonatomic` mean?

This property's setter and getter do not attempt to get a lock before making changes to the variable, rendering it thread-safe.
