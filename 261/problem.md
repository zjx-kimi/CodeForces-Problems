## Description

<div><p>Qingshan has a string $s$ which only contains $\texttt{0}$ and $\texttt{1}$.</p><p>A string $a$ of length $k$ is good if and only if</p><ul> <li> $a_i \ne a_{k-i+1}$ for all $i=1,2,\ldots,k$. </li></ul><p><span class="tex-font-size-small">For Div. 2 contestants, note that this condition is different from the condition in problem B.</span></p><p>For example, $\texttt{10}$, $\texttt{1010}$, $\texttt{111000}$ are good, while $\texttt{11}$, $\texttt{101}$, $\texttt{001}$, $\texttt{001100}$ are not good.</p><p>Qingshan wants to make $s$ good. To do this, she can do the following operation <span class="tex-font-style-bf">at most</span> $300$ times (possibly, zero): </p><ul> <li> insert $\texttt{01}$ to any position of $s$ (getting a new $s$). </li></ul><p>Please tell Qingshan if it is possible to make $s$ good. If it is possible, print a sequence of operations that makes $s$ good.</p></div><div class="input-specification"><p>The input consists of multiple test cases. The first line contains a single integer $t$ ($1\le t\le 100$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n\le 100$)&nbsp;— the length of string $s$, respectively.</p><p>The second line of each test case contains a string $s$ with length $n$.</p><p>It is guaranteed that $s$ only consists of $\texttt{0}$ and $\texttt{1}$.</p></div><div class="output-specification"><p>For each test case, if it impossible to make $s$ good, output $-1$.</p><p>Otherwise, output $p$ ($0 \le p \le 300$)&nbsp;— the number of operations, in the first line.</p><p>Then, output $p$ integers in the second line. The $i$-th integer should be an index $x_i$ ($0 \le x_i \le n+2i-2$)&nbsp;— the position where you want to insert $\texttt{01}$ in the current $s$. If $x_i=0$, you insert $\texttt{01}$ at the beginning of $s$. Otherwise, you insert $\texttt{01}$ immediately after the $x_i$-th character of $s$.</p><p>We can show that under the constraints in this problem, if an answer exists, there is always an answer that requires at most $300$ operations.</p></div>

## Input

<p>The input consists of multiple test cases. The first line contains a single integer $t$ ($1\le t\le 100$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n\le 100$)&nbsp;— the length of string $s$, respectively.</p><p>The second line of each test case contains a string $s$ with length $n$.</p><p>It is guaranteed that $s$ only consists of $\texttt{0}$ and $\texttt{1}$.</p>

## Output

<p>For each test case, if it impossible to make $s$ good, output $-1$.</p><p>Otherwise, output $p$ ($0 \le p \le 300$)&nbsp;— the number of operations, in the first line.</p><p>Then, output $p$ integers in the second line. The $i$-th integer should be an index $x_i$ ($0 \le x_i \le n+2i-2$)&nbsp;— the position where you want to insert $\texttt{01}$ in the current $s$. If $x_i=0$, you insert $\texttt{01}$ at the beginning of $s$. Otherwise, you insert $\texttt{01}$ immediately after the $x_i$-th character of $s$.</p><p>We can show that under the constraints in this problem, if an answer exists, there is always an answer that requires at most $300$ operations.</p>





```input1|2,3,6,7,10,11
6
2
01
3
000
4
1111
6
001110
10
0111001100
3
001
```




```output1
0

-1
-1
2
6 7
1
10
-1
```



## Note

<p>In the first test case, you can do zero operations and get $s=\texttt{01}$, which is good.</p><p>Another valid solution is to do one operation: (the inserted $\texttt{01}$ is underlined)</p><ol> <li> $\texttt{0}\underline{\texttt{01}}\texttt{1}$ </li></ol><p>and get $s = \texttt{0011}$, which is good.</p><p>In the second and the third test case, it is impossible to make $s$ good.</p><p>In the fourth test case, you can do two operations:</p><ol> <li> $\texttt{001110}\underline{\texttt{01}}$ </li><li> $\texttt{0011100}\underline{\texttt{01}}\texttt{1}$ </li></ol><p>and get $s = \texttt{0011100011}$, which is good.</p>
