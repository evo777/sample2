## What is Functional Programming
Functional programming is one of the primary programming paradigms in JavaScript (OOP or Object Oriented Programming being the other). It is the idea of writing code with relatively small, composable functions. It does this by keeping functions pure (i.e. produces no side effects and given the same input will always return the same output).

## How it works
The features in JavaScript that make functional programming possible are closures, higher order functions, and the fact that functions are just another type of object (and so can be passed around like other objects can).

The following is an example of functional programming using currying:

``` 
var add = function(x) {
  return function(y) {
    return x + y;
  };
};

var increment = add(1);
var addTen = add(10);

increment(2);
// 3

addTen(2);
// 12
```
In the above example, we are _composing_ new functions using the self-explanatory 'add' function. With it, we can create any number of different _add_ based functions. Since it is a pure function, without side-effects, given any input, we always know what output to expect.

## Functional Programming vs. Object Oriented Programming (OOP)
Functional programming is generally thought of as a more declarative pattern (telling the computer _how_ you want something to happen) as opposed to OOP which is imperative (telling the computer _what_ you want to happen). A discussion of pros and cons though generally comes down to personal preference as it can come down to what a developer is used to using. Because many popular languages make heavy use of OOP, the OOP patterns in JS were more familiar to developers coming from those languages. Some believe that OOP code can be harder to scale and maintain since, as a code base becomes larger, the side-effects on classes are harder to track down. Functional meanwhile can have a steeper learning curve because of its roots in lambda mathematics and comparative lack of instructional resources.

## Other examples of Functional Programming Languages
Lisp, ML, Haskell, Erlang, Clojure, Elm, F Sharp, OCaml

## Useful Resources
*  [ 10 Interview Questions Every JavaScript Developer Should Know](https://medium.com/javascript-scene/10-interview-questions-every-javascript-developer-should-know-6fa6bdf5ad95#.k0neqmgv6)
*  [What is a Pure Function](https://medium.com/javascript-scene/master-the-javascript-interview-what-is-a-pure-function-d1c076bec976#.qnqy6qnuq)