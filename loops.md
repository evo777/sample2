# Loops

## What are they?
- Loops are an easy to repeatedly complete a specific operation
- There many different kinds of loops, which are described below

## For loop
- A floor loop repeats until a specified statement is false
- A typical for loop will take three arguments
 - Initialization expression
 - Condition
 - Increment expression

For example, the below for loop will initialize at `i = 0`, continue as long as `i < 5`, and increment `i` by 1 after every iteration.
```javascript
for (let i = 0; i < 5; i++) {
  console.log(i);
}
```

## While loop
- Will continue as long as the specified `while` statement is `true`
- Some potential applications of while loops include breadth-first tree/graph traversal and binary search

```javascript
let arr = [true, true, false, true, true];
let i = 0;
while (arr[i]) {
  console.log('the value is true');
  i++;
}
```

## Do-While loop
- Similar to a while loop except that the code inside the loop will run at least once, regardless of whether or not the while statement is true 

```javascript
Do {
  console.log('I will run at lease once!'); // Will log to the console even though the while statement is false
} while (false);
```

## For in loop
- Iterates a specified variable over all the enumerable properties of an object

```javascript
let obj = { one: 1, two: 2, three: 3, };
for (let key in obj) {
  console.log(obj[key]); // Will log 1, 2, 3 to the console
  console.log(key); // Will log 'one', 'two', 'three' to the console
}
```

## For of loop
- Similar to a for-in loop except that it iterates over the property values (as opposed to property names)
- Only works for collections (arrays, maps, strings, sets) but does not work for objects
```javascript
let arr = [7, 12, 30];
for (let val of arr) {
  console.log(val); // Will log 7, 12, 30 to the console
}
let string = 'hello world'
for (let char of string) {
  console.log(char); // Will log 'h', 'e', 'l', etc.
}
```