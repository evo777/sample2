## How It Works
* Insertion Sort works by iterating over the array, leaving a sorted array behind the current position
* Out of place elements are removed and re-inserted into the trailing, sorted section of the array
* Elements to the right of the insertion point must be "shifted over" to the right by one spot to fill the "empty" spot
* Similar to how you would sort playing cards in your hand

[![Youtube Insertion Sort](https://i.ytimg.com/vi/c4BRHC7kTaQ/hqdefault.jpg?custom=true&w=120&h=90&jpg444=true&jpgq=90&sp=68&sigh=a0EXo5mFhbtD7dEoWYiwTq9O8Bk)](https://www.youtube.com/watch?v=c4BRHC7kTaQ)

## Example
For an in-place, stable, ascending-sort implementation:

1. Initialize a counter
1. An outer while-loop iterates across an array of values to be sorted
1. If an out-of-place element is detected (i.e. everything to the left of this spot is sorted), run the following routine
  1. Save a reference to this element (e.g. `outOfPlaceIndex`). Consider this spot "empty"
  1. Starting from the very beginning of the array, find the first element whose value is larger than that of the element at `outOfPlaceIndex`. Save a reference to this index (e.g. `firstLargerIndex`)
  1. Keep moving elements to the right by one index into the empty spot , ending with `firstLargerIndex`
  1. Move the `outOfPlaceIndex` element into the empty spot (which is now where `firstLargerEl` used to be)
  1. Continue the outer while-loop at the SAME spot to check if `firstLargerEl` is out of place (i.e. do NOT increment the counter)
1. Keep moving to the right by incrementing the counter until the last element has been processed

* Example js implementation
```javascript
function insertionSort(numbers) {
  numbers.forEach(function(number, i){
    let j = i;
    while( numbers[j] < numbers[j - 1] ) { // note that numbers[-1] returns undefined, and the comparison returns false
      let temp = numbers[j];
      numbers[j] = numbers[j - 1];
      numbers[j - 1] = temp;
      j--;
    }
  });
  return numbers;
};
```

## Time/Space Complexity
* Time
  * Average: O(n^2)
  * Worst: O(n^2)
  * Best is O(n) - an already-sorted array.
* Space
  * O(1)
* Compared to others
  * Like bubble sort, insertion sort is much less efficient than quick sort, merge sort, and heap sort which average O(n*logn)
  * However, still more efficient than bubble sort
* Advantages / Reasons to Use
  * In-place: O(1) memory
  * Online: Can sort a list as it receives it
  * Adaptive: efficient for data sets that are already substantially sorted (i.e. adding a a new item has minimal re-sorting cost)
  * Stable: same-value elements stay in their original order