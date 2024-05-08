## Description

<div><p>You are given $n$ strings $s_1, s_2, \dots, s_n$, consisting of lowercase Latin letters. Let $|x|$ be the length of string $x$.</p><p>Let a <span class="tex-font-style-it">collapse</span> $C(a, b)$ of two strings $a$ and $b$ be the following operation: </p><ul> <li> if $a$ is empty, $C(a, b) = b$; </li><li> if $b$ is empty, $C(a, b) = a$; </li><li> if the last letter of $a$ is equal to the first letter of $b$, then $C(a, b) = C(a_{1,|a|-1}, b_{2,|b|})$, where $s_{l,r}$ is the substring of $s$ from the $l$-th letter to the $r$-th one; </li><li> otherwise, $C(a, b) = a + b$, i. e. the concatenation of two strings. </li></ul><p>Calculate $\sum\limits_{i=1}^n \sum\limits_{j=1}^n |C(s_i, s_j)|$.</p></div><div class="input-specification"><p>The first line contains a single integer $n$ ($1 \le n \le 10^6$).</p><p>Each of the next $n$ lines contains a string $s_i$ ($1 \le |s_i| \le 10^6$), consisting of lowercase Latin letters.</p><p>The total length of the strings doesn't exceed $10^6$.</p></div><div class="output-specification"><p>Print a single integer&nbsp;— $\sum\limits_{i=1}^n \sum\limits_{j=1}^n |C(s_i, s_j)|$.</p></div>

## Input

<p>The first line contains a single integer $n$ ($1 \le n \le 10^6$).</p><p>Each of the next $n$ lines contains a string $s_i$ ($1 \le |s_i| \le 10^6$), consisting of lowercase Latin letters.</p><p>The total length of the strings doesn't exceed $10^6$.</p>

## Output

<p>Print a single integer&nbsp;— $\sum\limits_{i=1}^n \sum\limits_{j=1}^n |C(s_i, s_j)|$.</p>





```input1|
3
aba
ab
ba
```




```input2|
5
abab
babx
xab
xba
bab
```




```output1
20
```




```output2
126
```


