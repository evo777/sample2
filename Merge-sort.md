### Overview
* Divide and conquer sorting algorithm
* Can be done recursively or iteratively
* Most implementations achieve stable sort 
* Time complexity is O(n * log(n))

### Description
1. Divide unsorted set of values in half
2. Keep dividing into _n_ sublists. sublist of length 1 is considered to be sorted
3. Merge sorted sublists until only one sublist remaining

### Notes
* Usually uses a helper function for the merge step
* In most cases faster than insertion sort, except if list is already sorted.

### Sample Implementation
```
var merge = function (left, right) {
  var merged = [];
  var iL = 0, iR = 0;
  while (merged.length < left.length + right.length) {
    // Default to the left element for stability
    if (iR >= right.length || left[iL] <= right[iR])  {
      merged.push(left[iL]);
      iL += 1;
    } else {
      merged.push(right[iR]);
      iR += 1;
    }
  }
  return merged;
}

var mergeSort = function(array) {
  // Your code here.

  var lists = [];
  // Split array into sublists
  // Natural variant: split array into pre-sorted sublists
  var currentList = [];
  lists = []
  for (var i = 0; i < array.length; i++) {
    if (currentList.length && array[i] < currentList[currentList.length-1]) {
      lists.push(currentList);
      currentList = [];
    }
    currentList.push(array[i]);
  }
  lists.push(currentList);
  // Until the entire array is sorted
  while (lists.length > 1) {
    var newLists = [];
    // Merge all adjacent lists
    for (var i = 0; i < Math.floor(lists.length/2); i++) {
      newLists.push(merge(lists[i*2], lists[i*2+1]))
    }
    // Include the leftover list if the number is odd
    if (lists.length % 2) {
      newLists.push(lists[lists.length-1]);
    }
    lists = newLists;
  }
  // we have a single, fully sorted list
  return lists[0];
  };
```