## Description

<div><p>You are given an array $a$ of $n$ positive integers. In one operation, you must pick some $(i, j)$ such that $1\leq i &lt; j\leq |a|$ and append $|a_i - a_j|$ to the end of the $a$ (i.e. increase $n$ by $1$ and set $a_n$ to $|a_i - a_j|$). Your task is to minimize and print the minimum value of $a$ after performing $k$ operations.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains an integer $t$ ($1 \leq t \leq 1000$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $k$ ($2\le n\le 2\cdot 10^3$, $1\le k\le 10^9$)&nbsp;— the length of the array and the number of operations you should perform.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1\le a_i\le 10^{18}$)&nbsp;— the elements of the array $a$.</p><p>It is guaranteed that the sum of $n^2$ over all test cases does not exceed $4\cdot 10^6$.</p></div><div class="output-specification"><p>For each test case, print a single integer&nbsp;— the smallest possible value of the minimum of array $a$ after performing $k$ operations.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains an integer $t$ ($1 \leq t \leq 1000$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $k$ ($2\le n\le 2\cdot 10^3$, $1\le k\le 10^9$)&nbsp;— the length of the array and the number of operations you should perform.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1\le a_i\le 10^{18}$)&nbsp;— the elements of the array $a$.</p><p>It is guaranteed that the sum of $n^2$ over all test cases does not exceed $4\cdot 10^6$.</p>

## Output

<p>For each test case, print a single integer&nbsp;— the smallest possible value of the minimum of array $a$ after performing $k$ operations.</p>





```input1|2,3,6,7
4
5 2
3 9 7 15 1
4 3
7 4 15 12
6 2
42 47 50 54 62 79
2 1
500000000000000000 1000000000000000000
```




```output1
1
0
3
500000000000000000
```



## Note

<p>In the first test case, after any $k=2$ operations, the minimum value of $a$ will be $1$.</p><p>In the second test case, an optimal strategy is to first pick $i=1, j=2$ and append $|a_1 - a_2| = 3$ to the end of $a$, creating $a=[7, 4, 15, 12, 3]$. Then, pick $i=3, j=4$ and append $|a_3 - a_4| = 3$ to the end of $a$, creating $a=[7, 4, 15, 12, 3, 3]$. In the final operation, pick $i=5, j=6$ and append $|a_5 - a_6| = 0$ to the end of $a$. Then the minimum value of $a$ will be $0$.</p><p>In the third test case, an optimal strategy is to first pick $i=2, j=3$ to append $|a_2 - a_3| = 3$ to the end of $a$. Any second operation will still not make the minimum value of $a$ be less than $3$.</p>
