## What is it?
* A method for solving complex problems by breaking it down into simpler subproblems
* You only solve the subproblem just once and store the result in memory.
* used for optimization

## Top-Down
* Start solving the given problem by breaking it down. If you see the problem has already been solved then return the saved answer. If it has not, solve the answer and save it (Memoization)

## Bottom-Up
Analyze the problem to see the order in which the subproblems are solved and start solving from the trivial subproblem up towards the given problem. It is guaranteed that the subproblems are solved before solving the problem (Dynamic programming)

## Examples
* Shortest path problem - Find the shortest paths between nodes in a graph
* Fibonacci sequence
* Longest increasing subsequence - find the length of the longest subsequence of a given sequence such that all elements of the subsequence are sorted in increasing order.
* Knapsack problem - Given n items of weight wi and value vi, find the items that should be taken such that the weight is less than the maximum weight W and the corresponding total value is maximum.