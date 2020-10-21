### Problem E2: Micro Kitchens - Medium (25 points)
You are a space planner for a new start-up and need to find the ideal spot in the office to put the micro kitchen.

You must make it as easy as possible to get to by finding **all** the spots that **minimize the sum of distances from that spot to all employees in the office**. The distance to an employee is the number of moves on the shortest path moving left, right, up, or down (but not diagonally) by one cell at a time. There are <img src="https://latex.codecogs.com/png.latex?E"> employees in the office.

The office has grown a bit and to handle the scale, they have made some changes that need to be taken into account when finding the best spots to place micro kitchens:
* The office now has **walls** which obstruct employees' movements.
* Desks are larger, meaning that **it is no longer possible for employees to walk through each others' desk areas**.
* Employees found it distracting to be sitting in the same spot as the micro kitchen, so now employees **cannot share the same space with a micro kitchen**.

What are **all** the <img src="https://latex.codecogs.com/png.latex?X"> and <img src="https://latex.codecogs.com/png.latex?Y"> coordinates of the best spots to put micro kitchens for these new constraints, given that <img src="https://latex.codecogs.com/png.latex?\(0,0\)"> is in the top-left, with <img src="https://latex.codecogs.com/png.latex?X"> coordinates increasing from left to right, and <img src="https://latex.codecogs.com/png.latex?Y"> coordinates increasing from top to bottom? It's not guaranteed that a unique best spot exists, your job is to find all of them and show them in increasing order by <img src="https://latex.codecogs.com/png.latex?X"> and then by <img src="https://latex.codecogs.com/png.latex?Y">.

Your input specifies the layout of the office as follows:
* The first line contains 3 numbers: <img src="https://latex.codecogs.com/png.latex?W">, <img src="https://latex.codecogs.com/png.latex?H">, and <img src="https://latex.codecogs.com/png.latex?N">, representing the **width**, **height** and **number of floors** in the office. In this version of this problem, it's guaranteed that there is only a single floor <img src="https://latex.codecogs.com/png.latex?\(N=1\)">.
* What follows is <img src="https://latex.codecogs.com/png.latex?N"> sets of lines, with the <img src="https://latex.codecogs.com/png.latex?i">th set describing the <img src="https://latex.codecogs.com/png.latex?i">th floor:
  * Each set consists of <img src="https://latex.codecogs.com/png.latex?H"> lines that are <img src="https://latex.codecogs.com/png.latex?W"> characters wide.
  * Sets are separated by an empty line.
  * The <img src="https://latex.codecogs.com/png.latex?\(j,k\)">-th cell in the set (<img src="https://latex.codecogs.com/png.latex?j"> characters from the left and <img src="https://latex.codecogs.com/png.latex?k"> characters from the top of the set) represents the contents at position <img src="https://latex.codecogs.com/png.latex?\(j,k\)"> of the <img src="https://latex.codecogs.com/png.latex?i">th floor. Each cell will be one of the following:
    * "." - An empty space
    * "o" - An employee's desk area
    * "w" - A wall
    
**Constraints**

<img src="https://latex.codecogs.com/png.latex?1\leq\text{}W\leq200">
<img src="https://latex.codecogs.com/png.latex?1\leq\text{}H\leq200">
<img src="https://latex.codecogs.com/png.latex?1\leq\text{}E\leq50">
<img src="https://latex.codecogs.com/png.latex?N=1">

**Sample Input**
```
10 10 1
. . . . w . . . w .
. . o w . . . . o .
. . . . . . . . o .
. . w . o . . . . .
w . . . . . . . . .
. . . w . . o . . .
. . o . . . . . . w
. w w w . w . . . .
. . . . . . w . . .
w o . . . . . . . .
```
**Sample Output**
```
(4, 4) (5, 3)
```