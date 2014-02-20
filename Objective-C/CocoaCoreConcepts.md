Cocoa Core Competencies
=======================

MVC
---

### What does MVC stand for?

Model-View-Controller

From the [iOS Developer Library](https://developer.apple.com/library/ios/documentation/General/Conceptual/DevPedia-CocoaCore/MVC.html):

> The Model-View-Controller (MVC) design pattern assigns objects in an application one of three roles: model, view, or controller. The pattern defines not only the roles objects play in the application, it defines the way objects communicate with each other. Each of the three types of objects is separated from the others by abstract boundaries and communicates with objects of the other types across those boundaries. The collection of objects of a certain MVC type in an application is sometimes referred to as a layer—for example, model layer.

### What does a model do?

A model defines what your application is, but not how it is displayed.

### What does a controller do?

A controller defines how your model is presented to the user. This is where the UI logic goes.

### What does a view do?

A view is a generic UI element that is used by the controller.

### How does the communication work in MVC?

- Controllers can talk directly to models via their public APIs.
- Controllers can talk directly to views (outlet).
- Models and views can never talk to each other.
- Models can not talk to either the controller or view, but they can broadcast via Notification and KVO.

### Can views talk to controllers?

Yes, but it's very structured, using target-action. View sends an action to a Controller's target. The controller sets itself as the view's delegate (remember "will", "did", "should"). Controllers is the "data source" for the view (remember "data", "at", "count").

Resources
---------

iOS Developer Library - Apple

http://cs193p.stanford.edu
