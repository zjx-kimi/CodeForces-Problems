## Description

<div><p>You are given an array of integers $a$ of length $n$.</p><p>In one operation you: </p><ul> <li> Choose an index $i$ such that $1 \le i \le n - 1$ and $a_i \le a_{i + 1}$. </li><li> Increase $a_i$ by $1$. </li></ul><p>Find the maximum possible value of $\max(a_1, a_2, \ldots a_n)$ that you can get after performing this operation at most $k$ times.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line of input contains a single integer $t$ ($1 \le t \le 100$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $k$ ($2 \le n \le 1000$, $1 \le k \le 10^{8}$)&nbsp;— the length of the array $a$ and the maximum number of operations that can be performed.</p><p>The second line of each test case contains $n$ integers $a_1,a_2,\ldots,a_n$ ($1 \le a_i \le 10^{8}$)&nbsp;— the elements of the array $a$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $1000$.</p></div><div class="output-specification"><p>For each test case output a single integer&nbsp;— the maximum possible maximum of the array after performing at most $k$ operations.</p></div>

## Input

<p>Each test contains multiple test cases. The first line of input contains a single integer $t$ ($1 \le t \le 100$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $k$ ($2 \le n \le 1000$, $1 \le k \le 10^{8}$)&nbsp;— the length of the array $a$ and the maximum number of operations that can be performed.</p><p>The second line of each test case contains $n$ integers $a_1,a_2,\ldots,a_n$ ($1 \le a_i \le 10^{8}$)&nbsp;— the elements of the array $a$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $1000$.</p>

## Output

<p>For each test case output a single integer&nbsp;— the maximum possible maximum of the array after performing at most $k$ operations.</p>





```input1|2,3,6,7,10,11
6
3 4
1 3 3
5 6
1 3 4 5 1
4 13
1 1 3 179
5 3
4 3 2 2 2
5 6
6 5 4 1 5
2 17
3 5
```




```output1
4
7
179
5
7
6
```



## Note

<p>In the first test case, one possible optimal sequence of operations is: $[\color{red}{1}, 3, 3] \rightarrow [2, \color{red}{3}, 3] \rightarrow [\color{red}{2}, 4, 3] \rightarrow [\color{red}{3}, 4, 3] \rightarrow [4, 4, 3]$.</p><p>In the second test case, one possible optimal sequence of operations is: $[1, \color{red}{3}, 4, 5, 1] \rightarrow [1, \color{red}{4}, 4, 5, 1] \rightarrow [1, 5, \color{red}{4}, 5, 1] \rightarrow [1, 5, \color{red}{5}, 5, 1] \rightarrow [1, \color{red}{5}, 6, 5, 1] \rightarrow [1, \color{red}{6}, 6, 5, 1] \rightarrow [1, 7, 6, 5, 1]$.</p>
