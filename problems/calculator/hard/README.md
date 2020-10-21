### Problem A3: Calculator - Hard (40 points)
Finally, to make this calculator extra special, you're going to implement **equation solving**. You noticed a button on the calculator annotated with the letter **X**, so you're going to use this to let people input formulae with **variables** in them.

Your calculator will now accept **an integer Y** then a space, followed by **a formula** in **prefix notation** (like before) mentioning the variable **X exactly once**, in the place of a number. It will output the **integer** value that **X** must take to make the formula evaluate to **Y**, if such an integer exists. If it's impossible to find such an integer, output `Err` instead.

For example, if we wanted to solve the equation

$231 = (1 + 2) \times (X + 4) \times (5 + 6)$

we would input the following into the calculator:

`231 * * + 1 2 + X 4 + 5 6`

Again, your input is a list of $N$ calculator inputs, each on their own line. Each input starts with an integer $Y$, followed by an expression in prefix notation containing $2k-1$ terms: A single variable $X$, $k-1$ numbers,

$X_{0}$ $X_{1}$ ... $X_{k-1}$

and $k - 1$ operators,

$o_{0}$ $o_{1}$ ... $o_{k-2}$

all separated by spaces.

Output the answers to each expression in order, separated by spaces.

**Constraints**
$0 < N \leq 100$
$0 < k \leq 10$
$-2^{63} < Y < 2^{63}$
$-2^{21} < X < 2^{21}$
$-2^{21} < X_{i} < 2^{21}$&nbsp;&nbsp;&nbsp;&nbsp;$\forall 0 \leq i < k$
$o_{i} \in \{+,-,*\}$&nbsp;&nbsp;&nbsp;&nbsp;$\forall 0 \leq i < k - 1$

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