## Description

<div><p>You are given a string $s$ of length $n$ consisting of characters $\texttt{A}$ and $\texttt{B}$. You are allowed to do the following operation:</p><ul> <li> Choose an index $1 \le i \le n - 1$ such that $s_i = \texttt{A}$ and $s_{i + 1} = \texttt{B}$. Then, swap $s_i$ and $s_{i+1}$. </li></ul><p>You are only allowed to do the operation <span class="tex-font-style-bf">at most once</span> for each index $1 \le i \le n - 1$. However, you can do it in any order you want. Find the maximum number of operations that you can carry out. </p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 1000$). Description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2 \le n \le 2\cdot 10^5$)&nbsp;— the length of string $s$.</p><p>The second line of each test case contains the string $s$ ($s_i=\texttt{A}$ or $s_i=\texttt{B}$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2\cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, print a single integer containing the maximum number of operations that you can carry out.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 1000$). Description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2 \le n \le 2\cdot 10^5$)&nbsp;— the length of string $s$.</p><p>The second line of each test case contains the string $s$ ($s_i=\texttt{A}$ or $s_i=\texttt{B}$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2\cdot 10^5$.</p>

## Output

<p>For each test case, print a single integer containing the maximum number of operations that you can carry out.</p>





```input1|2,3,6,7
3
2
AB
4
BBBA
4
AABB
```




```output1
1
0
3
```



## Note

<p>In the first test case, we can do the operation exactly once for $i=1$ as $s_1=\texttt{A}$ and $s_2=\texttt{B}$.</p><p>In the second test case, it can be proven that it is not possible to do an operation.</p><p>In the third test case, we can do an operation on $i=2$ to form $\texttt{ABAB}$, then another operation on $i=3$ to form $\texttt{ABBA}$, and finally another operation on $i=1$ to form $\texttt{BABA}$. Note that even though at the end, $s_2 = \texttt{A}$ and $s_3 = \texttt{B}$, we cannot do an operation on $i=2$ again as we can only do the operation at most once for each index.</p>
