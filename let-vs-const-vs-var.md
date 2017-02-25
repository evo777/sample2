* `var` is function scoped
* `let` is block scoped
* `const` is also block scoped, but its value cannot be reassigned
  * Note that you can *modify* its value, e.g. if the value has been set to an array or object:
  ```
  const obj = {};
  obj.newProperty = 'newValue'; // this is fine
  obj = 5; // this will throw an error
  ```

## Hoisting for let and const
While `let` and `const` are hoisted like `var`, the interpreter does not automatically initialize them with a value of `undefined`. As such, in order to avoid errors, `let` and `const` variables should be declared before they are used.

For example, the below will result in an error 
```javascript
console.log(greeting); // ReferenceError: greeting is not defined
let greeting = 'hello';
```

However, there will be no error if `var` is used
```javascript
console.log(greeting); // undefined
var greeting = 'hello';
```