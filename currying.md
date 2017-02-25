# Currying
Currying is a technique for evaluating a function that takes multiple arguments by breaking it down into a sequence of functions that each take a single argument. Each function in the sequence returns another function with the previous function's argument applied. When the sequence reaches its end, the last function returns the desired value. In this way, a curry chain breaks down a function by each argument.

## Example

### Without Currying
function multiply (a, b) { <br>
&nbsp;&nbsp;&nbsp;&nbsp;return a * b;  <br>
} <br>
multiply(2, 5) //=> 10

### With Currying
function multiply (a) { <br>
&nbsp;&nbsp;&nbsp;&nbsp;return function(b) { <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;return a * b; <br>
&nbsp;&nbsp;&nbsp;&nbsp;} <br>
} <br>
multiply(2)(5) //=> 10

### Use Case
var double = multiply(2); <br>
double(5) //=> 10 <br>