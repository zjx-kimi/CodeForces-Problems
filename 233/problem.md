## Description

<div><p>Qingshan has a string $s$, while Daniel has a string $t$. Both strings only contain $\texttt{0}$ and $\texttt{1}$.</p><p>A string $a$ of length $k$ is good if and only if</p><ul> <li> $a_i \ne a_{i+1}$ for all $i=1,2,\ldots,k-1$. </li></ul><p>For example, $\texttt{1}$, $\texttt{101}$, $\texttt{0101}$ are good, while $\texttt{11}$, $\texttt{1001}$, $\texttt{001100}$ are not good.</p><p>Qingshan wants to make $s$ good. To do this, she can do the following operation any number of times (possibly, zero):</p><ul> <li> insert $t$ to any position of $s$ (getting a new $s$). </li></ul><p>Please tell Qingshan if it is possible to make $s$ good.</p></div><div class="input-specification"><p>The input consists of multiple test cases. The first line contains a single integer $T$ ($1\le T\le 2000$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $m$ ($1 \le n,m \le 50$)&nbsp;— the length of the strings $s$ and $t$, respectively.</p><p>The second line of each test case contains a string $s$ of length $n$.</p><p>The third line of each test case contains a string $t$ of length $m$.</p><p>It is guaranteed that $s$ and $t$ only contain $\texttt{0}$ and $\texttt{1}$.</p></div><div class="output-specification"><p>For each test case, print "<span class="tex-font-style-tt">YES</span>" (without quotes), if it is possible to make $s$ good, and "<span class="tex-font-style-tt">NO</span>" (without quotes) otherwise.</p><p>You can print letters in any case (upper or lower).</p></div>

## Input

<p>The input consists of multiple test cases. The first line contains a single integer $T$ ($1\le T\le 2000$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $m$ ($1 \le n,m \le 50$)&nbsp;— the length of the strings $s$ and $t$, respectively.</p><p>The second line of each test case contains a string $s$ of length $n$.</p><p>The third line of each test case contains a string $t$ of length $m$.</p><p>It is guaranteed that $s$ and $t$ only contain $\texttt{0}$ and $\texttt{1}$.</p>

## Output

<p>For each test case, print "<span class="tex-font-style-tt">YES</span>" (without quotes), if it is possible to make $s$ good, and "<span class="tex-font-style-tt">NO</span>" (without quotes) otherwise.</p><p>You can print letters in any case (upper or lower).</p>





```input1|2,3,4,8,9,10,14,15,16
5
1 1
1
0
3 3
111
010
3 2
111
00
6 7
101100
1010101
10 2
1001001000
10
```




```output1
Yes
Yes
No
No
No
```



## Note

<p>In the first test case, $s$ is good initially, so you can get a good $s$ by doing zero operations.</p><p>In the second test case, you can do the following two operations (the inserted string $t$ is underlined):</p><ol> <li> $\texttt{1}\underline{\texttt{010}}\texttt{11}$ </li><li> $\texttt{10101}\underline{\texttt{010}}\texttt{1}$ </li></ol><p>and get $s = \texttt{101010101}$, which is good.</p><p>In the third test case, there is no way to make $s$ good after any number of operations.</p>
