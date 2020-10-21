### Problem B3: Construct the Tree - Hard (35 points)
Given the **pre-order and in-order traversals** of a **binary tree**, compute the representation of the tree as it would appear as in input to the easy and medium problems:

A tree is represented by two lines.  The first line contains two tokens separated by a space:
* The first token is an integer, <img src="https://latex.codecogs.com/png.latex?N">, the number of nodes in the tree.  These nodes are referred to by ordinal numbers: <img src="https://latex.codecogs.com/png.latex?0,1">, up to <img src="https://latex.codecogs.com/png.latex?N-1">.
* The second token indicates the root node.  A value of <img src="https://latex.codecogs.com/png.latex?X"> indicates no root, i.e. an empty tree.  An integer value is interpreted as the ordinal of the root node.

The second line is a list of <img src="https://latex.codecogs.com/png.latex?2N"> tokens, separated by spaces:

<img src="https://latex.codecogs.com/png.latex?L_{0}\text{&space;}R_{0}\text{&space;}L_{1}\text{&space;}R_{1}\text{&space;...&space;}L_{N-1}\text{&space;}R_{N-1}">

* Where <img src="https://latex.codecogs.com/png.latex?L_i"> and <img src="https://latex.codecogs.com/png.latex?R_i"> represent the left and right children of the <img src="https://latex.codecogs.com/png.latex?i">th node (the node with ordinal i) respectively.
  * If <img src="https://latex.codecogs.com/png.latex?L_i"> is the literal <img src="https://latex.codecogs.com/png.latex?X">, this indicates that the <img src="https://latex.codecogs.com/png.latex?i">th node has no left child.
  * If it is an integer, it is interpreted as the ordinal number of the <img src="https://latex.codecogs.com/png.latex?i">th node's left child.
  * <img src="https://latex.codecogs.com/png.latex?R_i"> is encoded similarly.
* It is guaranteed that interpreting the input this way will produce a binary tree:
  * The graph will be acyclic.
  * The root has no parent edges.
  * Each non-root node will have precisely one parent edge.

For example, this tree:

```
     5
 /       \
3         2
 \       /  
  6     1    
       / \
      4   0
```

Would be output as:

`7 5 X X 4 0 1 X X 6 X X 3 2 X X`

For further clarity, the following diagram illustrates the non-existent children in the tree above which the <img src="https://latex.codecogs.com/png.latex?X"> characters represent in the output:

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

<img src="https://latex.codecogs.com/png.latex?1\leq\text{}N\leq1000">

**Sample Input**
```
5 2 0 3 1 4
2 3 0 5 1 4
```
**Sample Output**
```
6 5
3 X X 4 X 0 X X X X 2 1
```