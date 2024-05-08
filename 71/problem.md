## Description

<div><p>You are given an array of integers $a_1, a_2, \dots, a_n$. You can perform the following operation any number of times (possibly zero):</p><ul> <li> Choose any element $a_i$ from the array and change its value to any integer between $0$ and $a_i$ (inclusive). More formally, if $a_i &lt; 0$, replace $a_i$ with any integer in $[a_i, 0]$, otherwise replace $a_i$ with any integer in $[0, a_i]$. </li></ul><p>Let $r$ be the minimum possible product of all the $a_i$ after performing the operation any number of times.</p><p>Find the minimum number of operations required to make the product equal to $r$. Also, print one such shortest sequence of operations. If there are multiple answers, you can print any of them.</p></div><div class="input-specification"><p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 500$) - the number of test cases. This is followed by their description.</p><p>The first line of each test case contains the a single integer $n$ ($1 \leq n \leq 100$) — the length of the array.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($-10^9 \leq a_i \leq 10^9$).</p></div><div class="output-specification"><p>For each test case: </p><ul> <li> The first line must contain the minimum number of operations $k$ ($0 \leq k \leq n$). </li><li> The $j$-th of the next $k$ lines must contain two integers $i$ and $x$, which represent the $j$-th operation. That operation consists in replacing $a_i$ with $x$. </li></ul></div>

## Input

<p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 500$) - the number of test cases. This is followed by their description.</p><p>The first line of each test case contains the a single integer $n$ ($1 \leq n \leq 100$) — the length of the array.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($-10^9 \leq a_i \leq 10^9$).</p>

## Output

<p>For each test case: </p><ul> <li> The first line must contain the minimum number of operations $k$ ($0 \leq k \leq n$). </li><li> The $j$-th of the next $k$ lines must contain two integers $i$ and $x$, which represent the $j$-th operation. That operation consists in replacing $a_i$ with $x$. </li></ul>





```input1
4
1
155
4
2 8 -1 3
4
-1 0 -2 -5
4
-15 -75 -25 -30
```




```output1
1
1 0
0
0
1
3 0
```



## Note

<p>In the first test case, we can change the value of the first integer into $0$ and the product will become $0$, which is the minimum possible.</p><p>In the second test case, initially, the product of integers is equal to $2 \cdot 8 \cdot (-1) \cdot 3 = -48$ which is the minimum possible, so we should do nothing in this case.</p>
