#Generators

##What are they?
* Generators are a new kind of function available in ES6.
  * They are declared with `function*(...) { ... }` - note the extra asterisk.

* A generator returns a function that can be paused in its execution. In other words, the generated function **does not run to completion**, i.e. does not need to finish running before other code can run.

* A generator includes `yield` statement(s) in its body. These pause the execution of the generated function and indicate what value to return at that time.

* The generated function has a `next` method that continues the execution of the function until the next `yield` statement and returns an object containing two keys:
  * `value`: The value of the `yield` statement
  * `done`: Indicates if the generated function has run to completion. This will be `false` if there is more code to run.

* The generated function conforms to both the iterable protocol and [iterator](iterators) protocol.

##Examples
```javascript
// generator
const threeToFive = function*() {
  yield 3;
  yield 4;
  yield 5;
};

// generated function
const threeFive = threeToFive();

console.log(threeFive.next()) // { value: 3, done: false }
console.log(threeFive.next().value) // 4
console.log(threeFive.next().value) // 5

// generator
const numGen = function*(start) {
  while(true) {
    yield start++
  }
};

// generated function
const counter = numGen(5);

console.log(counter.next().value); // 5
console.log(counter.next().value); // 6
console.log(counter.next().value); // 7
console.log(counter.next().value); // 8
```

##Useful resources
* https://davidwalsh.name/es6-generators
* https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Generator