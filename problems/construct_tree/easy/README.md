### Problem B1: Construct the Tree - Easy (15 points)
Given a binary tree, compute its pre-order traversal. A pre-order traversal from a root node R is defined recursively by visiting R, then performing a pre-order traversal of R's left subtree, and then performing a pre-order traversal of its right subtree.

A tree is represented by two lines.  The first line contains two tokens separated by a space:
* The first token is an integer, <img src="https://latex.codecogs.com/png.latex?N">, the number of nodes in the tree.  These nodes are referred to by ordinal numbers: <img src="https://latex.codecogs.com/png.latex?0,1">, up to <img src="https://latex.codecogs.com/png.latex?N-1">.
* The second token indicates the root node.  A value of <img src="https://latex.codecogs.com/png.latex?X"> indicates no root, i.e. an empty tree.  An integer value is interpreted as the ordinal of the root node.

The second line is a list of <img src="https://latex.codecogs.com/png.latex?2N"> tokens, separated by spaces:

<img src="https://latex.codecogs.com/png.latex?L_{0}\text{&space;}R_{0}\text{&space;}L_{1}\text{&space;}R_{1}\text{&space;...&space;}L_{N-1}\text{&space;}R_{N-1}">

* Where <img src="https://latex.codecogs.com/png.latex?L_i"> and <img src="https://latex.codecogs.com/png.latex?R_i"> represent the left and right children of the <img src="https://latex.codecogs.com/png.latex?i">th node (the node with ordinal i) respectively.
  * If <img src="https://latex.codecogs.com/png.latex?L_i"> is the literal <img src="https://latex.codecogs.com/png.latex?X">, this indicates that the <img src="https://latex.codecogs.com/png.latex?i">th node has no left child.
  * <img src="https://latex.codecogs.com/png.latex?R_i"> is encoded similarly.
* It is guaranteed that interpreting the input this way will produce a binary tree:
  * The graph will be acyclic.
  * The root has no parent edges.
  * Each non-root node will have precisely one parent edge.

For example, this input:

```
7 5
X X 4 0 1 X X 6 X X 3 2 X X
```

corresponds to the following tree:

```
     5
 /       \
3         2
 \       /  
  6     1    
       / \
      4   0
```

For further clarity, the following diagram illustrates the nonexistent children in that tree which the <img src="https://latex.codecogs.com/png.latex?X"> characters in the input represent:

```
        5
   /         \
  3           2
 / \         / \
X   6       1   X
   / \    /   \
  X   X  4     0
        / \   / \
       X   X X   X
```

Output the values of all of the tree’s nodes in order of the pre-order traversal, separated by spaces.

**Constraints**

<img src="https://latex.codecogs.com/png.latex?1\leq\text{}N\leq10">
<img src="https://latex.codecogs.com/png.latex?0\leq\text{}L_i,R_i<N\text{&space;}\forall0\leq\text{&space;}i<k">


**Sample Input**
```
6 5
4 2 X X X X X X 3 X 1 0
```
**Sample Output**
```
5 1 0 4 3 2
```