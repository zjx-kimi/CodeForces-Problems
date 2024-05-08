## Description

<div><p><span class="tex-font-style-bf">This is the easy version of the problem. The only difference between the two versions is the constraint on $k$. You can make hacks only if all versions of the problem are solved.</span></p><p>In this statement, all strings are $0$-indexed.</p><p>For two strings $a$, $b$ of the same length $p$, we define the following definitions:</p><ul> <li> The hamming distance between $a$ and $b$, denoted as $h(a, b)$, is defined as the number of positions $i$ such that $0 \le i &lt; p$ and $a_i \ne b_i$. </li><li> $b$ is a cyclic shift of $a$ if there exists some $0 \leq k &lt; p$ such that $b_{(i+k) \bmod p} = a_i$ for all $0 \le i &lt; p$. Here $x \bmod y$ denotes the remainder from dividing $x$ by $y$. </li></ul><p>You are given two binary strings $s$ and $t$ of length $2^{k+1}$ each. Both strings may contain missing characters (denoted by the character '<span class="tex-font-style-tt">?</span>'). Your task is to count the number of ways to replace the missing characters in both strings with the characters '<span class="tex-font-style-tt">0</span>' or '<span class="tex-font-style-tt">1</span>' such that: </p><ul> <li> Each string $s$ and $t$ contains exactly $2^k$ occurrences of each character '<span class="tex-font-style-tt">0</span>' and '<span class="tex-font-style-tt">1</span>' </li><li> $h(s, c) \ge 2^k$ for all strings $c$ that is a cyclic shift of $t$. </li></ul><p>As the result can be very large, you should print the value modulo $998\,244\,353$.</p></div><div class="input-specification"><p>The first line of the input contains a single integer $k$ ($1 \le k \le 7$).</p><p>The second line of the input contains string $s$ of size $2^{k+1}$, consisting of the characters '<span class="tex-font-style-tt">0</span>', '<span class="tex-font-style-tt">1</span>' and '<span class="tex-font-style-tt">?</span>'.</p><p>The third line of the input contains string $t$ of size $2^{k+1}$, consisting of the characters '<span class="tex-font-style-tt">0</span>', '<span class="tex-font-style-tt">1</span>' and '<span class="tex-font-style-tt">?</span>'.</p><p>It is guaranteed that both strings $s$ and $t$ contains no more than $2^k$ character '<span class="tex-font-style-tt">0</span>' or '<span class="tex-font-style-tt">1</span>'.</p></div><div class="output-specification"><p>Print a single integer&nbsp;— the answer to the problem modulo $998\,244\,353$.</p></div>

## Input

<p>The first line of the input contains a single integer $k$ ($1 \le k \le 7$).</p><p>The second line of the input contains string $s$ of size $2^{k+1}$, consisting of the characters '<span class="tex-font-style-tt">0</span>', '<span class="tex-font-style-tt">1</span>' and '<span class="tex-font-style-tt">?</span>'.</p><p>The third line of the input contains string $t$ of size $2^{k+1}$, consisting of the characters '<span class="tex-font-style-tt">0</span>', '<span class="tex-font-style-tt">1</span>' and '<span class="tex-font-style-tt">?</span>'.</p><p>It is guaranteed that both strings $s$ and $t$ contains no more than $2^k$ character '<span class="tex-font-style-tt">0</span>' or '<span class="tex-font-style-tt">1</span>'.</p>

## Output

<p>Print a single integer&nbsp;— the answer to the problem modulo $998\,244\,353$.</p>





```input1
1
0011
0101
```




```input2
1
0011
0110
```




```input3
1
0??1
01??
```




```input4
2
000?????
01010101
```




```input5
2
0???????
1???????
```




```input6
5
0101010101010101010101010101010101010101010101010101010101010101
????????????????????????????????????????????????????????????????
```




```output1
1
```




```output2
0
```




```output3
2
```




```output4
3
```




```output5
68
```




```output6
935297567
```



## Note

<p>In the first example, we can check that the condition $h(s, c) \ge 2^k$ for all cyclic shift $c$ of $t$ is satisfied. In particular: </p><ul> <li> for $c = \mathtt{0101}$, $h(s, c) = h(\mathtt{0110}, \mathtt{0101}) = 2 \ge 2^1$; </li><li> for $c = \mathtt{1010}$, $h(s, c) = h(\mathtt{0110}, \mathtt{1010}) = 2 \ge 2^1$. </li></ul><p>In the second example, there exists a cycle shift $c$ of $t$ such that $h(s, c) &lt; 2^k$ (in particular, $c = \mathtt{0011}$, and $h(s, c) = h(\mathtt{0011}, \mathtt{0011}) = 0$).</p><p>In the third example, there are $2$ possible ways to recover the missing characters: </p><ul> <li> $s = \mathtt{0101}$, $t = \mathtt{0110}$; </li><li> $s = \mathtt{0011}$, $t = \mathtt{0101}$. </li></ul><p>In the fourth example, there are $3$ possible ways to recover the missing characters: </p><ul> <li> $s = \mathtt{00011110}$, $t = \mathtt{01010101}$; </li><li> $s = \mathtt{00011011}$, $t = \mathtt{01010101}$; </li><li> $s = \mathtt{00001111}$, $t = \mathtt{01010101}$. </li></ul>
