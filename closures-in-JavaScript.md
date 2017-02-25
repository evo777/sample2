A function retains **ongoing access** to all variables available in the **scope in which the function was created**.

### Ongoing access

This means you can get *and* set the variable's value. You can modify the value or even reassign it, and any future function calls that have access to that variable will see the updated value.

### Scope in which the function was created
Remember that in JavaScript, [scope](scope-in-JavaScript) is delineated only by function. So if you are looking at a line of code and want to figure out what scope you're in, you simply need to look for the innermost function body that encloses that line.

Now let's clarify what it means for a function to be "created":

* Usually you can just look for the place where you literally see its function definition, i.e. the whole `function() { ... }` thing.
```
var outerFunction = function() {
  // some stuff
  var innerFunction = function() { // this function was created inside outerFunction
    // some other stuff
  }
};
```

* However, the function could also be created by other means, e.g. as the result of another function call.
```
var functionCreator = function() {
  return function() {
    console.log('hi');
  };
};
var outerFunction = function() {
  // some stuff
  var innerFunction = functionCreator(); // this function was still created inside outerFunction
};
```