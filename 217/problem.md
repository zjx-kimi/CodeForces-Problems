## Description

<div><p>A ticket is a non-empty string of digits from $1$ to $9$.</p><p>A <span class="tex-font-style-it">lucky</span> ticket is such a ticket that: </p><ul> <li> it has an even length; </li><li> the sum of digits in the first half is equal to the sum of digits in the second half. </li></ul><p>You are given $n$ ticket pieces $s_1, s_2, \dots, s_n$. How many pairs $(i, j)$ (for $1 \le i, j \le n$) are there such that $s_i + s_j$ is a <span class="tex-font-style-it">lucky</span> ticket? Note that it's possible that $i=j$.</p><p>Here, the <span class="tex-font-style-tt">+</span> operator denotes the concatenation of the two strings. For example, if $s_i$ is <span class="tex-font-style-tt">13</span>, and $s_j$ is <span class="tex-font-style-tt">37</span>, then $s_i + s_j$ is <span class="tex-font-style-tt">1337</span>.</p></div><div class="input-specification"><p>The first line contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$)&nbsp;— the number of ticket pieces.</p><p>The second line contains $n$ non-empty strings $s_1, s_2, \dots, s_n$, each of length at most $5$ and consisting only of digits from $1$ to $9$.</p></div><div class="output-specification"><p>Print a single integer&nbsp;— the number of pairs $(i, j)$ (for $1 \le i, j \le n$) such that $s_i + s_j$ is a <span class="tex-font-style-it">lucky</span> ticket.</p></div>

## Input

<p>The first line contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$)&nbsp;— the number of ticket pieces.</p><p>The second line contains $n$ non-empty strings $s_1, s_2, \dots, s_n$, each of length at most $5$ and consisting only of digits from $1$ to $9$.</p>

## Output

<p>Print a single integer&nbsp;— the number of pairs $(i, j)$ (for $1 \le i, j \le n$) such that $s_i + s_j$ is a <span class="tex-font-style-it">lucky</span> ticket.</p>





```input1|
10
5 93746 59 3746 593 746 5937 46 59374 6
```




```input2|
5
2 22 222 2222 22222
```




```input3|
3
1 1 1
```




```output1
20
```




```output2
13
```




```output3
9
```


