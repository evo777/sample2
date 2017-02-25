### What is it?

* JavaScript is weakly typed, meaning that its interpreter will perform type coercion when an operand is not the expected type (e.g. string, number, Boolean, etc.).
* Specifically, the interpreter will convert the type of an operand to either match the type that a given operator expects, or the type of another operand, to evaluate an expression.
* Note that this type coercion does not actually affect the value of the operand itself - it is simply used to execute the evaluation.

This concept is relevant to all kinds of operators:
* arithmetic: `+`, `-`, `*`, `/`, etc.
* Boolean: `==`, `!=`, `&&`, `||`, `!`, etc.
* bitwise: `&`, `|`, `<<`, `>>`, `^`, etc.

#### Turning "off" type coercion

Use `===` and `!==` (in lieu of `==` and `!=`) to compare the equality/non-equality of two values **without** type coercion.

### Examples

```javascript
// when adding a string with a number (regardless of order), the result is coerced to a string
'1' + 2; // '12'
1 + '2'; // '12'
1 + 2 + '9'; // '39': before the string, numbers are added normally
1 + 2 + '9' + 4 + 5; // '3945': but afterward, each subsequent number is coerced

// when using bitshift operators, operands will be coerced to numbers
'1' << 2; // 4
1 << '2'; // 4
'1' << '2'; // 4
'1' << true; // 2
'1' << false; // 1

// the coercion does not affect the operand's value
var x = '1';
var y = 2;
x << y; // 4
x; // '1'

// type coercion is turned "off" when using ===
'1' == 1; // true
'1' === 1; // false
```