## Description

<div><p><span class="tex-font-style-bf">This is the solo version of the problem. Note that the solution of this problem may or may not share ideas with the solution of the game version. You can solve and get points for both versions independently.</span></p><p><span class="tex-font-style-bf">You can make hacks only if both versions of the problem are solved.</span></p><p>Given an integer variable $x$ with the initial value of $n$. A single break operation consists of the following steps: </p><ul> <li> Choose a value $y$ such that $0 \lt y \lt x$ and $0 \lt (x \oplus y) \lt x$. </li><li> Update $x$ by either setting $x = y$ or setting $x = x \oplus y$. </li></ul> Determine whether it is possible to transform $x$ into $m$ using a maximum of $63$ break operations. If it is, provide the sequence of operations required to achieve $x = m$.<p>You don't need to minimize the number of operations.</p><p>Here $\oplus$ denotes the <a href="https://en.wikipedia.org/wiki/Bitwise_operation#XOR">bitwise XOR operation</a>.</p></div><div class="input-specification"><p>The first line contains one positive integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>Each test case consists of a single line containing two integers $n$ and $m$ ($1 \leq m \lt n \leq 10^{18}$)&nbsp;— the initial value of $x$ and the target value of $x$.</p></div><div class="output-specification"><p>For each test case, output your answer in the following format.</p><p>If it is not possible to achieve $m$ in $63$ operations, print $-1$.</p><p>Otherwise, </p><p>The first line should contain $k$ ($1 \leq k \leq 63$)&nbsp;— where $k$ is the number of operations required.</p><p>The next line should contain $k+1$ integers&nbsp;— the sequence where variable $x$ changes after each break operation. The $1$-st and $k+1$-th integers should be $n$ and $m$, respectively.</p></div>

## Input

<p>The first line contains one positive integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>Each test case consists of a single line containing two integers $n$ and $m$ ($1 \leq m \lt n \leq 10^{18}$)&nbsp;— the initial value of $x$ and the target value of $x$.</p>

## Output

<p>For each test case, output your answer in the following format.</p><p>If it is not possible to achieve $m$ in $63$ operations, print $-1$.</p><p>Otherwise, </p><p>The first line should contain $k$ ($1 \leq k \leq 63$)&nbsp;— where $k$ is the number of operations required.</p><p>The next line should contain $k+1$ integers&nbsp;— the sequence where variable $x$ changes after each break operation. The $1$-st and $k+1$-th integers should be $n$ and $m$, respectively.</p>





```input1|2,4
3
7 3
4 2
481885160128643072 45035996273704960
```




```output1
1
7 3
-1
3
481885160128643072 337769972052787200 49539595901075456 45035996273704960
```



## Note

<p>In the first test case $n = 7$, for the first operation $x = 7$ if we choose $y = 3$ then $(7 \oplus 3) \lt 7$, hence we can update $x$ with $3$ which is equal to $m$.</p><p>In the second test case $n = 4$, for the first operation $x = 4$.</p><p>If we choose: </p><ul> <li> $y = 1$ then $(4 \oplus 1) \gt 4$ </li><li> $y = 2$ then $(4 \oplus 2) \gt 4$ </li><li> $y = 3$ then $(4 \oplus 3) \gt 4$ </li></ul><p>Hence we can't do the first operation and it is impossible to make $x = 2$.</p>
