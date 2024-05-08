## Description

<div><p>You are given a binary string $s$ of length $n$ (a string consisting of $n$ characters, and each character is either <span class="tex-font-style-tt">0</span> or <span class="tex-font-style-tt">1</span>).</p><p>Let's look at $s$ as at a binary representation of some integer, and name that integer as the <span class="tex-font-style-it">value</span> of string $s$. For example, the value of <span class="tex-font-style-tt">000</span> is $0$, the value of <span class="tex-font-style-tt">01101</span> is $13$, "<span class="tex-font-style-tt">100000</span>" is $32$ and so on.</p><p>You can perform at most $k$ operations on $s$. Each operation should have one of the two following types: </p><ul> <li> <span class="tex-font-style-tt">SWAP</span>: choose two indices $i &lt; j$ in $s$ and swap $s_i$ with $s_j$; </li><li> <span class="tex-font-style-tt">SHRINK-REVERSE</span>: delete all leading zeroes from $s$ and reverse $s$. </li></ul> For example, after you perform <span class="tex-font-style-tt">SHRINK-REVERSE</span> on <span class="tex-font-style-tt">000101100</span>, you'll get <span class="tex-font-style-tt">001101</span>.<p>What is the minimum value of $s$ you can achieve by performing at most $k$ operations on $s$?</p></div><div class="input-specification"><p>The first line contains two integers $n$ and $k$ ($2 \le n \le 5 \cdot 10^5$; $1 \le k \le n$)&nbsp;— the length of the string $s$ and the maximum number of operations.</p><p>The second line contains the string $s$ of length $n$ consisting of characters <span class="tex-font-style-tt">0</span> and/or <span class="tex-font-style-tt">1</span>. </p><p>Additional constraint on the input: $s$ contains <span class="tex-font-style-bf">at least one</span> <span class="tex-font-style-tt">1</span>.</p></div><div class="output-specification"><p>Print a single integer&nbsp;— the minimum value of $s$ you can achieve using no more than $k$ operations. Since the answer may be too large, print it modulo $10^{9} + 7$.</p><p>Note that you need to minimize the original value, not the remainder.</p></div>

## Input

<p>The first line contains two integers $n$ and $k$ ($2 \le n \le 5 \cdot 10^5$; $1 \le k \le n$)&nbsp;— the length of the string $s$ and the maximum number of operations.</p><p>The second line contains the string $s$ of length $n$ consisting of characters <span class="tex-font-style-tt">0</span> and/or <span class="tex-font-style-tt">1</span>. </p><p>Additional constraint on the input: $s$ contains <span class="tex-font-style-bf">at least one</span> <span class="tex-font-style-tt">1</span>.</p>

## Output

<p>Print a single integer&nbsp;— the minimum value of $s$ you can achieve using no more than $k$ operations. Since the answer may be too large, print it modulo $10^{9} + 7$.</p><p>Note that you need to minimize the original value, not the remainder.</p>





```input1|
8 2
10010010
```




```input2|
8 2
01101000
```




```input3|
30 30
111111111111111111111111111111
```




```input4|
14 1
10110001111100
```




```output1
7
```




```output2
7
```




```output3
73741816
```




```output4
3197
```



## Note

<p>In the first example, one of the optimal strategies is the following: </p><ol> <li> <span class="tex-font-style-tt"><span class="tex-font-style-underline">1</span>0010<span class="tex-font-style-underline">0</span>10</span> $\xrightarrow{\texttt{SWAP}}$ <span class="tex-font-style-tt">00010110</span>; </li><li> <span class="tex-font-style-tt">000<span class="tex-font-style-underline">1</span>011<span class="tex-font-style-underline">0</span></span> $\xrightarrow{\texttt{SWAP}}$ <span class="tex-font-style-tt">00000111</span>. </li></ol> The value of <span class="tex-font-style-tt">00000111</span> is $7$.<p>In the second example, one of the optimal strategies is the following: </p><ol> <li> <span class="tex-font-style-tt">01101000</span> $\xrightarrow{\texttt{SHRINK}}$ <span class="tex-font-style-tt">1101000</span> $\xrightarrow{\texttt{REVERSE}}$ <span class="tex-font-style-tt">0001011</span>; </li><li> <span class="tex-font-style-tt">000<span class="tex-font-style-underline">10</span>11</span> $\xrightarrow{\texttt{SWAP}}$ <span class="tex-font-style-tt">0000111</span>. </li></ol> The value of <span class="tex-font-style-tt">0000111</span> is $7$.
