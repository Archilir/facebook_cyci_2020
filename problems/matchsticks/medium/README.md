### Problem D2: Matchsticks - Medium (10 points)
You have been given a bag of matchsticks of various lengths.  What's the perimeter of the largest **rectangle** that you can form using a single, whole matchstick for each of its sides?

Your input consists of <img src="https://latex.codecogs.com/png.latex?20"> lines.  Each line is a list of <img src="https://latex.codecogs.com/png.latex?N"> space-delimited **positive integers** representing the lengths of the matchsticks in a single test case:

<img src="https://latex.codecogs.com/png.latex?M_0\text{&space;}M_1\text{&space;...&space;}M_{N-1}">

For each line of input, output a single integer representing the **perimeter of the largest rectangle**, or -1 if it is not possible to make a rectangle with the given bag of matchsticks.  Format the outputs on a single line, separated by spaces.

**Constraints**

<img src="https://latex.codecogs.com/png.latex?0<N\leq100000">
<img src="https://latex.codecogs.com/png.latex?0<M_i\leq100000\text{&space;}\forall0\leq\text{}i<N">

**Sample Input**
```
6 10 6 6 6 10
5 10 6 9 5 5 5
8 10 8 10 8 4 8
4 7 8 9 8 7 7 8 9 7
3 4 1 3 1 9
```
**Sample Output**
```
32 20 36 34 8
```