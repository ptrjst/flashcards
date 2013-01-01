# JavaScript: The Good Parts

### There are two ways to comment code—what are they, which one is bad, and why?

Two ways to comment:

1. `/* */`
2. `//`

`/* */` is bad because it's not safe for commenting out code blocks. JavaScript is likely to contain regular expression literals, which uses the same symbols.

    /*
      var rm_a = /a*/.match(s);
    */

Use `//` exclusively.

### How many different number types does JavaScript have?

Only a single number type -- a 64-bit floating point, same as Java's double. 

1 and 1.0 are the same value.

### What is `NaN`?

`NaN` is a number value that is the result of an operation that cannot produce a normal result.

`NaN` is not equal to any value, including itself.

You can detect `NaN` with the `isNan(number)` function.