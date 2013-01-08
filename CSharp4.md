C# 4.0
======

This deck will bring you up-to-speed on the new C# features in the .NET Framework 4.

## Dynamic Binding

### What is dynamic typing?

A programming language is said to be **dynamically typed** when the majority of its type checking is performed at run-time as opposed to at compile-time. In dynamic typing values have types, but variables do not; that is, a variable can refer to a value of any type. Dynamically typed languages include JavaScript, Lisp, MATLAB, PHP, Python, and Ruby.

*Source: [Wikipedia - Type System](http://en.wikipedia.org/wiki/Type_system#Dynamic_typing)*

### What is static typing?

A programming language is said to use **static typing** when type checking is performed during compile-time as opposed to run-time. Statically typed languages include Java, C, Fortran, Go, and Objective-C.

*Source: [Wikipedia - Type System](http://en.wikipedia.org/wiki/Type_system#Static_typing)*

### Is C# a static or dynamic typed language?

Static

### What is the benefit of dynamic binding?

Dynamic binding allows you to write method, operator and indexer calls, property and field accesses, and even object invocations which bypass the C# static type checking and instead gets resolved at runtime.

### What is a drawback of dynamic binding?

Static typing is not enforced for operations.  A dynamic object is assumed at compile time to support any operation, and only at runtime will you get an error if it wasn’t so. 

### Explain the `dynamic type`.

`dynamic` is a static type that gets resolved at runtime.  

    dynamic d = GetDynamicObject(…);
    d.M(7);

The C# compiler allows you to call a method with any name and any arguments on d because it is of type dynamic. At runtime the actual object that d refers to will be examined to determine what it means to “call M with an int” on it.  

The type dynamic can be thought of as a special version of the type object, which signals that the object can be used dynamically. 

### What is an implicit conversion of a `dynamic` object?

    dynamic d = 7; // compile-time implicit conversion
    int i = d;     // runtime implicit conversion

### What is an explicit conversion of a `dynamic` object?

    dynamic d = 7;
    int i = (int)d; // compile-time implicit conversion

### What are the two scenarios where the result of a dynamic operation is not of type `dynamic`?

1. The type of a dynamic constructor call is the constructed type
2. The type of a dynamic implicit or explicit conversion is the target type of the conversion.

## Named and Optional Arguments

### What are optional parameters?

**Optional parameters** allow you to leave out arguments in method calls.

### What are named arguments?

**Named arguments** are a way to provide an argument using the name of the parameter instead of relying on its order in the parameter list.

### If you find yourself writing many overloads of a method with different combinations of parameters, what should you do instead?

Write a single method that uses optional parameters.

### What is the syntax for declaring an optional parameter for a method?

    int Foo(int x, int y = 1)
    {
      return x + y;
    }

### How would you call the method `Foo(int x, int y = 1)` passing the minimum number of required parameters?

    Foo(5);

### How would you call the method `Foo(int x, int y = 1)` overriding the default value of the second parameter to be 7?

    Foo(5, 7);

## Further reading

[New Features in C# 4.0 - Word Doc](http://code.msdn.microsoft.com/Visual-Studio-2010-Samples-31b491f3/file/46874/1/New%20features%20in%20CSharp%204.0.doc)

[New C# Features in the .NET Framework 4 - MSDN](http://msdn.microsoft.com/en-us/magazine/ff796223.aspx)
