# ES6 Classes
## What is it?
- JavaScript classes are introduced in ECMAScript 6 and are syntactical sugar over JavaScript's existing prototype-based inheritance. 
- ES6 classes function similarly to pseudoclassical instantiation. However, unlike functions, classes are not hoisted and most be declared before they are used.
- Classes can be defined using `class` declarations or `class` expressions.
- The `constructor` method in the class is used to create and initialize the object.
- The `super` method can be used to call the constructor of a parent class.

## Example
``` javascript
class Vehicle {
	constructor(color) {
		this.color = color;
	}
}

class Car extends Vehicle {
	constructor(color, type) {
		super(color);
		this.type = type;
	}
	
	drive() {
		console.log('The ' + this.color + ' ' + this.type + ' is driving!');
	}
}
const myCar = new Car('red', 'BMW');
myCar.drive(); // The red BMW is driving!
```