## Description

<div><p>You are given two positive integers $n$ and $k$. </p><p>Your task is to find a string $s$ such that all possible strings of length $n$ that can be formed using the first $k$ lowercase English alphabets occur as a subsequence of $s$. </p><p>If there are multiple answers, print the one with the smallest length. If there are still multiple answers, you may print any of them.</p><p><span class="tex-font-style-bf">Note:</span> A string $a$ is called a subsequence of another string $b$ if $a$ can be obtained by deleting some (possibly zero) characters from $b$ without changing the order of the remaining characters.</p></div><div class="input-specification"><p>The first line of input contains a single integer $t$ ($1\leq t\leq 676$) denoting the number of test cases.</p><p>Each test case consists of a single line of input containing two integers $n$ ($1\leq n\leq 26$) and $k$ ($1\leq k\leq 26$).</p></div><div class="output-specification"><p>For each test case, print a single line containing a single string $s$ which satisfies the above property. If there are multiple answers, print the one with the smallest length. If there are still multiple answers, you may print any of them.</p></div>

## Input

<p>The first line of input contains a single integer $t$ ($1\leq t\leq 676$) denoting the number of test cases.</p><p>Each test case consists of a single line of input containing two integers $n$ ($1\leq n\leq 26$) and $k$ ($1\leq k\leq 26$).</p>

## Output

<p>For each test case, print a single line containing a single string $s$ which satisfies the above property. If there are multiple answers, print the one with the smallest length. If there are still multiple answers, you may print any of them.</p>





```input1|2,4
4
1 2
2 1
2 2
2 3
```




```output1
ab
aa
baab
abcbac
```



## Note

<p>For the first test case, there are two strings of length $1$ which can be formed using the first $2$ lowercase English alphabets, and they are present in $s$ as a subsequence as follows: </p><ul> <li> $\texttt{a}: {\color{red}{\texttt{a}}}\texttt{b}$ </li><li> $\texttt{b}: \texttt{a}{\color{red}{\texttt{b}}}$ </li></ul><p>For the second test case, there is only one string of length $2$ which can be formed using the first lowercase English alphabet, and it is present in $s$ as a subsequence as follows: </p><ul> <li> $\texttt{aa}: {\color{red}{\texttt{aa}}}$ </li></ul><p>For the third test case, there are $4$ strings of length $2$ which can be formed using the first $2$ lowercase English alphabets, and they are present in $s$ as a subsequence as follows: </p><ul> <li> $\texttt{aa}: \texttt{b}{\color{red}{\texttt{aa}}}\texttt{b}$ </li><li> $\texttt{ab}: \texttt{ba}{\color{red}{\texttt{ab}}}$ </li><li> $\texttt{ba}: {\color{red}{\texttt{ba}}}\texttt{ab}$ </li><li> $\texttt{bb}: {\color{red}{\texttt{b}}}\texttt{aa}{\color{red}{\texttt{b}}}$ </li></ul><p>For the fourth test case, there are $9$ strings of length $2$ which can be formed using the first $3$ lowercase English alphabets, and they are present in $s$ as a subsequence as follows: </p><ul> <li> $\texttt{aa}: {\color{red}{\texttt{a}}}\texttt{bcb}{\color{red}{\texttt{a}}}\texttt{c}$ </li><li> $\texttt{ab}: {\color{red}{\texttt{ab}}}\texttt{cbac}$ </li><li> $\texttt{ac}: \texttt{abcb}{\color{red}{\texttt{ac}}}$ </li><li> $\texttt{ba}: \texttt{abc}{\color{red}{\texttt{ba}}}\texttt{c}$ </li><li> $\texttt{bb}: \texttt{a}{\color{red}{\texttt{b}}}\texttt{c}{\color{red}{\texttt{b}}}\texttt{ac}$ </li><li> $\texttt{bc}: \texttt{a}{\color{red}{\texttt{bc}}}\texttt{bac}$ </li><li> $\texttt{ca}: \texttt{ab}{\color{red}{\texttt{c}}}\texttt{b}{\color{red}{\texttt{a}}}\texttt{c}$ </li><li> $\texttt{cb}: \texttt{ab}{\color{red}{\texttt{cb}}}\texttt{ac}$ </li><li> $\texttt{cc}: \texttt{ab}{\color{red}{\texttt{c}}}\texttt{ba}{\color{red}{\texttt{c}}}$ </li></ul>
