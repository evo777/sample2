## What is Memoization?
In computer science, memoization is the process of caching the results of computations to be easily referenced later, to avoid potentially expensive operations. 

## Why do we Memoize?
Memoization is an optimization to save on computational resources, e.g. a space saving strategy when implementing recursive function calls. 

## Example
```
function Fibber() {
    this.memo = {};
}

Fibber.prototype.fib = function(n) {

    // edge case
    if (n < 0) {
        throw new Error('Index was negative. No such thing as a negative index in a series.');

    // base cases
    } else if (n === 0 || n === 1) {
        return n;
    }

    // see if we've already calculated this
    if (this.memo.hasOwnProperty(n)) {
        console.log('grabbing memo[' + n + ']');
        return this.memo[n];
    }

    console.log('computing fib(' + n + ')');
    var result = this.fib(n-1) + this.fib(n-2);

    // memoize
    this.memo[n] = result;

    return result;
}
```
example from: [interview cake](https://www.interviewcake.com/concept/javascript/memoization)


## Additional Information
Memoization is a popular strategy in dynamic programming, which is when a problem can be broken down into smaller subproblems. Another common strategy in dynamic programming is the bottom-up strategy.

## Popular Implementations
* [Underscore Library](http://underscorejs.org/#memoize)

## Extra Resources
* [Interview Cake](https://www.interviewcake.com/concept/javascript/memoization)
* [Wikipedia](https://en.wikipedia.org/wiki/Memoization)