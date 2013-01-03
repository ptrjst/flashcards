# Ruby Keywords

A set of important reserved words (keywords) for Ruby the programming language. Based off Zed Shaw's [Learn Ruby the Hard Way](http://ruby.learncodethehardway.org/) and containing definitions wording directly from [ruby-doc.org](ruby-doc.org). Forked from [Thornquest's Quizlet flashcard deck](http://quizlet.com/11068057/learn-ruby-the-hard-way-keywords-flash-cards/). Containing additional descriptions from the O'Reilly Ruby Pocket Reference (2007).

## alias

To create a another name for an existing method, operator, or global variable.

``` ruby
class Microwave
  def on
    puts "The microwave is on"
  end

  alias :start :on  # using symbols
  alias go on       # using... not symbols
end

m = Microwave.new
m.start  # same as m.on
m.go     # same as m.on
```

and
A command that appends two or more objects together.

begin
Delimits a `begin` block of code or group of statements, which can allow the use of while and until in modifier position with multi-line statements. Closes with `end`.

BEGIN
Designates code that must be run unconditionally at the beginning of the program before any other.

break
Terminates a `while` or `until` loop, or a method inside a block. Gives an unconditional termination to a code block, and is usually placed with an argument.

case
starts a case statement; this block of code will output a result and end when it's terms are fulfilled, which are defined with when or else.

class
Opens a class definition block, which can later be reopened and added to with variables and even functions. Closes with `end`.

def
Used to define a function. Closes with `end`.

defined?
A boolean logic function that asks whether or not a targeted expression refers to anything recognizable in Ruby; i.e. literal object, local variable that has been initialized, method name visible from the current scope, etc.

do
Paired with end, this can delimit a code block, much like curly braces; however, curly braces retain higher precedence.

## each

Calls block once for each element in self, passing that element as a parameter. If no block is given, an enumerator is returned instead.

``` ruby
names = ["Bogdanovich", "Cassavetes", "Kubrick"]

names.each do |name|
  puts "Hello #{name}!"
end
```

else
Gives an "otherwise" within a function, if-statement, or for-loop, i.e. if cats = cute, puts "Yay!" else puts "Oh, a cat."

elsif
Much like else, but has a higher precedence, and is usually paired with terms.

END
Designates, via code block, code to be executed just prior to program termination.

end
Marks the end of a while, until, begin, if, def, class, or other keyword-based, block-based construct.

ensure
Marks the final, optional clause of a begin/end block, generally in cases where the block also contains a rescue clause. The code in this term's clause is guaranteed to be executed, whether control flows to a rescue block or not.

false
denotes a special object, the sole instance of FalseClass. false and nil are the only objects that evaluate to Boolean falsehood in Ruby (informally, that cause an if condition to fail.)

for
A loop constructor; used in for-loops.

if
Ruby's basic conditional statement constructor.

in
Used with for, helps define a for-loop.

module
Opens a library, or module, within a Ruby Stream.

next
Bumps an iterator, or a while or until block, to the next iteration, unconditionally and without executing whatever may remain of the block.

nil
A special "non-object"; it is, in fact, an object (the sole instance of NilClass), but connotes absence and indeterminacy. nil and false are the only two objects in Ruby that have Boolean falsehood (informally, that cause an if condition to fail).

not
Boolean negation. i.e. not true # false, not 10 # false, not false # true.

or
Boolean or. Differs from || in that or has lower precedence.

redo
Causes unconditional re-execution of a code block, with the same parameter bindings as the current execution.

rescue
Designates an exception-handling clause that can occur either inside a begin<code>/<code>end block, inside a method definition (which implies begin), or in modifier position (at the end of a statement).

retry
Inside a rescue clause, causes Ruby to return to the top of the enclosing code (the begin keyword, or top of method or block) and try executing the code again.

return
Inside a method definition, executes the ensure clause, if present, and then returns control to the context of the method call. Takes an optional argument (defaulting to nil), which serves as the return value of the method. Multiple values in argument position will be returned in an array.

self
The "current object" and the default receiver of messages (method calls) for which no explicit receiver is specified. Which object plays the role of self depends on the context.

super
Called from a method, searches along the method lookup path (the classes and modules available to the current object) for the next method of the same name as the one being executed. Such method, if present, may be defined in the superclass of the object's class, but may also be defined in the superclass's superclass or any class on the upward path, as well as any module mixed in to any of those classes.

then
Optional component of conditional statements (if, unless, when). Never mandatory, but allows for one-line conditionals without semi-colons.

true
The sole instance of the special class TrueClass. true encapsulates Boolean truth; however, <emph>all</emph> objects in Ruby are true in the Boolean sense (informally, they cause an if test to succeed), with the exceptions of false and nil.

undef
Undefines a given method, for the class or module in which it's called. If the method is defined higher up in the lookup path (such as by a superclass), it can still be called by instances classes higher up.

unless
The negative equivalent of if. i.e. unless y.score > 10 puts "Sorry; you needed 10 points to win." end.

until
The inverse of while: executes code until a given condition is true, i.e., while it is not true. The semantics are the same as those of while.

when
Same as case.

while
Takes a condition argument, and executes the code that follows (up to a matching end delimiter) while the condition is true.

yield
Called from inside a method body, yields control to the code block (if any) supplied as part of the method call. If no code block has been supplied, calling yield raises an exception.
