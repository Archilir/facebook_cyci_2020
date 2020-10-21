### Problem E3: Micro Kitchens - Hard (50 points)
You are a space planner for a new start-up and need to find the ideal spot in the office to put the micro kitchen.

You must make it as easy as possible to get to by finding **all** the spots that **minimize the sum of distances from that spot to all employees in the office**. The distance to an employee is the number of moves on the shortest path moving left, right, up, or down (but not diagonally) by one cell at a time. There are <img src="https://latex.codecogs.com/png.latex?E"> employees in the office.

Your startup has outgrown its office yet again and is planning another move. Luckily, the new office doesn't introduce any more exotic architecture (like walls), but it will be spread out over **multiple floors**, connected by **flights of stairs**. Each floor features exactly one flight of stairs.

The constraints for movement and placing of the micro kitchen remain the same as in the single-floor layout:
* **Walls** still obstruct employees' movements.
* Employees **cannot walk through each others' desk areas**.
* Employees **cannot share the same space with a micro kitchen**.

The office employs a modern design that **doesn't require flights of stairs to be in the same position in every floor**. Moving up or down a floor doesn't take any effort for employees either, meaning the cost of moving between floors is 0 and an employee standing on a flight of stairs is one move away from the spots adjacent to stairs on all floors.

What are **all** the <img src="https://latex.codecogs.com/png.latex?F">, <img src="https://latex.codecogs.com/png.latex?X">, and <img src="https://latex.codecogs.com/png.latex?Y"> coordinates of the best spots to put micro kitchens, given that <img src="https://latex.codecogs.com/png.latex?\(0,0,0\)"> is in the top-left corner of the <img src="https://latex.codecogs.com/png.latex?0">th floor, with <img src="https://latex.codecogs.com/png.latex?F"> coordinates increasing for successive floors, <img src="https://latex.codecogs.com/png.latex?X"> coordinates increasing from left to right, and <img src="https://latex.codecogs.com/png.latex?Y"> coordinates increasing from top to bottom? It's **not** guaranteed that a unique best spot, your job is to find all of them and show them in increasing order by <img src="https://latex.codecogs.com/png.latex?F">, then by <img src="https://latex.codecogs.com/png.latex?X"> and then by <img src="https://latex.codecogs.com/png.latex?Y">.

Your input specifies the layout of the office as follows:
* The first line contains 3 numbers: <img src="https://latex.codecogs.com/png.latex?W">, <img src="https://latex.codecogs.com/png.latex?H">, and <img src="https://latex.codecogs.com/png.latex?N">, representing the **width**, **height** and **number of floors** in the office. In this version of this problem, it's guaranteed that there is only a single floor <img src="https://latex.codecogs.com/png.latex?\(N=1\)">.
* What follows is <img src="https://latex.codecogs.com/png.latex?N"> sets of lines, with the <img src="https://latex.codecogs.com/png.latex?i">th set describing the <img src="https://latex.codecogs.com/png.latex?i">th floor:
  * Each set consists of <img src="https://latex.codecogs.com/png.latex?H"> lines that are <img src="https://latex.codecogs.com/png.latex?W"> characters wide.
  * Sets are separated by an empty line.
  * The <img src="https://latex.codecogs.com/png.latex?\(j,k\)">-th cell in the set (<img src="https://latex.codecogs.com/png.latex?j"> characters from the left and <img src="https://latex.codecogs.com/png.latex?k"> characters from the top of the set) represents the contents at position <img src="https://latex.codecogs.com/png.latex?\(j,k\)"> of the <img src="https://latex.codecogs.com/png.latex?i">th floor. Each cell will be one of the following:
    * "." - An empty space
    * "o" - An employee's desk area
    * "w" - A wall
    * "s" - A flight of stairs (occurring exactly once per floor)
    
**Constraints**

<img src="https://latex.codecogs.com/png.latex?1\leq\text{}W\leq50">
<img src="https://latex.codecogs.com/png.latex?1\leq\text{}H\leq50">
<img src="https://latex.codecogs.com/png.latex?1\leq\text{}N\leq10">
<img src="https://latex.codecogs.com/png.latex?1\leq\text{}E\leq50">

**Sample Input**
```
10 10 3
. . . . . . . . . .
. w o . . . . . . .
. . w . . . . w . .
. . . w o . . . . .
w . . s w . . . . .
. . . . . . . . . .
. . . . . . . . . .
. . w . . . . . . .
. . . . . . . . . w
. . . . . . . o w .

. . o . . w w . . .
. . . . o . . . . .
. . . . w . . w . w
. . . . o . w . . .
. . . . w w . . . .
w . . . . . . . . .
. . . . s . . . . .
. w w . . w . . . .
w . . . . . . . o .
. . . . . w w . w w

. w . . . . . . w .
. . w s . . . . w .
. . . . . . . . . .
. . . . w . w . . .
o . . . o . . . . o
. w . . . . . . . w
w w . w w . . . . .
. w . w . . . . . .
. . . . . . . w . w
. w w . . w . . . .
```
**Sample Output**
```
(0, 3, 5) (1, 3, 6) (1, 4, 5) (2, 3, 2)
```