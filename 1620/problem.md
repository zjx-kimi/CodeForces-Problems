## Description

<div><p>You are given four integers $n$, $B$, $x$ and $y$. You should build a sequence $a_0, a_1, a_2, \dots, a_n$ where $a_0 = 0$ and for each $i \ge 1$ you can choose: </p><ul> <li> either $a_i = a_{i - 1} + x$ </li><li> or $a_i = a_{i - 1} - y$. </li></ul><p>Your goal is to build such a sequence $a$ that $a_i \le B$ for all $i$ and $\sum\limits_{i=0}^{n}{a_i}$ is maximum possible.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. Next $t$ cases follow.</p><p>The first and only line of each test case contains four integers $n$, $B$, $x$ and $y$ ($1 \le n \le 2 \cdot 10^5$; $1 \le B, x, y \le 10^9$).</p><p>It's guaranteed that the total sum of $n$ doesn't exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, print one integer&nbsp;— the maximum possible $\sum\limits_{i=0}^{n}{a_i}$.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. Next $t$ cases follow.</p><p>The first and only line of each test case contains four integers $n$, $B$, $x$ and $y$ ($1 \le n \le 2 \cdot 10^5$; $1 \le B, x, y \le 10^9$).</p><p>It's guaranteed that the total sum of $n$ doesn't exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, print one integer&nbsp;— the maximum possible $\sum\limits_{i=0}^{n}{a_i}$.</p>





```input1|2,4
3
5 100 1 30
7 1000000000 1000000000 1000000000
4 1 7 3
```




```output1
15
4000000000
-10
```



## Note

<p>In the first test case, the optimal sequence $a$ is $[0, 1, 2, 3, 4, 5]$.</p><p>In the second test case, the optimal sequence $a$ is $[0, 10^9, 0, 10^9, 0, 10^9, 0, 10^9]$.</p><p>In the third test case, the optimal sequence $a$ is $[0, -3, -6, 1, -2]$.</p>
