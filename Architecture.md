Software Architecture and Design Patterns
=========================================

This deck will walk you through the basics of software architecture and design.

### abstraction

refers to the grouping of data (and the operations on that data) into one entity

### encapsulation

refers to the separation of external aspects of an object from the internal implementation details of the object

### Ways to achieve polymorphism

- method overloading
- operator overloading
- method over-riding

### OCP

The Open Closed Principle by Bertrand Meyer

You should be able to extend a class's behavior without modifying it.

A module should be open for extension, but closed for modification.

### LSP

The Liskov Substitution Principle

Derived classes must be substitutable for their base classes.

### DIP

The Dependency Inversion Principle

Depend on abstractions. Not on concretions.

### ISP

The Interface Segregation Principle

Make fine-grained interfaces that are client specific.

### REP

The Reuse Release Equivalency Principle

### CCP

The Common Closure Principle

### CRP

The Common Reuse Principle

### ADP

The Acyclic Dependencies Principle

### SDP

The Stable Dependencies Principle

### SAP

The Single Abstractions Principle

### SRP

The Single Responsibility Principle

A class should have one—and only one—reason to change.

### The Singleton Pattern requires one instance of a class. How do you impose this condition?

It must have a class variable that is a reference to its single instance.

### The Four Main Object Oriented Concepts

Also known as The Four Object-Oriented Gods:

1. Encapsulation
2, Abstraction
3. Inheritance
4. Polymorphism

### UML notation for associations

- ―――◆  Composition
- ―――>  Association
- ---▷ Inheritance
- ―――▷ Realize/Implement
- --->  Dependency
- ―――◇  Aggregation

### Do state diagrams help you in defining your data model?

No.

A state diagram helps in the design of the dynamic model. Class hierarchy diagrams help in the design of the data model.


