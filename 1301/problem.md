## Description

<div><p>Mark has just purchased a rack of $n$ lightbulbs. The state of the lightbulbs can be described with binary string $s = s_1s_2\dots s_n$, where $s_i=\texttt{1}$ means that the $i$-th lightbulb is turned on, while $s_i=\texttt{0}$ means that the $i$-th lightbulb is turned off.</p><p>Unfortunately, the lightbulbs are broken, and the only operation he can perform to change the state of the lightbulbs is the following:</p><ul> <li> Select an index $i$ from $2,3,\dots,n-1$ such that $s_{i-1}\ne s_{i+1}$. </li><li> Toggle $s_i$. Namely, if $s_i$ is $\texttt{0}$, set $s_i$ to $\texttt{1}$ or vice versa. </li></ul><p>Mark wants the state of the lightbulbs to be another binary string $t$. Help Mark determine the minimum number of operations to do so.</p></div><div class="input-specification"><p>The first line of the input contains a single integer $q$ ($1\leq q\leq 10^4$) — the number of test cases.</p><p>The first line of each test case contains a single integer $n$ ($3\leq n\leq 2\cdot 10^5$) — the number of lightbulbs.</p><p>The second line of each test case contains a binary string $s$ of length $n$ — the initial state of the lightbulbs.</p><p>The third line of each test case contains a binary string $t$ of length $n$ — the final state of the lightbulbs.</p><p>It is guaranteed that the sum of $n$ across all test cases does not exceed $2\cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, print a line containing the minimum number of operations Mark needs to perform to transform $s$ to $t$. If there is no such sequence of operations, print $-1$.</p></div>

## Input

<p>The first line of the input contains a single integer $q$ ($1\leq q\leq 10^4$) — the number of test cases.</p><p>The first line of each test case contains a single integer $n$ ($3\leq n\leq 2\cdot 10^5$) — the number of lightbulbs.</p><p>The second line of each test case contains a binary string $s$ of length $n$ — the initial state of the lightbulbs.</p><p>The third line of each test case contains a binary string $t$ of length $n$ — the final state of the lightbulbs.</p><p>It is guaranteed that the sum of $n$ across all test cases does not exceed $2\cdot 10^5$.</p>

## Output

<p>For each test case, print a line containing the minimum number of operations Mark needs to perform to transform $s$ to $t$. If there is no such sequence of operations, print $-1$.</p>





```input1|2,3,4,8,9,10
4
4
0100
0010
4
1010
0100
5
01001
00011
6
000101
010011
```




```output1
2
-1
-1
5
```



## Note

<p>In the first test case, one sequence of operations that achieves the minimum number of operations is the following. </p><ul> <li> Select $i=3$, changing $\texttt{01}\color{red}{\texttt{0}}\texttt{0}$ to $\texttt{01}\color{red}{\texttt{1}}\texttt{0}$. </li><li> Select $i=2$, changing $\texttt{0}\color{red}{\texttt{1}}\texttt{10}$ to $\texttt{0}\color{red}{\texttt{0}}\texttt{10}$. </li></ul> In the second test case, there is no sequence of operations because one cannot change the first digit or the last digit of $s$.<p>In the third test case, even though the first digits of $s$ and $t$ are the same and the last digits of $s$ and $t$ are the same, it can be shown that there is no sequence of operations that satisfies the condition.</p><p>In the fourth test case, one sequence that achieves the minimum number of operations is the following: </p><ul> <li> Select $i=3$, changing $\texttt{00}\color{red}{\texttt{0}}\texttt{101}$ to $\texttt{00}\color{red}{\texttt{1}}\texttt{101}$. </li><li> Select $i=2$, changing $\texttt{0}\color{red}{\texttt{0}}\texttt{1101}$ to $\texttt{0}\color{red}{\texttt{1}}\texttt{1101}$. </li><li> Select $i=4$, changing $\texttt{011}\color{red}{\texttt{1}}\texttt{01}$ to $\texttt{011}\color{red}{\texttt{0}}\texttt{01}$. </li><li> Select $i=5$, changing $\texttt{0110}\color{red}{\texttt{0}}\texttt{1}$ to $\texttt{0110}\color{red}{\texttt{1}}\texttt{1}$. </li><li> Select $i=3$, changing $\texttt{01}\color{red}{\texttt{1}}\texttt{011}$ to $\texttt{01}\color{red}{\texttt{0}}\texttt{011}$. </li></ul>
