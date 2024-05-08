## Description

<div><div class="epigraph"><div class="epigraph-text"><span class="tex-font-style-it"><a href="https://soundcloud.com/messi-ola/crystal-gravity-tanchiky-vs">Tanchiky &amp; Siromaru - Crystal Gravity</a></span></div><div class="epigraph-source">⠀</div></div><p>You are given two strings $s$, $t$ of length $n$, $m$, respectively. Both strings consist of lowercase letters of the English alphabet.</p><p>Count the triples $(x, y, z)$ of strings such that the following conditions are true:</p><ul> <li> $s = x+y+z$ (the symbol $+$ represents the concatenation); </li><li> $t = x+\underbrace{ y+\dots+y }_{k \text{ times}} + z$ for some integer $k$. </li></ul></div><div class="input-specification"><p>The first line contains two integers $n$ and $m$ ($1 \leq n &lt; m \leq 10^7$)&nbsp;— the length of the strings $s$ and $t$, respectively.</p><p>The second line contains the string $s$ of length $n$, consisting of lowercase letters of the English alphabet.</p><p>The third line contains the string $t$ of length $m$, consisting of lowercase letters of the English alphabet.</p></div><div class="output-specification"><p>Output a single integer: the number of valid triples $(x, y, z)$.</p></div>

## Input

<p>The first line contains two integers $n$ and $m$ ($1 \leq n &lt; m \leq 10^7$)&nbsp;— the length of the strings $s$ and $t$, respectively.</p><p>The second line contains the string $s$ of length $n$, consisting of lowercase letters of the English alphabet.</p><p>The third line contains the string $t$ of length $m$, consisting of lowercase letters of the English alphabet.</p>

## Output

<p>Output a single integer: the number of valid triples $(x, y, z)$.</p>





```input1|
4 8
abcd
abcbcbcd
```




```input2|
3 5
aaa
aaaaa
```




```input3|
12 16
abbababacaab
abbababababacaab
```




```output1
1
```




```output2
5
```




```output3
8
```



## Note

<p>In the first test case, the only valid triple is $(x, y, z) = (\texttt{"a"}, \texttt{"bc"}, \texttt{"d"})$. In fact, </p><ul> <li> $\texttt{"abcd"} = \texttt{"a"} + \texttt{"bc"} + \texttt{"d"}$; </li><li> $\texttt{"abcbcbcd"} = \texttt{"a"} + \texttt{"bc"} + \texttt{"bc"} + \texttt{"bc"} + \texttt{"d"}$. </li></ul><p>In the second test case, there are $5$ valid triples: </p><ul> <li> $(x, y, z) = (\texttt{""}, \texttt{"a"}, \texttt{"aa"})$; </li><li> $(x, y, z) = (\texttt{""}, \texttt{"aa"}, \texttt{"a"})$; </li><li> $(x, y, z) = (\texttt{"a"}, \texttt{"a"}, \texttt{"a"})$; </li><li> $(x, y, z) = (\texttt{"a"}, \texttt{"aa"}, \texttt{""})$; </li><li> $(x, y, z) = (\texttt{"aa"}, \texttt{"a"}, \texttt{""})$. </li></ul><p>In the third test case, there are $8$ valid triples: </p><ul> <li> $(x, y, z) = (\texttt{"ab"}, \texttt{"ba"}, \texttt{"babacaab"})$; </li><li> $(x, y, z) = (\texttt{"abb"}, \texttt{"ab"}, \texttt{"abacaab"})$; </li><li> $(x, y, z) = (\texttt{"abba"}, \texttt{"ba"}, \texttt{"bacaab"})$; </li><li> $(x, y, z) = (\texttt{"ab"}, \texttt{"baba"}, \texttt{"bacaab"})$; </li><li> $(x, y, z) = (\texttt{"abbab"}, \texttt{"ab"}, \texttt{"acaab"})$; </li><li> $(x, y, z) = (\texttt{"abb"}, \texttt{"abab"}, \texttt{"acaab"})$; </li><li> $(x, y, z) = (\texttt{"abbaba"}, \texttt{"ba"}, \texttt{"caab"})$; </li><li> $(x, y, z) = (\texttt{"abba"}, \texttt{"baba"}, \texttt{"caab"})$. </li></ul>
