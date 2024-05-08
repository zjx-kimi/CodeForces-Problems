## Description

<div><center> <img class="tex-graphics" height="302px" src="file://Ojfwi60n.png" style="max-width: 100.0%;max-height: 100.0%;" width="454px"> </center><p>William has two arrays of numbers $a_1, a_2, \dots, a_n$ and $b_1, b_2, \dots, b_m$. The arrays satisfy the conditions of being convex. Formally an array $c$ of length $k$ is considered convex if $c_i - c_{i - 1} &lt; c_{i + 1} - c_i$ for all $i$ from $2$ to $k - 1$ and $c_1 &lt; c_2$.</p><p>Throughout William's life he observed $q$ changes of two types happening to the arrays: </p><ol> <li> Add the arithmetic progression $d, d \cdot 2, d \cdot 3, \dots, d \cdot k$ to the suffix of the array $a$ of length $k$. The array after the change looks like this: $[a_1, a_2, \dots, a_{n - k}, a_{n - k + 1} + d, a_{n - k + 2} + d \cdot 2, \dots, a_n + d \cdot k]$. </li><li> The same operation, but for array $b$. </li></ol><p>After each change a matrix $d$ is created from arrays $a$ and $b$, of size $n \times m$, where $d_{i, j}=a_i + b_j$. William wants to get from cell ($1, 1$) to cell ($n, m$) of this matrix. From cell ($x, y$) he can only move to cells ($x + 1, y$) and ($x, y + 1$). The length of a path is calculated as the sum of numbers in cells visited by William, including the first and the last cells.</p><p>After each change William wants you to help find out the minimal length of the path he could take.</p></div><div class="input-specification"><p>The first line contains three integers $n$, $m$ and $q$ ($2 \le n \le 100, 2 \le m \le 10^5$, $1 \le q \le 10^5$), the sizes of the arrays and the number of changes.</p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le 10^{12}$), the contents of array $a$.</p><p>The third line contains $m$ integers $b_1, b_2, \dots, b_m$ ($1 \le b_i \le 10^{12}$), the contents of array $b$.</p><p>Each of the next $q$ lines contains three integers $type$, $k$ and $d$ ($1 \le type \le 2$, if $type = 1$, then $1 \le k \le n$ otherwise $1 \le k \le m$, $1 \le d \le 10^3$).</p></div><div class="output-specification"><p>After each change, output one integer, the minimum length of the path in the constructed matrix.</p></div>

## Input

<p>The first line contains three integers $n$, $m$ and $q$ ($2 \le n \le 100, 2 \le m \le 10^5$, $1 \le q \le 10^5$), the sizes of the arrays and the number of changes.</p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le 10^{12}$), the contents of array $a$.</p><p>The third line contains $m$ integers $b_1, b_2, \dots, b_m$ ($1 \le b_i \le 10^{12}$), the contents of array $b$.</p><p>Each of the next $q$ lines contains three integers $type$, $k$ and $d$ ($1 \le type \le 2$, if $type = 1$, then $1 \le k \le n$ otherwise $1 \le k \le m$, $1 \le d \le 10^3$).</p>

## Output

<p>After each change, output one integer, the minimum length of the path in the constructed matrix.</p>





```input1
5 3 4
1 2 4 7 11
5 7 10
1 3 2
2 2 5
1 5 4
2 1 7
```




```input2
5 6 7
4 9 22 118 226
7 94 238 395 565 738
2 1 95
1 4 54
1 2 5
1 2 87
2 6 62
2 1 143
1 1 77
```




```output1
98
128
219
229
```




```output2
3639
5122
5162
5617
7663
7806
7960
```


