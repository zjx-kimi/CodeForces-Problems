## Description

<div><p>You are given a binary$^\dagger$ pattern $p$ of length $n$.</p><p>A binary string $q$ of the same length $n$ is called <span class="tex-font-style-bf">good</span> if for every $i$ ($1 \leq i \leq n$), there exist indices $l$ and $r$ such that: </p><ul> <li> $1 \leq l \leq i \leq r \leq n$, and </li><li> $p_i$ is a mode$^\ddagger$ of the string $q_lq_{l+1}\ldots q_r$. </li></ul><p>Count the number of good binary strings modulo $998\,244\,353$.</p><p>$^\dagger$ A binary string is a string that only consists of characters $\mathtt{0}$ and $\mathtt{1}$.</p><p>$^\ddagger$ Character $c$ is a mode of string $t$ of length $m$ if the number of occurrences of $c$ in $t$ is at least $\lceil \frac{m}{2} \rceil$. For example, $\mathtt{0}$ is a mode of $\mathtt{010}$, $\mathtt{1}$ is not a mode of $\mathtt{010}$, and both $\mathtt{0}$ and $\mathtt{1}$ are modes of $\mathtt{011010}$.</p></div><div class="input-specification"><p>The first line of input contains a single integer $n$ ($1 \le n \le 10^5$)&nbsp;— the length of the binary string $p$.</p><p>The second line of input contains a binary string $p$ of length $n$ consisting of characters <span class="tex-font-style-tt">0</span> and <span class="tex-font-style-tt">1</span>.</p></div><div class="output-specification"><p>Output the number of good strings modulo $998\,244\,353$.</p></div>

## Input

<p>The first line of input contains a single integer $n$ ($1 \le n \le 10^5$)&nbsp;— the length of the binary string $p$.</p><p>The second line of input contains a binary string $p$ of length $n$ consisting of characters <span class="tex-font-style-tt">0</span> and <span class="tex-font-style-tt">1</span>.</p>

## Output

<p>Output the number of good strings modulo $998\,244\,353$.</p>





```input1|
1
0
```




```input2|
3
111
```




```input3|
4
1011
```




```input4|
6
110001
```




```input5|
12
111010001111
```




```output1
1
```




```output2
5
```




```output3
9
```




```output4
36
```




```output5
2441
```



## Note

<p>In the second example, the good strings are </p><ul> <li> $\mathtt{010}$; </li><li> $\mathtt{011}$; </li><li> $\mathtt{101}$; </li><li> $\mathtt{110}$; </li><li> $\mathtt{111}$. </li></ul>
