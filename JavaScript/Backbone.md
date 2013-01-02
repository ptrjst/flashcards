Backbone.js
===========

Backbone is a lightweight JavaScript library created by Jeremy Ashkenas for developing single-page web applications.

From the project's website:

> Backbone.js gives structure to web applications by providing models with key-value binding and custom events, collections with a rich API of enumerable functions, views with declarative event handling, and connects it all to your existing API over a RESTful JSON interface.

### Who is the creator of Backbone.js?

Backbone was created by Jeremy Ashkenas, who is also known for CoffeeScript and Underscore.js.

### What is the Wikipedia definition of Backbone.js?

Backbone is a JavaScript framework/API with a RESTful JSON interface, and is loosely based on the Model-View-Controller application design paradigm. Backbone is known for being lightweight, as its only dependency is on one JavaScript library. It is designed for developing single-page web applications, and for keeping various parts of web applications (e.g. multiple clients and the server) synchronized.

### What is the official Backbone.js elevator statement?

Backbone.js gives structure to web applications by providing models with key-value binding and custom events, collections with a rich API of enumerable functions, views with declarative event handling, and connects it all to your existing API over a RESTful JSON interface.

### Name the seven most popular Backbone.js apps.

1. BitTorrent.com
2. Diaspora
3. DocumentCloud
4. Groupon Now
5. LinkedIn Mobile
6. Pandora Radio
7. Trello

### What are the three pillars of a Backbone.js app?

1. Modal
2. View
3. Router

### What are the five main objects in Backbone.js?

1. `Backbone.Collection`
2. `Backbone.Model`
3. `Backbone.Controller`
4. `Backbone.View`
5. `Backbone.Events`

### Can jQuery, Underscore, and Backbone be loaded asynchronous—at the same time?

No. Unfortunatly, these libraries must be loaded synchronously because they depend on each other existing in the global namespace.

1. Modernizr
2. jQuery
3. Underscore
4. Backbone
5. Your Application

### How does Backbone's architecture map to Ruby's architecture?

<table>
  <tr>
    <th>Purpose</th>
    <th>Backbone.js</th>
    <th>Rails</th>
  </tr>
  <tr>
    <td>Business data and logic</td>
    <td>Models and Collections</td>
    <td>Models</td>
  </tr>
  <tr>
    <td>Handles view events</td>
    <td>Views and Routers</td>
    <td>Controllers</td>
  </tr>
  <tr>
    <td>Renders the DOM</td>
    <td>Templates</td>
    <td>Views</td>
  </tr>    
</table>

### Where does the HTML markup live in a Backbone app? What about in a Rails app?

In Rails, HTML goes in a View. Backbone has Views, too—but that's not where the HTML goes. In Backbone, HTML goes in a Template. The View in Backbone is all JavaScript. It's more like a Rails Controller.

### What is Eco?

Referes to *.eco files for the Eco templating engine. It behaves similar to ERB (you can use ERB tags) but it's just Coffeescript. Commonly used in Backbone on Rails apps.

### What is Underscore.js?

Underscore is the tie to go along with jQuery's tux, and Backbone's suspenders.

### What are the pros and cons of using Backbone?

Pros:

- Highly flexible. You can choose not to implement some features (e.g Controller) based on your requirement.
- It is tightly integrated with underscore.js which is great.
- Initially you have to write more JavaScript code but it's very easy to implement complex user interaction.

Cons:

- Designed more towards consuming REST data.
- More complex initially if compared to knockout.js.

### How is Backbone lightweight?

- Less than 700 lines of JavaScript.
- Easy to read in an hour.
- Focused functionality.
- No UI widgets.
- Template agnostic.
- Use the HTML & CSS you already know.


### What does a `Backbone.Model` object do?

- Store data
- Provide get/set accessors
- Fire events when modified
- Optionally make REST calls to a server for persistence

### When do you capitalize a model object?

Let's say you have a model for albums.

    window.Album = Backbone.Model.extend({});

You'd capitalize "Album" as a convention, just to show that it is an abstract object that doesn't store data directly, but will be used to create other new Album objects with their own data.

### What are the four most common `Backbone.Model` methods?

1. get(key)
2. set({key:value})

1 & 2 modify attributes.

3. isNew()

Returns true if model is not persistent (has not been saved).

4. toJSON()

Returns attribute keys and values, ready for serialization.

### What does a `Backbone.View` object do?

- Display data and UI controls
- Render data with a template
- React to model changes
- Act on user input

### What are the three common render tasks for a `Backbone.View`?

1. Combine template and data

Use the model's data with an existing HTML template, often setup in the View's initialize() method.

2. Append to the DOM

Append, insert, or otherwise augment the existing HTML document with the newly rendered template output.

3. Return `this`

So other methods can be called.

### What special root properties ("options") do `Backbone.View` objects have?

- this.model
- this.collection
- this.el
- this.id
- this.className
- this.tagName

### What is `el`?

The overall DOM element represented by a view.

## What are the DOM properties you can override in a view?

- `id` - Manually set the unique identifier for the current element.
- `tagName` - Set the HTML tag: div, li, span, etc.
- `className` - Set the CSS class. For styling.
- `el` - The overall DOM element represented by a view.

### What are the model change events?

`set({a:'b'})` → `change` & `change:a`

Two events are triggered. Views can re-render themselves.

### What does it mean for Backbone to be "data-driven"?

Backbone applications are built around data. You'll drive behavior by changing model data rather than manipulating views directly.

Views will react to user actions by modifying data and letting the changes events cascade down (sometimes back to the same view).

### What is `bindAll`?

    initialize: function() {
      _.bindAll(this, 'render');
      this.template = _.template($('#album-template').html());
    }
    
`bindAll(obj, methods)` Permanently associates methods with a specific object. Most of your Backbone Views will need to start out with this line.

### What's the typical routine of a `Backbone.Model`?

- **Models store data**<br>
  Persistent or temporary.
- **Views render model data**<br>
  Using templates or directly.
- **Models trigger change events**<br>
  Handled by the framework when you call `set`.
- **Views observe and re-render**<br>
  The UI is updated instantly. 

### What does a `Backbone.Collection` object do?

- Fetch model data
- Add to existing set
- Remove from set
- Your custom query code

Are kinda like class methods in ActiveRecord.

### Backbone models have the `urlRoot` property while Backbone collections have the `url` property. What's the difference between these two?

Both `urlRoot` and `url` specify the base for the server-side JSON API that houses the resource. If you use one, there's usually no need to set the other.

Setting the model's `urlRoot` property:

    var Task = Backbone.Model.extend({ 
      urlRoot: '/tasks'
    });
    
    var Tasks = Backbone.Collection.extend({ 
      model: Task
    });

Setting the collection's `url` property:

    var Tasks = Backbone.Collection.extend({ 
      model: Task,
      url: '/tasks'
    });
    
    var Task = Backbone.Model.extend({});

If we specify the URL for Tasks in our collection instead, then models within the collection will use the collection’s URL to construct their own URLs, and the urlRoot no longer needs to be specified in the model. If we make that change, then our collection and model will be as follows.

### What are the Underscore.js methods for Collections?

`each`, `map`, `select`, `reject`, `pluck`, `max`, `min`, `sortBy`, `size`

### What are the Underscore.js methods for Arrays?

`first`, `rest`, `last`, `compact`, `flatten`, `without`, `union`, `intersection`, `uniq`, `indexOf`, `range`

### What are the Underscore.js methods for Functions?

`bind`, `bindAll`, `memoize`, `delay`, `defer`, `throttle`, `once`, `after`, `wrap`

### What is an shorter way to write `albums.map(function (album) { return album.get('title') })`?

`albums.pluck('title')`

### What are the Collection events?

1. `add`
2. `remove`
3. `reset`

### Can Backbone have nested views?

Yes. Views have other views inside them. Individual subviews can update their content at any time without affecting the other views.

A Collection-backed view operates this way -- each item in the collection is rendered by its own view.

### Convention: What do jQuery objects look like?

They always begin with a dollar sign: `$albums`.

### Does a view automatically insert itself into the DOM?

No. You have to do it.

    $albums.append(view.render().el);
    
### What does "render on data" mean?

**Render when data arrives.** It happens asynchronously, so you can't guarantee that the data will be there at any specific time. React to the arrival of data.

**May fire several times.** The render method will be called at least twice, and maybe many more times. Clear out the existing HTML so content isn't duplicated.

### What are the two ways to load data in Backbone?

1. **Network** - Load data from the server with a network request for JSON data. Fires the 'reset' event when done.

    Albums.fetch()
    
2. **Preload** - Call 'reset' directly with an array of key/value objects. Fires the 'reset' event when done.

    Albums.reset([{ title: '...' }])
    
### What are the three key parts of a router?

1. **routes** - Keys and values mapping URLs to custom route handler methods.

2. **initialize** - Setup root views, but don't render or append to the document.

3. **Custom Route Handlers** - Add specific views to the document and load extra data (such as a specific date specified in the URL).

### What are the two differeny ways Backbone routers handle URLs?

1. **Hashmark** - This is the default.

    Backbone.history.start();

2. **Push State** - This is optional, uses traditional-style URLs.

    Backbone.history.start({ pushState: true });
    
### How do you navigate in the console?

Where `App` is an object that extends `Backbone.Router`, to navigate to `http://yourapp.dev/#albums`:

    App.navigate('albums', true)

## Further reading

- http://addyosmani.com/resources/essentialjsdesignpatterns/book/
- http://dublintech.blogspot.com/2012/04/javascript-language-z-cheat-sheet.html
