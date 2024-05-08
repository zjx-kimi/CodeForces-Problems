## Description

<div><p>Josuke is tired of his peaceful life in Morioh. Following in his nephew Jotaro's footsteps, he decides to study hard and become a professor of computer science. While looking up competitive programming problems online, he comes across the following one: </p><p>Let $s$ be a binary string of length $n$. An operation on $s$ is defined as choosing two distinct integers $i$ and $j$ ($1 \leq i &lt; j \leq n$), and swapping the characters $s_i, s_j$.</p><p>Consider the $m$ strings $t_1, t_2, \ldots, t_m$, where $t_i$ is the substring $^\dagger$ of $s$ from $l_i$ to $r_i$. Define $t(s) = t_1+t_2+\ldots+t_m$ as the concatenation of the strings $t_i$ in that order.</p><p>There are $q$ updates to the string. In the $i$-th update $s_{x_i}$ gets flipped. That is if $s_{x_i}=1$, then $s_{x_i}$ becomes $0$ and vice versa. After each update, find the minimum number of <span class="tex-font-style-bf">operations one must perform on $s$</span> to make $t(s)$ lexicographically as large$^\ddagger$ as possible. </p><p>Note that no operation is actually performed. We are only interested in the number of operations.</p><p>Help Josuke in his dream by solving the problem for him.</p><center> —————————————————————— </center><p>$\dagger$ A string $a$ is a substring of a string $b$ if $a$ can be obtained from $b$ by the deletion of several (possibly, zero or all) characters from the beginning and several (possibly, zero or all) characters from the end.</p><p>$\ddagger$ A string $a$ is lexicographically larger than a string $b$ of the same length if and only if the following holds: </p><ul> <li> in the first position where $a$ and $b$ differ, the string $a$ has a $1$, and the string $b$ has a $0$. </li></ul></div><div class="input-specification"><p>The first line contains three integers $n$, $m$, $q$ ($1 \leq n,m,q \leq 2 \cdot 10^5$). </p><p>The next line contains a binary string $s$ of length $n$, consisting only of digits $0$ and $1$.</p><p>The $i$-th line of the next $m$ lines contains two integers $l_i$ and $r_i$ ($1 \leq l_i \leq r_i \leq n$).</p><p>The $i$-th line of the next $q$ lines contains a single integer $x_i$ ($1 \leq x_i \leq n$).</p></div><div class="output-specification"><p>Print $q$ integers. The $i$-th integer is the minimum number of operations that need to be performed on $s$ to get the lexicographically largest possible string $t(s)$ in the $i$-th round.</p></div>

## Input

<p>The first line contains three integers $n$, $m$, $q$ ($1 \leq n,m,q \leq 2 \cdot 10^5$). </p><p>The next line contains a binary string $s$ of length $n$, consisting only of digits $0$ and $1$.</p><p>The $i$-th line of the next $m$ lines contains two integers $l_i$ and $r_i$ ($1 \leq l_i \leq r_i \leq n$).</p><p>The $i$-th line of the next $q$ lines contains a single integer $x_i$ ($1 \leq x_i \leq n$).</p>

## Output

<p>Print $q$ integers. The $i$-th integer is the minimum number of operations that need to be performed on $s$ to get the lexicographically largest possible string $t(s)$ in the $i$-th round.</p>





```input1
2 2 4
01
1 2
1 2
1
1
2
2
```




```input2
8 6 10
10011010
5 6
2 3
6 8
5 7
5 8
6 8
3
5
6
2
5
2
5
8
4
1
```




```output1
0
1
0
1
```




```output2
2
3
2
2
1
2
2
2
2
2
```



## Note

<p>In the first test case,</p><p>Originally, $t(s) = s(1,2) + s(1,2) = 0101$.</p><p>After the $1$-st query, $s$ becomes $11$ and consequently $t$ becomes $1111$. You don't need to perform any operation as $t(s)$ is already the lexicographically largest string possible.</p><p>After the $2$-nd query, $s$ becomes $01$ and consequently $t$ becomes $0101$. You need to perform $1$ operation by swapping $s_1$ and $s_2$. Consequently, $t(s)$ becomes $1010$ which is the lexicographically largest string you can achieve.</p>
