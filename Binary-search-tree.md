## Background

A Binary Search Tree is a data structure that stores its nodes in sorted order according to the following conditions:

* Each node contains one key (unique).
* The keys in the left sub-tree are less than the key in its parent node.
* The keys in the right sub-tree greater than the key in its parent node.
* Duplicate node keys are not allowed.

![Binary Search Treet](http://i.stack.imgur.com/X6vkB.png)

## Properties

* Fast lookup, addition and removal of items (but slower than hash tables).
* Can be searched in O(log n) time complexity.
* Values stored in sorted order.

## Basic Operations

* Search
* Insert
* Delete
* Preorder Traversal:
  - process all nodes of a tree by processing the root, then recursively processing all subtrees.
* Inorder Traversal:
  - process all nodes of a tree by recursively processing the left sub-tree, then processing the root, and finally the right sub-tree.
* Postorder Traversal:
  - process all nodes of a tree by recursively processing the all subtrees, then finally processing the root.

## See also

* Hash Tables
* Time and Space Complexity (Big O notation)

