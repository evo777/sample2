### What is it?
* Hoisting occurs when __function__ and __variable__ **declarations** are moved to the top of the scope; either the function scope or to the global scope.
* This happens before any of your own code is executed.
* Functions are hoisted first, then variables.
* When you conduct static analysis, imagine functions and variables within a containing scope being moved to the top.

#### Clarification of function and variable declarations

* For function declarations, this includes the function body, so the function will be defined anywhere inside that scope.
* For variable declarations, this does NOT include the initialization of its value, so the variable will be `undefined` until the first line of code where you actually assign it a value.
* This is why it matters how you define your functions. **These two will hoist differently:**
  * Function declaration style: `function myFunc() { ... }`
  * Variable declaration style: `var myFunc = function() { ... };`

### Clarifications for ES6
In ES6, variables and functions are hoisted as explained above. However, `let` and `const` declarations, though hoisted, will not be initialized with a value of `undefined`. As such, trying to access a `let` or `const` variable before it has been declared in the code will throw a `ReferenceError`. For example:

Using var below does not result in an error
```javascript
console.log(name); // undefined
var name = 'Bob';
```

If const or let is used instead, a reference error will be thrown:
```javascript
console.log(name); // ReferenceError: name is not defined
let name = 'Bob';
```


### How is it used?
> An example of **hoisting** is as follows:

##### Variable Hoisting
```
herp = 'Wow, this is cool!';

var herp;

console.log(herp); // 'Wow, this is cool!'
```

##### Function Hoisting
```
derp();

function derp() {
  console.log('Wow, this is cool!');
};

// 'Wow, this is cool!'
```

> If within the scope, a _function_ and/or a _variable_ can be used before it has been declared.