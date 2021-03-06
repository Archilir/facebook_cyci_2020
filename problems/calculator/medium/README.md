### Problem A2: Calculator - Medium (15 points)
Now let's hook up multiplication to your old calculator. Only now you notice your calculator has no parenthesis buttons!

How will you input a calculation like <img src="https://latex.codecogs.com/png.latex?(1+2)\times(3+4)\times(5+6)">? You decide to use [prefix notation](https://en.wikipedia.org/wiki/Polish_notation?fbclid=IwAR11VISin6XH_38-CFvu8ju4DzaaIZIqt4I_x-3wvwAs9JhM1UGhZgfATtw), where the **operator** is input **before** its operands. For example, our expression is equivalent to both:

`* + 1 2 * + 3 4 + 5 6`

and

`* * + 1 2 + 3 4 + 5 6`

Write a calculator supporting **addition**, **subtraction** and **multiplication** of **integers**. The integers can be **positive** or **negative** (starting with a -). The formula will be given in **prefix notation** with a space between each term (operator or operand).

Like before, your input file is a list of <img src="https://latex.codecogs.com/png.latex?N"> expressions to evaluate, each on their own line, although this time they are in prefix notation and may include multiplications. Each input contains <img src="https://latex.codecogs.com/png.latex?2k-1"> terms: <img src="https://latex.codecogs.com/png.latex?k"> numbers,

<img src="https://latex.codecogs.com/png.latex?X_{0}\text{&space;}X_{1}\text{&space;...&space;}X_{k-1}">

and <img src="https://latex.codecogs.com/png.latex?k-1"> operators,

<img src="https://latex.codecogs.com/png.latex?o_{0}\text{&space;}o_{1}\text{&space;...&space;}o_{k-2}">

all separated by spaces.

Output the answers to each expression in order, separated by spaces.

**Constraints**

<img src="https://latex.codecogs.com/png.latex?0<N\leq100">
<img src="https://latex.codecogs.com/png.latex?0<k\leq10">
<img src="https://latex.codecogs.com/png.latex?-2^{21}<X_{i}<2^{21}\text{&space;}\forall0\leq\text{&space;}i<k">
<img src="https://latex.codecogs.com/png.latex?o_{i}\in\{+,-,*\}\text{&space;}\forall0\leq\text{&space;}i<k-1">

**Sample Input**
```
* - + * -218391 -1972178 -716219 792848 -1734976
- - -1909632 1018165 - * -639315 -1125817 1697636
+ 460272 * + -388143 - -1643824 1236325 512934
```
**Sample Output**
```
-747261825775288256 -719752925516 -1676417628456
```