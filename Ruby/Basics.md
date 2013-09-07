Ruby Basics
===========

### Everything in Ruby is an ___.

object

Even simple numeric literals and the values true, false, and nil.

### The special value that indicates the absence of a value

`nil`

Ruby's version of null

### Is the Ruby convention to use tabs or spaces?

Spaces. Two spaces per ident.

### Should Ruby have lots of comments?

No. Good Ruby code should speak for itself, and most of the time you should let it do its own talking. 

Good code is like a good joke: It needs no explanation. 

### What is "snake case"?

The `lowercase_words_separated_by_underscores` naming style used for methods, arguments, and variables. 

Class names are the only exception. They're camel case: `MovieTheatre`. 

### What is the naming style for constants?

Ruby programmers seem divided between camel case:

`FurlongsPerFortnight = 0.0001663`

And all uppercase, punctuated by underscore:

`ANTLERS_PER_MALE_MOOSE = 2`

Russ Olsen prefers all uppercase.

### What are blocks?

Ruby's implementation of closures.

### How can you print out the current callstack?

	puts caller
	
### What's another way of saying "call a block"?

Yield to a block.

### What is the return value of a lamba?

A proc.

### Are procs, blocks, and lambdas all the same thing?

Yes. They're all closures.

But, not. They're implemented differently.

### What's a predicate method?

A predicate method is a Ruby method whose name ends with a question mark `?` and returns a Boolean value. In the following example, `empty?` is a predicate method:

    do_something_with(array) unless array.empty?

In the following RSpec example, the method named `be_empty` is known as a "predicate matcher":

    array.should be_empty

## Internals

### Where is the Ruby standard library located?

You can find it on GitHub here:

https://github.com/ruby/ruby/tree/trunk/lib

Its documentation is here:

http://www.ruby-doc.org/stdlib-1.9.3/

### What is the name of Ruby's virtual machine?

YARV (Yet another Ruby VM)—it's the official interpreter for Ruby, starting in Jan. 2007 with version 1.9.

YARV was written by Koichi Sasada and is also known as KRI (Koichi's Ruby Interpreter).

### How might you get a list of an object's methods containing the word "event"?

	my_obj.methods.grep(/event/)