###What is destructuring?

In short, it is ES6 syntactic sugar for accessing and assigning variables using arrays and objects.

##Examples
Destructuring can be used to access specific elements with arrays or specific keys within objects
```javascript
const arr = [1, 2, 3, 4];
const obj = {
  one: 1,
  two: 2,
  three: 3,
  four: 4
};

// destructuring from array
const [a, b, ...rest] = arr;
console.log(a); // 1
console.log(b); // 2
console.log(rest); // [3, 4];

// destructuring from object
const { two, four } = obj;
console.log(two); // 2
console.log(four); // 4

// destructuring can also be used to swap variable
let one = 1;
let two = 2;
[one, two] = [two, one];
console.log(one); // 2
console.log(two); // 1

// new variable names can be assigned when destructuring an object
const fooBar = {
  foo: 1,
  bar: 2,
}
const { foo: one, bar: two } = fooBar;
console.log(one); // 1
console.log(two); // 2

// destructuring also works for nested arrays/objects
const fooBar = {
  foo: { one: 1, two: 2, three: 3 },
  bar: [4, 5, 6],
};
const { foo: { one, two, three }, bar: [four, five, six] } = fooBar;

console.log(one); // 1
console.log(two); // 2
console.log(three); // 3
console.log(four); // 4
console.log(five); // 5
console.log(six); // 6
```

###Docs
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment