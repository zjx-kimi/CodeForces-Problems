## Description

<div><p>You are given an array $a_1, a_2, \ldots, a_n$. Initially, $a_i=i$ for each $1 \le i \le n$.</p><p>The operation $\texttt{swap}(k)$ for an integer $k \ge 2$ is defined as follows: </p><ul> <li> Let $d$ be the largest divisor$^\dagger$ of $k$ which is not equal to $k$ itself. Then swap the elements $a_d$ and $a_k$. </li></ul><p>Suppose you perform $\texttt{swap}(i)$ for each $i=2,3,\ldots, n$ in this exact order. Find the position of $1$ in the resulting array. In other words, find such $j$ that $a_j = 1$ after performing these operations.</p><p>$^\dagger$ An integer $x$ is a divisor of $y$ if there exists an integer $z$ such that $y = x \cdot z$.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^4$). The description of the test cases follows.</p><p>The only line of each test case contains one integer $n$ ($1 \le n \le 10^9$)&nbsp;— the length of the array $a$.</p></div><div class="output-specification"><p>For each test case, output the position of $1$ in the resulting array.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^4$). The description of the test cases follows.</p><p>The only line of each test case contains one integer $n$ ($1 \le n \le 10^9$)&nbsp;— the length of the array $a$.</p>

## Output

<p>For each test case, output the position of $1$ in the resulting array.</p>





```input1|2,4
4
1
4
5
120240229
```




```output1
1
4
4
67108864
```



## Note

<p>In the first test case, the array is $[1]$ and there are no operations performed.</p><p>In the second test case, $a$ changes as follows:</p><ul> <li> Initially, $a$ is $[1,2,3,4]$. </li><li> After performing $\texttt{swap}(2)$, $a$ changes to $[\underline{2},\underline{1},3,4]$ (the elements being swapped are underlined). </li><li> After performing $\texttt{swap}(3)$, $a$ changes to $[\underline{3},1,\underline{2},4]$. </li><li> After performing $\texttt{swap}(4)$, $a$ changes to $[3,\underline{4},2,\underline{1}]$. </li></ul><p>Finally, the element $1$ lies on index $4$ (that is, $a_4 = 1$). Thus, the answer is $4$.</p>
