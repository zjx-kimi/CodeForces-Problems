## Description

<div><p>You are given a two-dimensional plane, and you need to place $n$ chips on it. </p><p>You can place a chip only at a point with integer coordinates. The cost of placing a chip at the point $(x, y)$ is equal to $|x| + |y|$ (where $|a|$ is the absolute value of $a$).</p><p>The cost of placing $n$ chips is equal to the <span class="tex-font-style-bf">maximum</span> among the costs of each chip.</p><p>You need to place $n$ chips on the plane in such a way that the Euclidean distance between each pair of chips is <span class="tex-font-style-bf">strictly greater</span> than $1$, and the cost is the minimum possible.</p></div><div class="input-specification"><p>The first line contains one integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. Next $t$ cases follow.</p><p>The first and only line of each test case contains one integer $n$ ($1 \le n \le 10^{18}$)&nbsp;— the number of chips you need to place.</p></div><div class="output-specification"><p>For each test case, print a single integer&nbsp;— the minimum cost to place $n$ chips if the distance between each pair of chips must be strictly greater than $1$.</p></div>

## Input

<p>The first line contains one integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. Next $t$ cases follow.</p><p>The first and only line of each test case contains one integer $n$ ($1 \le n \le 10^{18}$)&nbsp;— the number of chips you need to place.</p>

## Output

<p>For each test case, print a single integer&nbsp;— the minimum cost to place $n$ chips if the distance between each pair of chips must be strictly greater than $1$.</p>





```input1|2,4
4
1
3
5
975461057789971042
```




```output1
0
1
2
987654321
```



## Note

<p>In the first test case, you can place the only chip at point $(0, 0)$ with total cost equal to $0 + 0 = 0$.</p><p>In the second test case, you can, for example, place chips at points $(-1, 0)$, $(0, 1)$ and $(1, 0)$ with costs $|-1| + |0| = 1$, $|0| + |1| = 1$ and $|0| + |1| = 1$. Distance between each pair of chips is greater than $1$ (for example, distance between $(-1, 0)$ and $(0, 1)$ is equal to $\sqrt{2}$). The total cost is equal to $\max(1, 1, 1) = 1$.</p><p>In the third test case, you can, for example, place chips at points $(-1, -1)$, $(-1, 1)$, $(1, 1)$, $(0, 0)$ and $(0, 2)$. The total cost is equal to $\max(2, 2, 2, 0, 2) = 2$.</p>
