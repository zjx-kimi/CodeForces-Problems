## Description

<div><p>You are given two integers $a$ and $b$, and $q$ queries. The $i$-th query consists of two numbers $l_i$ and $r_i$, and the answer to it is the number of integers $x$ such that $l_i \le x \le r_i$, and $((x \bmod a) \bmod b) \ne ((x \bmod b) \bmod a)$. Calculate the answer for each query.</p><p>Recall that $y \bmod z$ is the remainder of the division of $y$ by $z$. For example, $5 \bmod 3 = 2$, $7 \bmod 8 = 7$, $9 \bmod 4 = 1$, $9 \bmod 9 = 0$.</p></div><div class="input-specification"><p>The first line contains one integer $t$ ($1 \le t \le 100$)&nbsp;— the number of test cases. Then the test cases follow.</p><p>The first line of each test case contains three integers $a$, $b$ and $q$ ($1 \le a, b \le 200$; $1 \le q \le 500$).</p><p>Then $q$ lines follow, each containing two integers $l_i$ and $r_i$ ($1 \le l_i \le r_i \le 10^{18}$) for the corresponding query.</p></div><div class="output-specification"><p>For each test case, print $q$ integers&nbsp;— the answers to the queries of this test case in the order they appear.</p></div>

## Input

<p>The first line contains one integer $t$ ($1 \le t \le 100$)&nbsp;— the number of test cases. Then the test cases follow.</p><p>The first line of each test case contains three integers $a$, $b$ and $q$ ($1 \le a, b \le 200$; $1 \le q \le 500$).</p><p>Then $q$ lines follow, each containing two integers $l_i$ and $r_i$ ($1 \le l_i \le r_i \le 10^{18}$) for the corresponding query.</p>

## Output

<p>For each test case, print $q$ integers&nbsp;— the answers to the queries of this test case in the order they appear.</p>





```input1
2
4 6 5
1 1
1 3
1 5
1 7
1 9
7 10 2
7 8
100 200
```




```output1
0 0 0 2 4 
0 91
```


