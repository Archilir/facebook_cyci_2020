### Problem A1: Calculator - Easy (5 points)
You've found an old calculator lying around (I mean **really** old). Its buttons and screen work, but it doesn't seem to do anything when you press the = button.  You've figured out that it has an onboard computer but its memory got wiped a long time ago. You've taken it upon yourself to restore it to its former glory.

Let's start by writing support for the **addition** and **subtraction** of **integers**. Input is fed to the calculator as a sequence of these integers, joined by addition and subtraction operators in infix notation (meaning each operator appears between its operands, as per usual).

Your input file is a list of <img src="https://latex.codecogs.com/png.latex?N"> valid inputs to your calculator, each on their own line. Each input contains <img src="https://latex.codecogs.com/png.latex?k"> numbers interleaved with <img src="https://latex.codecogs.com/png.latex?k-1"> operators, all separated by spaces:

<img src="https://latex.codecogs.com/png.latex?X_{0}\text{&space;}o_{0}\text{&space;}X_{1}\text{&space;}o_{1}\text{&space;...&space;}o_{k-2}\text{&space;}X_{k-1}">

Output the answers to each expression in order, separated by spaces.

**Constraints**

<img src="https://latex.codecogs.com/png.latex?0<N\leq100">
<img src="https://latex.codecogs.com/png.latex?0<k\leq10">
<img src="https://latex.codecogs.com/png.latex?-2^{21}<X_{i}<2^{21}\text{&space;}\forall0\leq\text{&space;}i<k">
<img src="https://latex.codecogs.com/png.latex?o_{i}\in\{+,-\}\text{&space;}\forall0\leq\text{&space;}i<k-1">

**Sample Input**
```
1179336 - -1848725 - 673545 - -538839 + 2088552 
-239204 + 1762703 - 1485958 - -2042708 - 560445 
1381566 + -1276476 + 2015012 + -392345 - 1507206
```
**Sample Output**
```
4981907 1519804 220551
```