# JavaScript

### What are the three core global objects?

`Date`, `Math`, and `JSON`

### What are the top level functions for converting strings to numbers?

`parseFloat(string, radix)`

`parseInt(string, radix)`

Radix is base 2, base 10, base 16, etc. This is optional. The default value is 10. That said, you should *always* supply this argument. JavaScript does some funny conversions from strings to ints, sometimes.

### Does JavaScript have classes?

No. JavaScript is classless, but classes can be simulated using functions.

    function Person() {
      this.publicMember = "foo";
      this.privilegedMethod = function() { return privateMethod(); }
      var privateMember = "bar";
      function privateMethod() { return "hello"; 	}
    }

### What does the error "can't serialize, infinite loop" mean?

This means you tried to serialize a hierarchical data structure into JSON. Probably using `JSON.parse()` or `JSON.stringify()`.

The solution to this problem is found in the concept of "deep copy"—you make a copy of an object and changes in the copy are reflected in the original. There's a jQuery function for this: `jQuery.clone()`.

### How do you perform a GET or POST request to a remote URL?

    XMLHttpRequest
    jQuery.ajax(url, callback)
    jQuery.get()
    jQuery.post()
    
### What's the difference between `undefined` and `null`?

`undefined` is where no notion of the thing exists: no type and has never been reference before in the scope.

`null` is where the thing is known to exist, but it's not known what the value is. `null` is an object whose type is `null`—a special value meaning "no value".

### What's the difference between double and triple equals?

Double equal (==) checks value which triple (===) checks both value and type.

    1 == "1" // true
    1 === "1" // false (checks type too)
    1 === 1.0 // true (all just numbers)
    new String("a") == new String("a") // false
    new String("a").valueOf() == new String("a").valueOf() // true
    
### What are the two ways to set properties in JavaScript?

1. dot syntax

    person.gender

2. bracket syntax

    person["gender"]

### How many ways are there for creating objects?

Four ways to create objects.

    var newObject = {};
    var newObject = Object.create(null);
    var newObject = new Object(); // constructor function
    
    // and with a closure
    var counter = function(count) {
      console.log(">> setting count to " + this.count);
      return {
        getCount: function() {
          return ++count;
        }
      }
    }
    mycounterWithOffset = counter(10);
    console.log(mycounterWithOffset.getCount());  // outputs 11

The convention is that constructor functions should begin with a capital letter. Note: if the new keyword is not used, then the 'this' variable inside the function will refer to the global object. Can you smell a potential mess? Hence why the capital letter convention for constructor functions is used. The capital letter means: "I am a constructor function, please use the new keyword".

### Developers are always frustrated with DOM methods. What's the deal with that?

DOM methods are nightmares: getElementById, getElementsByTagName (riddled with IE bugs - .length gets overwritten in IE if an element with an ID="length" is found). John Resig gave a great talk called The DOM Is a Mess. If there's a DOM method, there's probably a problem with it somewhere, in some capacity.

