JavaScript only scopes by function. This is unlike many other languages that scope by any block, including function bodies but also `if` blocks, `for` loops, etc.

This means that within a function, there is a local scope. Any variables declared inside a function body are local to each call to that function and will be garbage-collected at some point after the function returns (unless it is the return value for the function).

## Changes in ES6
In ES6, let and const declarations are block-scoped and are not necessarily available everywhere inside of function. Examples of blocks include `if` blocks, `for` blocks, function blocks, etc. See below for some practical examples of block scope.

Variables declared with `var` are scoped by function.
```javascript
var logFive = function() {
  if (true) {
    var five = 5;
  }
  console.log(five); // Logs '5' to the console
}
```

Variables declared with `let` and `const` are block scoped.
```javascript
var logFive = function() {
  if (true) {
    let five = 5;
  }
  console.log(five); // Throws 'ReferenceError: five is not defined'
}
````