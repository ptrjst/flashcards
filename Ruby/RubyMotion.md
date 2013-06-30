# RubyMotion

Concepts required for developers working with RubyMotion.

### Is RubyMotion an interpreter?

No. It's a compiler. It compiles Ruby down to native code.

### What is the Objective C library package manager?

CocoaPods

### What is Teacup?

github.com/rubymotion/teacup

Teacup is a DSL/library that comes with RubyMotion that lets you define stylesheets for UI elements.

It builds some separation between how you define the style of your components with how you're adding them into the view.

It's similar to how the structure of HTML is different from the styles in CSS.

### What is Bubblewrap?

github.com/rubymotion/bubblewrap

The most used abstraction library created for RubyMotion.

It was started for HTTP networking stuff, but now is slowly moving to abstract ALL of the Cocoa APIs -- JSON, XML, Camera, Location, Media, etc.

All of the most common, annoying things you have to do -- they're making it better for RubyMotion developers.

### What is the one big feature of the Ruby language that is not available in RubyMotion?

`eval`

This is to comply with Apple's Developer guideslines discourages interpreters in iOS apps.

### What is Formotion

github.com/clayallsopp/formotion

It's a DSL/abstraction library for "making iOS Forms insanely great" with RubyMotion.

### What is ParseModel?

github.com/adelevie/ParseModel

### What is MotionStateMachine?

github.com/opyh/motion-state-machine

Lets you built a finite state machine for view management.

### If you link a C library, is its constants available in your Ruby code?

Yes.

For example, if you could do:

    def glkView(view, drawInRect:rect)
      glClearColor(@curRed, 0.0, 0.0, 1.0)
      glClear(GL_COLOR_BUFFER_BIT)
      ...
    end
    
### Once you compile your Ruby code with RubyMotion, are there any additional libraries that have to be included in your compiled application, just because you're using RubyMotion?

Of course. There are many features of the Ruby language that would not work without a fair bit of Objective C code that gets included in your application.



### predicate method

A predicate method is a Ruby method whose name ends with a question mark `?` and returns a Boolean value. In the following example, `empty?` is a predicate method:

    do_something_with(array) unless array.empty?

In the following RSpec example, the method named `be_empty` is known as a "predicate matcher":

    array.should be_empty
    
### How do you update RubyMotion?

`sudo update motion`

You need to be root to run this command.

### How do you create a new RubyMotion project?

`motion create YourProjectName`

### What files are generated when you create a RubyMotion project?

```
.gitignore
Rakefile
app
app/app_delegate.rb
resources
spec
spec/main_spec.rb
```

### What happens when you just run `rake`?

Running `rake` from the command line is the same as running `rake default` and the description of the default Rake task is:

    Build the project, then run the simulator

### How do you list all of the rake tasks?

`rake --tasks`

### What does the `$:.unshift()` line do in the Rakefile?

The line in question—the second line of the generated Rakefile:

`$:.unshift("/Library/RubyMotion/lib")`

This tells Ruby to look in `/Library/RubyMotion/lib` anytime you use the `require` method in a Ruby file.

The line below it—third line—wouldn't work at all without the second line:

`require 'motion/project'`

### What is AppDelegate?

`AppDelegate` is class -- the *default* `delegate_class` set in a vanilla RubyMotion project's config. You can override this default value with whatever you want, but "AppDelegate" is the convention.

An application delegate is the first thing to recieve control from the operating system. It only has to implement the `application:didFinishLaunchingWithOptions` method.


