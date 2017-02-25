# Bind

## What is it?
- Binds a specified `this` to the function which will be used when the function is called (irrespective of the context in which it is called)
- Can also be used to bind specific arguments to a function

```javascript
this.multiply = 5;
const multiplyObject = {
  multiply: 10,
};

const addMultiply = function(a, b) {
  return ( a + b ) * this.multiply;
}

addMultiply(3, 2) // 25

const addMultiplyTen = addMultiply.bind(multiplyObject); // binds the this value to multiplyObject
addMultiplyTen(3, 2) // 50

const addFiveMultiplyTen = addMultiply.bind(multiplyObject, 5) // binds the first argument to 5
addFiveMultiplyTen(5);
```

## Arrow functions
- Because the this binding of arrow functions is determined by their lexical scope (as opposed to being bound at call time), `bind` cannot be used with arrow functions to bind a `this` value. 
- However, `bind` can still be used to bind specific arguments. For example, see below:
```javascript
const add = (a, b) => a + b;
const addFive = add.bind(null, 5);
addFive(7); // 12
```