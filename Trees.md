## Definition
As a data structure, a tree consists of a group of nodes, where each node has a value and a list of references to other nodes(its children). The children themselves are trees as well.  To differentiate a tree from a graph data structure, there is a requirement where no two references point to the same node.

## Tree traversal
### Depth First Search
DFS starts at the root of the tree and explore as deep as possible along each branch before backtracking and move onto the next branch of the tree.  The implementation of the DFS uses a stack.
There are 3 different kinds of depth first traversals for binary trees:
  * pre-order: visit each node before visiting any of its children
  * in-order: visit each node after visiting its left child, but before visiting its right child
  * post-order: visit each node after visiting both of its children

### Breath First Search (BFS)
BFS starts at the root of the tree and explores all the neighboring nodes first before moving onto the next level(generation).  The implementation of the BFS uses a queue.

### Time and Space complexity
Note: b is branching factor of the tree, and d is the depth of the tree
* DFS
  * Time: O(b^d): must examine every node in the tree. Search is unconstrained by the goal until it happens to stumble on the goal.
  * space: O(b*d): the longest possible path is d, and for every node in that path must maintain a fringe of size b
* BFS
  * Time: O(b^d)
  * space: O(b^d), because the whole frontier is stored in memory

Reference Lecture slides here:(https://www.cs.ubc.ca/~kevinlb/teaching/cs322%20-%202008-9/Lectures/Search3.pdf)