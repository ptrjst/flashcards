# Ruby - Vocabulary

A set of important vocabulary for Ruby the programming language.

### ancestor & descendant vs. parent & child

TODO: Write answer for this question.

### predicate method

A predicate method is a Ruby method whose name ends with a question mark `?` and returns a Boolean value. In the following example, `empty?` is a predicate method:

    do_something_with(array) unless array.empty?

In the following RSpec example, the method named `be_empty` is known as a "predicate matcher":

    array.should be_empty