### Problem B2: Construct the Tree - Medium (15 points)

Given a **binary tree**, compute its **in-order traversal**. An in-order traversal from a root node R is defined recursively by performing an in-order traversal of R's left subtree, then visiting R, and then performing an in-order traversal of its right subtree.

Inputs consists of two lines, the first containing the number of nodes <img src="https://latex.codecogs.com/png.latex?N"> and the root node, the second containing <img src="https://latex.codecogs.com/png.latex?2N"> tokens describing the edges in the tree.  The full description of the input format is defined in the *Easy* variant of this problem.

Output the values of all of the tree’s nodes in order of the in-order traversal, separated by spaces.

**Constraints**

<img src="https://latex.codecogs.com/png.latex?1\leq\text{}N\leq1000">

**Sample Input**
```
6 0
3 2 X X X X 4 5 X 1 X X
```
**Sample Output**
```
4 1 3 5 0 2
```