## Description

<div><p>A binary string is a string that consists of characters $0$ and $1$. A bi-table is a table that has exactly two rows of equal length, each being a binary string.</p><p>Let $\operatorname{MEX}$ of a bi-table be the smallest digit among $0$, $1$, or $2$ that does not occur in the bi-table. For example, $\operatorname{MEX}$ for $\begin{bmatrix} 0011\\ 1010 \end{bmatrix}$ is $2$, because $0$ and $1$ occur in the bi-table at least once. $\operatorname{MEX}$ for $\begin{bmatrix} 111\\ 111 \end{bmatrix}$ is $0$, because $0$ and $2$ do not occur in the bi-table, and $0 &lt; 2$.</p><p>You are given a bi-table with $n$ columns. You should cut it into any number of bi-tables (each consisting of consecutive columns) so that each column is in exactly one bi-table. It is possible to cut the bi-table into a single bi-table — the whole bi-table.</p><p>What is the <span class="tex-font-style-bf">maximal</span> sum of $\operatorname{MEX}$ of all resulting bi-tables can be?</p></div><div class="input-specification"><p>The input consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 10^4$) — the number of test cases. Description of the test cases follows.</p><p>The first line of the description of each test case contains a single integer $n$ ($1 \le n \le 10^5$)&nbsp;— the number of columns in the bi-table.</p><p>Each of the next two lines contains a binary string of length $n$&nbsp;— the rows of the bi-table.</p><p>It's guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p></div><div class="output-specification"><p>For each test case print a single integer&nbsp;— the maximal sum of $\operatorname{MEX}$ of all bi-tables that it is possible to get by cutting the given bi-table optimally.</p></div>

## Input

<p>The input consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 10^4$) — the number of test cases. Description of the test cases follows.</p><p>The first line of the description of each test case contains a single integer $n$ ($1 \le n \le 10^5$)&nbsp;— the number of columns in the bi-table.</p><p>Each of the next two lines contains a binary string of length $n$&nbsp;— the rows of the bi-table.</p><p>It's guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p>

## Output

<p>For each test case print a single integer&nbsp;— the maximal sum of $\operatorname{MEX}$ of all bi-tables that it is possible to get by cutting the given bi-table optimally.</p>





```input1
4
7
0101000
1101100
5
01100
10101
2
01
01
6
000000
111111
```




```output1
8
8
2
12
```



## Note

<p>In the first test case you can cut the bi-table as follows:</p><ul> <li> $\begin{bmatrix} 0\\ 1 \end{bmatrix}$, its $\operatorname{MEX}$ is $2$.</li><li> $\begin{bmatrix} 10\\ 10 \end{bmatrix}$, its $\operatorname{MEX}$ is $2$.</li><li> $\begin{bmatrix} 1\\ 1 \end{bmatrix}$, its $\operatorname{MEX}$ is $0$.</li><li> $\begin{bmatrix} 0\\ 1 \end{bmatrix}$, its $\operatorname{MEX}$ is $2$.</li><li> $\begin{bmatrix} 0\\ 0 \end{bmatrix}$, its $\operatorname{MEX}$ is $1$.</li><li> $\begin{bmatrix} 0\\ 0 \end{bmatrix}$, its $\operatorname{MEX}$ is $1$.</li></ul><p>The sum of $\operatorname{MEX}$ is $8$.</p>
