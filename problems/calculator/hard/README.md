### Problem A3: Calculator - Hard (40 points)
Finally, to make this calculator extra special, you're going to implement **equation solving**. You noticed a button on the calculator annotated with the letter **X**, so you're going to use this to let people input formulae with **variables** in them.

Your calculator will now accept **an integer Y** then a space, followed by **a formula** in **prefix notation** (like before) mentioning the variable **X exactly once**, in the place of a number. It will output the **integer** value that **X** must take to make the formula evaluate to **Y**, if such an integer exists. If it's impossible to find such an integer, output `Err` instead.

For example, if we wanted to solve the equation

<img src="https://latex.codecogs.com/png.latex?231=(1+2)\times(X+4)\times(5+6)">

we would input the following into the calculator:

`231 * * + 1 2 + X 4 + 5 6`

Again, your input is a list of <img src="https://latex.codecogs.com/png.latex?N"> calculator inputs, each on their own line. Each input starts with an integer <img src="https://latex.codecogs.com/png.latex?Y">, followed by an expression in prefix notation containing <img src="https://latex.codecogs.com/png.latex?2k-1"> terms: A single variable <img src="https://latex.codecogs.com/png.latex?X">, <img src="https://latex.codecogs.com/png.latex?k-1"> numbers,

<img src="https://latex.codecogs.com/png.latex?X_{0}\text{&space;}X_{1}\text{&space;...&space;}X_{k-1}">

and <img src="https://latex.codecogs.com/png.latex?k-1"> operators,

<img src="https://latex.codecogs.com/png.latex?o_{0}\text{&space;}o_{1}\text{&space;...&space;}o_{k-2}">

all separated by spaces.

Output the answers to each expression in order, separated by spaces.

**Constraints**

<img src="https://latex.codecogs.com/png.latex?0<N\leq100">
<img src="https://latex.codecogs.com/png.latex?0<k\leq10">
<img src="https://latex.codecogs.com/png.latex?-2^{63}<Y<2^{63}">
<img src="https://latex.codecogs.com/png.latex?-2^{21}<X<2^{21}">
<img src="https://latex.codecogs.com/png.latex?-2^{21}<X_{i}<2^{21}\text{&space;}\forall0\leq\text{&space;}i<k">
<img src="https://latex.codecogs.com/png.latex?o_{i}\in\{+,-,*\}\text{&space;}\forall0\leq\text{&space;}i<k-1">

**Sample Input**
```
-4492458 - -869258 - + 766233 -405212 - + -74602 X -266504
1283990195631957899 + * - - -1322631 X * 1958979 -464816 1410102 916224
-494694 - + 687540 X + + 1972708 -638545 + 85021 1414869
```
**Sample Output**
```
-3454081 Err 1651819
```