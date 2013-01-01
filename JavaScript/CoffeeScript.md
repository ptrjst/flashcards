### Convert the following JavaScript to CoffeeScript:

    CreditCard =
      cleanNumber: (number) ->
        number.replace /[- ]/g, ""
    
### Covert the following CoffeeScript to JavaScript:    
    
    var CreditCard =
      cleanNumber: function(number) {
        return number.replace(/[- ]/g, "");
      }

---------------------------------------

### JavaScript:

    var number;
    for (number = 1; number <= 3; number++) {
      alert(number);
    }

### CoffeeScript:

    for number in [1..3]
      alert number

---------------------------------------

### JavaScript

    $(function() {
      alert "We're in jQuery.";
    });

### CoffeeScript

    $ ->
      alert "We're in jQuery."
    
    jQuery ->
      alert "We're in jQuery."