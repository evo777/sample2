Namespacing is a practice used to to prevent collisions with other objects, functions and variables. It helps protect your code and third-party code from breaking in the event you are using the same name as another developer and it helps make your code more modular & organized.

Common interweaving techniques followed by examples:

* Single global variables
* Object literal notation
* Checking for code collisions
* Nested namespacing
* Immediately invoked function expressions
* Namespace injection

### Single global variables
```
var application =  (function(){
        function(){
            /*...*/
        },
        return{
            /*...*/
        }
})();
```
Single global variables still run into the problem of potentially using a name used by other developers. Generally ok for smaller to mid sized applications but larger applications will likely require another approach.

### Object Literal Notation
Object literal notation is one spin on creating a single global variable
```
var myApp = {
 
    id: 0,
 
    next: function() {
        return this.id++;   
    },
 
    reset: function() {
        this.id = 0;    
    }
}
window.console && console.log(
    myApp.next(),
    myApp.next(),
    myApp.reset(),
    myApp.next()
) //0, 1, undefined, 0

```

### Checking for code collisions
It is generally considered a good practice to check for variable collisions. Here is an example with an obj:
```
myApplication || (myApplication = {});
```

### Nested namespacing
Nesting objects can lower the probability of a collision. Yahoo uses this practice regularly.
```
YAHOO.util.Dom.getElementsByClassName('test');
```

Nested namespacing comes at the cost of extra lookups but the performance cost seems to be negligible.

### Immediately invoked function expressions
An immediately function is function that is defined and immediately invoked.

A common practice involves passing in a namespace object as an argument to the invocation and assigning public methods to it. Private methods can also be used to leverage closure.

```
var namespace = namespace || {};

// here a namespace object is passed as a function
// parameter, where we assign public methods and
// properties to it
(function( o ){
    o.foo = "foo";
    o.bar = function(){
        return "bar";
    };
})(namespace);

console.log(namespace);

```


### Namespace injection
Namespace injection generally follows a similar pattern to the IIFE except instead of directly passing in an object and referring to that object throughout, *this* is used.

```
(function() {
    var val = 5;

    this.getValue = function() {
        return val;
    };

    this.setValue = function(newVal) {
        val = newVal;
    }

    // also introduce a new sub-namespace
    this.tools = {};

}).apply(myApp.utils);

```



*Code was liberally borrowed from [Addy Osmani's coverage on namespacing](https://addyosmani.com/blog/essential-js-namespacing/#beginners)*