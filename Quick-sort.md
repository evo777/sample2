## Quicksort (the better? sort)

## What
Quicksort is a divide and conquer algorithm. Quicksort first divides a large array into two smaller sub-arrays: the low elements and the high elements. Quicksort can then recursively sort the sub-arrays. It is not a stable sort, meaning that the relative order of equal sort items is not preserved. Quicksort can operate in-place on an array, requiring small additional amounts of memory to perform the sorting.

It's best case is O(n log(n))
Worst case us O(n^2)

Worst case happens if all elements in the array are the same value.

## How

1. if start isn't given:  left = pointer at the head
1. if end isn't given: right = pointer at the tail
1. if right-left <= 1 return array as is else 
1. Choose a pivot point (right-left/2) floored  (pivot)
1. if the left is < pivot increment the pointer position (up to the pivot position)
1. if the right is > pivot decrement right pointer position (up to the pivot position)
1. if left not equal to right
  * swap left and right.
  * if left or right was the pivot, swap the pivot pointer as well.
1. go to 4 and continue walking in until 
1. once left equals right we have sorted one element to its correct position.  

sort start to pivot-1 and sort pivot +1 to end


## The code

```javascript
var quickSort = function (items, left, right) {
  if (left === undefined) {
    left = 0;
    right = items.length-1;
  }
  if (right-left <= 1) {
    return items;
  } else {
    var pivot = Math.floor(right-left/2);
  }
  var origLeft = left;
  var origRight = right;

  while (left<right) {
    if (items[left] > items[pivot] && left < pivot) {
      while (items[right] > items[pivot] && right > pivot) {
        right--;
      }
      swap(items, left, right);
      if (pivot === right) {
        pivot === left;
      }
    }
    left++;
  }
  quickSort(items, origLeft, pivot-1);
  quickSort(items, origRight, pivot+1);
  return items;
};

var swap = function (items, left, right) {
  var holder = items[left];
  items[left] = items[right];
  items[right] = holder;

  return items;
};
```




