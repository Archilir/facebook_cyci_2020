### Problem E1: Micro Kitchens - Easy (5 points)
You are a space planner for a new start-up and need to find the ideal spot in the office to put the micro kitchen.

You must make it as easy as possible to get to by picking the spot that **minimizes the sum of distances from that spot to all employees in the office**. The distance to an employee is the number of moves on the shortest path moving left, right, up, or down (but not diagonally) by one cell at a time.

For now, the office only contains the startup's employees, who work on a single office floor. They don't mind sharing a spot with the micro kitchen and they can walk through each others' desk areas. What are the <img src="https://latex.codecogs.com/png.latex?X"> and  <img src="https://latex.codecogs.com/png.latex?Y"> coordinates of the best spot to put the micro kitchen, given that <img src="https://latex.codecogs.com/png.latex?\(0,0\)"> is in the top-left, with <img src="https://latex.codecogs.com/png.latex?X"> coordinates increasing from left to right, and <img src="https://latex.codecogs.com/png.latex?Y"> coordinates increasing from top to bottom? It's guaranteed that a unique best spot exists.

Your input specifies the layout of the office as follows:
* The first line contains 3 numbers: <img src="https://latex.codecogs.com/png.latex?W">, <img src="https://latex.codecogs.com/png.latex?H">, and <img src="https://latex.codecogs.com/png.latex?N">, representing the **width**, **height** and **number of floors** in the office. In this version of this problem, it's guaranteed that there is only a single floor <img src="https://latex.codecogs.com/png.latex?\(N=1\)">.
* What follows is <img src="https://latex.codecogs.com/png.latex?N"> sets of lines, with the <img src="https://latex.codecogs.com/png.latex?i">th set describing the <img src="https://latex.codecogs.com/png.latex?i">th floor:
  * Each set consists of <img src="https://latex.codecogs.com/png.latex?H"> lines that are <img src="https://latex.codecogs.com/png.latex?W"> characters wide.
  * Sets are separated by an empty line.
  * The <img src="https://latex.codecogs.com/png.latex?\(j,k\)">-th cell in the set (<img src="https://latex.codecogs.com/png.latex?j"> characters from the left and <img src="https://latex.codecogs.com/png.latex?k"> characters from the top of the set) represents the contents at position <img src="https://latex.codecogs.com/png.latex?\(j,k\)"> of the <img src="https://latex.codecogs.com/png.latex?i">th floor. Each cell will be one of the following:
    * "." - An empty space
    * "o" - An employee's desk area
    
**Constraints**

<img src="https://latex.codecogs.com/png.latex?1\leq\text{}W\leq1000">
<img src="https://latex.codecogs.com/png.latex?1\leq\text{}H\leq1000">
<img src="https://latex.codecogs.com/png.latex?N=1">

**Sample Input**
```
10 10 1
. . . . . . . . . .
. . . . . . . . . .
. . . . . . . . . .
. . . . . o . . . .
. . . . . . o . . o
. . . . . o . o . .
. . . . . . . . . .
. . . o . . . . . .
. . . . . . . . . o
. . . . . . . . . .
```
**Sample Output**
```
(6, 5)
```