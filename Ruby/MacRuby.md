MacRuby
=======

Author: Sean Moubry

This deck teaches the fundamentals of MacRuby--an implementation of Ruby 1.9 directly on top of Mac OS X core technologies such as the Objective-C runtime and garbage collector.

## Fundamentals

### Who is the primary author of MacRuby?

Laurent Sansonetti ([@lrz](twitter.com/lrz))

### What does the Ruby object `String` map to in Objective-C?

`NSMutableString`

### What does the Ruby object `Number` map to in Objective-C?

`NSNumber`

### What does the Ruby object `Array` map to in Objective-C?

`NSMutableArray`

### What does the Ruby object `Hash` map to in Objective-C?

`NSMutableDictionary`

### What does the Ruby object `Object` map to in Objective-C?

`NSObject`

### What are the big reasons to use MacRuby?

- Productivity and prototypes
- Ruby style
- Closures (blocks)
- Meta-programming
- RSpec and other test libraries
- Scripting without AppleScript

### What is Objective-C?

Object-oriented variant/extension of the C programming language. Like Ruby, it's heavily influences by Smalltalk.

### What is Core Foundation?

The C-language low level libraries that ship with Mac OS X. Related methods and data structures usually start with `CF`.

### What is Cocoa?

The framework for writing desktop applications. Includes Foundation (wrapper around many Core Foundation functions), AppKit, QTKit, etc. Most classes start with `NS` as part of the NextStep operating system.

### What is `llvm`?

### What is `clang`?
