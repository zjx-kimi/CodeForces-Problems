## Description

<div><p>You are given $n$ strings $s_1, s_2, \dots, s_n$ of length at most $\mathbf{8}$. </p><p>For each string $s_i$, determine if there exist two strings $s_j$ and $s_k$ such that $s_i = s_j + s_k$. That is, $s_i$ is the concatenation of $s_j$ and $s_k$. Note that $j$ <span class="tex-font-style-bf">can</span> be equal to $k$.</p><p>Recall that the concatenation of strings $s$ and $t$ is $s + t = s_1 s_2 \dots s_p t_1 t_2 \dots t_q$, where $p$ and $q$ are the lengths of strings $s$ and $t$ respectively. For example, concatenation of "<span class="tex-font-style-tt">code</span>" and "<span class="tex-font-style-tt">forces</span>" is "<span class="tex-font-style-tt">codeforces</span>".</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \leq t \leq 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains a single integer $n$ ($1 \leq n \leq 10^5$)&nbsp;— the number of strings.</p><p>Then $n$ lines follow, the $i$-th of which contains non-empty string $s_i$ of length at most $\mathbf{8}$, consisting of lowercase English letters. Among the given $n$ strings, there may be equal (duplicates).</p><p>The sum of $n$ over all test cases doesn't exceed $10^5$.</p></div><div class="output-specification"><p>For each test case, output a binary string of length $n$. The $i$-th bit should be $\texttt{1}$ if there exist two strings $s_j$ and $s_k$ where $s_i = s_j + s_k$, and $\texttt{0}$ otherwise. Note that $j$ can be equal to $k$.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \leq t \leq 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains a single integer $n$ ($1 \leq n \leq 10^5$)&nbsp;— the number of strings.</p><p>Then $n$ lines follow, the $i$-th of which contains non-empty string $s_i$ of length at most $\mathbf{8}$, consisting of lowercase English letters. Among the given $n$ strings, there may be equal (duplicates).</p><p>The sum of $n$ over all test cases doesn't exceed $10^5$.</p>

## Output

<p>For each test case, output a binary string of length $n$. The $i$-th bit should be $\texttt{1}$ if there exist two strings $s_j$ and $s_k$ where $s_i = s_j + s_k$, and $\texttt{0}$ otherwise. Note that $j$ can be equal to $k$.</p>





```input1|2,3,4,5,6,7,12,13,14,15,16,17,18,19,20
3
5
abab
ab
abc
abacb
c
3
x
xx
xxx
8
codeforc
es
codes
cod
forc
forces
e
code
```




```output1
10100
011
10100101
```



## Note

<p>In the first test case, we have the following: </p><ul> <li> $s_1 = s_2 + s_2$, since $\texttt{abab} = \texttt{ab} + \texttt{ab}$. Remember that $j$ can be equal to $k$. </li><li> $s_2$ is not the concatenation of any two strings in the list. </li><li> $s_3 = s_2 + s_5$, since $\texttt{abc} = \texttt{ab} + \texttt{c}$. </li><li> $s_4$ is not the concatenation of any two strings in the list. </li><li> $s_5$ is not the concatenation of any two strings in the list. </li></ul> Since only $s_1$ and $s_3$ satisfy the conditions, only the first and third bits in the answer should be $\texttt{1}$, so the answer is $\texttt{10100}$.
