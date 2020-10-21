### Problem A1: Calculator - Easy (5 points)
You've found an old calculator lying around (I mean **really** old). Its buttons and screen work, but it doesn't seem to do anything when you press the = button.  You've figured out that it has an onboard computer but its memory got wiped a long time ago. You've taken it upon yourself to restore it to its former glory.

Let's start by writing support for the **addition** and **subtraction** of **integers**. Input is fed to the calculator as a sequence of these integers, joined by addition and subtraction operators in infix notation (meaning each operator appears between its operands, as per usual).

Your input file is a list of $N$ valid inputs to your calculator, each on their own line. Each input contains $k$ numbers interleaved with $k-1$ operators, all separated by spaces:

$X_{0}$ $o_{0}$ $X_{1}$ $o_{1}$ ... $o_{k-2}$ $X_{k-1}$

Output the answers to each expression in order, separated by spaces.

**Constraints**
$0 < N \leq 100$
$0 < k \leq 10$
$-2^{21} < X_{i} < 2^{21}$&nbsp;&nbsp;&nbsp;&nbsp;$\forall 0 \leq i < k$
$o_{i} \in \{+,-\}$&nbsp;&nbsp;&nbsp;&nbsp;$\forall 0 \leq i < k - 1$

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