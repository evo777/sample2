# ES6 Arrow Functions

## What are they?

ES6 arrow functions make use of 'fat arrows'. See an example of a 'traditional' function converted to an arrow function below:
```javascript
// 'Traditional' function
var add = function(a, b) {
  return a + b;
};
// Arrow function
var add = (a, b) => {
  return a + b;
}
```
## Special properties of arrow functions
### Lexical this binding
The `this` binding of the function is determined by where it is defined, not where it is used.
In addition, the this binding of arrow functions cannot be changed.

This property has some interesting consequences. For example, it can cause issues with pseudoclassical instantiation:

When using a traditional function to define the methods, we see no issues...
```javascript
const Human = function(age) {
	this.age = age;
};
Human.prototype.getAge = function () {
	console.log(this.age);
}

const me = new Human(27);
me.getAge(); // 27
```
However, when using an arrow function, the `getAge` method will log undefined...
```javascript
const Human = function(age) {
	this.age = age;
};
Human.prototype.getAge = () => {
	console.log(this.age); 
}
const me = new Human(27);
me.getAge(); // undefined
```
### No `new`able
Arrow functions cannot be used as constructors and will throw an error if the `new` keyword is used
### Implicit return value
If an arrow function contains a single expression, then omitting the `{` and `}` will cause it to return the evaluation of that expression.

For example, the 3 functions below will all return the same value:
```javascript
// Traditional function
var addTraditional = function(a, b) {
  return a + b;
};
// Arrow function
var addArrow = (a, b) => {
  return a + b;
};
// Arrow function with implicit return
var addArrowImplicit = (a, b) => a + b // Note how there is not return statement
```


