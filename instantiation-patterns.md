There are four instantiation patterns in JavaScript (ES5). With ES6, we get a fifth pattern, i.e. actual classes.

Jump to:
* [Overview](#overview)
* [Sample code](#sample-code)

## Overview
### Functional
* Methods are defined for each instance
* Because this is the only pattern where each instance gets its own freshly defined functions, it has two unique points:
  * the `this` keyword is never needed
  * **instance variables can be made private**: methods can access them directly via closure, so they do not need to be added as properties on the instance object itself!

### Functional-shared
* Methods are defined in one object and added to each instance using `extend`
* Because `extend` is an one-time copy of properties from one object to another, modifications to the methods object will NOT affect existing instances

### Prototypal
* Methods are defined in one object and set as the `__proto__` object for each instance
* Because of how property lookup falls through to the previous object in the prototype chain, modifications to the methods object WILL affect existing instances

### Pseudoclassical
* Methods are defined in one object and set as the `__proto__` object for each instance
* Specifically, the object must be the `Constructor.prototype` object
* Because of how property lookup falls through to the previous object in the prototype chain, modifications to the methods object WILL affect existing instances
* The `new` keyword must be used when creating new instances

### Classes
These are available only in ES6, which finally adds formal classes to JavaScript.
* Instance variables are defined in the `constructor` function inside the class
* Methods are defined in the class and are shared by all instances
* The `new` keyword must be used when creating new instances

## Sample code

### Functional
```
var Car = function() {
  var car = {};
  var color = 'blue'; // note this variable doesn't need to be added to car
                      // but it could be, if desired
  car.changeColor = function(newColor) {
    color = newColor;
  };
  return car;
};

var myCar = Car();
```

### Functional-shared
```
var Car = function() {
  var car = {
    color: 'blue'
  };
  _.extend(car, carMethods);
  return car;
};

var carMethods = {
  changeColor: function(newColor) {
    this.color = newColor;
  }
};

var myCar = Car();
```

### Prototypal
```
var Car = function() {
  var car = Object.create(carMethods);
  car.color = 'blue';
  return car;
};

var carMethods = {
  changeColor: function(newColor) {
    this.color = newColor;
  }
};

var myCar = Car();
```

### Pseudoclassical
```
var Car = function() {
  this.color = 'blue';
};

Car.prototype = {
  changeColor: function(newColor) {
    this.color = newColor;
  }
};

var myCar = new Car();
```

### Classes

Remember that this is available only starting with ES6.

```
class Car {
  constructor() {
    this.color = 'blue';
  }
  changeColor(newColor) {
    this.color = newColor;
  }
}

var myCar = new Car();
```