## Description

<div><p>You are given a tree with $n$ vertices, whose vertices are numbered from $1$ to $n$. Each edge is labeled with some integer $w_i$.</p><p>Define $len(u, v)$ as the number of edges in the simple path between vertices $u$ and $v$, and $gcd(u, v)$ as the Greatest Common Divisor of all numbers written on the edges of the simple path between vertices $u$ and $v$. For example, $len(u, u) = 0$ and $gcd(u, u) = 0$ for any $1 \leq u \leq n$.</p><p>You need to find the maximum value of $len(u, v) \cdot gcd(u, v)$ over all pairs of vertices in the tree.</p></div><div class="input-specification"><p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 10^4$)&nbsp;— the number of test cases. This is followed by their description.</p><p>The first line of each test case contains the number $n$ ($2 \leq n \leq 10^5$)&nbsp;— the number of vertices in the tree.</p><p>The next $n-1$ lines specify the edges in the format $u$, $v$, $w$ ($1 \leq u, v \leq n$, $1 \leq w \leq 10^{12}$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p></div><div class="output-specification"><p>For each test case, output a single number equal to the maximum value of $len(u, v) \cdot gcd(u, v)$ over all pairs of vertices in the tree.</p></div>

## Input

<p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 10^4$)&nbsp;— the number of test cases. This is followed by their description.</p><p>The first line of each test case contains the number $n$ ($2 \leq n \leq 10^5$)&nbsp;— the number of vertices in the tree.</p><p>The next $n-1$ lines specify the edges in the format $u$, $v$, $w$ ($1 \leq u, v \leq n$, $1 \leq w \leq 10^{12}$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p>

## Output

<p>For each test case, output a single number equal to the maximum value of $len(u, v) \cdot gcd(u, v)$ over all pairs of vertices in the tree.</p>





```input1|2,3,8,9,10,11,12,13,14,15
4
2
1 2 1000000000000
4
3 2 6
2 1 10
2 4 6
8
1 2 12
2 3 9
3 4 9
4 5 6
5 6 12
6 7 4
7 8 9
12
1 2 12
2 3 12
2 4 6
2 5 9
5 6 6
1 7 4
4 8 12
8 9 4
8 10 12
2 11 9
7 12 9
```




```output1
1000000000000
12
18
24
```


