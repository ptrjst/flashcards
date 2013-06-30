### What is the application delegate?

The `AppDelegate` is the entry point for your app.

### What are the basic callback methods for `AppDelegate`?

`UIApplication` asks the `AppDelegate` to respond to the following lifecycle events:

- `application:didFinishLaunchingWithOptions:`
- `applicationDidBecomeActive:`
- `applicationWillResignActive:
- `applicationDidEnterBackground:`
- `applicationWillEnterForeground:`
- `applicationWillTerminate`

### What are the basic callback methods for `UIViewController`?

- `loadView`
- `viewDidLoad`
- `viewDidUnload`
- `viewWillAppear:`
- `viewDidAppear:`
- `shouldAutorotateToInterfaceOrientation:`
- `didReceiveMemoryWarning`

### What is the most obvious example of a feature that Ruby Motion adds to the Ruby language, that is not there by default?

The `didFinishLaunchingWithOptions:launchOptions` is the perfect example. It's using a named parameter syntax way for calling methods that Objective-C uses.

```ruby
class AppDelegate
  def application(application, didFinishLaunchingWithOptions:launchOptions)
    true
  end
end
```

### How do you create a simple alert?

```ruby
alert = UIAlertView.new
alert.message = "Hello!"
alert.show
```

### What is the `loadView` callback on `UIViewController` for?

You define a `loadView` method to get the view for the controller—which happens when the view hasn't already been set. You do this by setting the view property of the controller to an instance of some view.

### In iOS, all views are subclasses of what?

`UIView`

### When do you use `foo.init` vs. `foo.alloc.init`?

Let me Google that for you:

https://groups.google.com/forum/?fromgroups=#!topic/rubymotion/RPxKXMfcGGs

### What does the Rakefile do?

It defines all of the project-level configuration.

### How do you set the application's icon?

Open the `Rakefile` and add:

```ruby
Motion::Project::App.setup do |app|
  app.name = 'Quartermaster'
  app.icons << 'icon.png'
end
```

### Which Terminal command prints out your application's configuration information?

`rake config`

### Which Terminal command cleans out your simulator sandbox?

`rake clean`

### Which Terminal command cleans then runs your app?

`rake clean=1`






# Ruby Motion REPL Exercises

One of the killer things about Ruby Motion is the REPL. You can build an entire app through it. It's one of the easiest ways to interactively prototype-out an app. That is, if you know how to use it.

It's also killer for debugging -- you can grab objects from your app at runtime and begin manipulating them directly from the console.

This deck will give you challenges (katas?) to help you level-up your Ruby Motion REPL skills.

### What is `main`?

From the REPL, `main` is a global instance of the class `TopLevel`, which inherits from `NSObject`.

    (main)> self.methods(false)
    => [:"repl:", :quit, :help, :sessions]
    
or
    
    (main)> methods false
    => [:"repl:", :quit, :help, :sessions]

### What ⌘+Clicking a UI element in the simulator do?

It captures the UI element in the REPL, creating a new session, making it the contextual object.

### What does the REPL command `sessions` do?

It returns the current session object. This lists the currently running sessions.

It you run `quit` from here and you'll bounce out to `main`, the top running sessions.

### What is `UIApplication`?

From the REPL you can say:

    (main)> app = UIApplication.sharedApplication
    => #<UIApplication:0x954c400>

Remember, your application delegate (`AppDelegate`) is set as the delegate of the `UIApplication`. So, if you look at the delegate property:

    (main)> app.delegate
    => #<AppDelegate:0x9550600 @window=#<UIWindow:0xa970f00>>
    
For example, here there's an `@window` instance variable—your app may be different.

### How do you change the contextual object of the REPL?

By using the `repl` command, you create a new session whose focused is the object you pass in as a parameter.

    (main)> sessions
    => [main]
    (main)> repl(app.delegate)
    => #<AppDelegate:0x9550600 @window=#<UIWindow:0xa970f00>>
    (#<AppDelegate:0x9550600 @windo...)> sessions
    => [main, #<AppDelegate:0x9550600 @window=#<UIWindow:0xa970f00>>]
    (#<AppDelegate:0x9550600 @windo...)> @window
    => #<UIWindow:0xa970f00>
    (#<AppDelegate:0x9550600 @windo...)> 

Notice that we have easy access to the object's instance variables—such as `@window`, in this case—because this is the context we're in.

### How do you switch between open sessions?

The `sessions` object is an array, so you can access each session using the index bracket syntax, and pass that into the `repl` command:

    (#<UIImageView:0x9357e00>)> sessions
    => [main, #<AppDelegate:0x9550600 @window=#<UIWindow:0xa970f00>>, #<UIImageView:0x9357e00>]
    (#<UIImageView:0x9357e00>)> sessions[1]
    => #<AppDelegate:0x9550600 @window=#<UIWindow:0xa970f00>>
    (#<UIImageView:0x9357e00>)> repl(sessions[1])
    => #<AppDelegate:0x9550600 @window=#<UIWindow:0xa970f00>>
    (#<AppDelegate:0x9550600 @windo...)> 

### What does this message mean: "Application windows are expected to have a root view controller at the end of application launch"?

It means your app instantiated a `UIWindow` without setting the `rootViewController` property to an instance of `UIViewController`.

You need to do something like this:

    class AppDelegate
      def application(application, didFinishLaunchingWithOptions:launchOptions)
        @window = UIWindow.alloc.initWithFrame(UIScreen.mainScreen.bounds)
        @window.rootViewController = MySuperViewController.alloc.init
        @window.makeKeyAndVisible
        true
      end
    end
    
