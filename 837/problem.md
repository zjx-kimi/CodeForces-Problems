## Description

<div><p>Serval has two $n$-bit binary integer numbers $a$ and $b$. He wants to share those numbers with Toxel.</p><p>Since Toxel likes the number $b$ more, Serval decides to change $a$ into $b$ by some (possibly zero) operations. In an operation, Serval can choose any <span class="tex-font-style-bf">positive</span> integer $k$ between $1$ and $n$, and change $a$ into one of the following number:</p><ul> <li> $a\oplus(a\ll k)$ </li><li> $a\oplus(a\gg k)$ </li></ul><p>In other words, the operation moves every bit of $a$ left or right by $k$ positions, where the overflowed bits are removed, and the missing bits are padded with $0$. The bitwise XOR of the shift result and the original $a$ is assigned back to $a$.</p><p>Serval does not have much time. He wants to perform <span class="tex-font-style-bf">no more than</span> $n$ operations to change $a$ into $b$. Please help him to find out an operation sequence, or determine that it is impossible to change $a$ into $b$ in at most $n$ operations. You do <span class="tex-font-style-bf">not need</span> to minimize the number of operations. </p><p>In this problem, $x\oplus y$ denotes the <a href="https://en.wikipedia.org/wiki/Bitwise_operation#XOR">bitwise XOR operation</a> of $x$ and $y$. $a\ll k$ and $a\gg k$ denote the <a href="https://en.wikipedia.org/wiki/Logical_shift">logical left shift</a> and <a href="https://en.wikipedia.org/wiki/Logical_shift">logical right shift</a>.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1\le t\le2\cdot10^{3}$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1\le n\le2\cdot10^{3}$) — the number of bits in numbers $a$ and $b$.</p><p>The second and the third line of each test case contain a binary string of length $n$, representing $a$ and $b$, respectively. The strings contain only characters <span class="tex-font-style-tt">0</span> and <span class="tex-font-style-tt">1</span>.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2\cdot10^{3}$.</p></div><div class="output-specification"><p>For each test case, if it is impossible to change $a$ into $b$ in at most $n$ operations, print a single integer $-1$.</p><p>Otherwise, in the first line, print the number of operations $m$ ($0\le m\le n$).</p><p>If $m&gt;0$, in the second line, print $m$ integers $k_{1},k_{2},\dots,k_{m}$ representing the operations. If $1\le k_{i}\le n$, it means logical left shift $a$ by $k_{i}$ positions. If $-n\le k_{i}\le-1$, it means logical right shift $a$ by $-k_{i}$ positions.</p><p>If there are multiple solutions, print any of them.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1\le t\le2\cdot10^{3}$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1\le n\le2\cdot10^{3}$) — the number of bits in numbers $a$ and $b$.</p><p>The second and the third line of each test case contain a binary string of length $n$, representing $a$ and $b$, respectively. The strings contain only characters <span class="tex-font-style-tt">0</span> and <span class="tex-font-style-tt">1</span>.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2\cdot10^{3}$.</p>

## Output

<p>For each test case, if it is impossible to change $a$ into $b$ in at most $n$ operations, print a single integer $-1$.</p><p>Otherwise, in the first line, print the number of operations $m$ ($0\le m\le n$).</p><p>If $m&gt;0$, in the second line, print $m$ integers $k_{1},k_{2},\dots,k_{m}$ representing the operations. If $1\le k_{i}\le n$, it means logical left shift $a$ by $k_{i}$ positions. If $-n\le k_{i}\le-1$, it means logical right shift $a$ by $-k_{i}$ positions.</p><p>If there are multiple solutions, print any of them.</p>





```input1|2,3,4,8,9,10
3
5
00111
11000
1
1
1
3
001
000
```




```output1
2
3 -2
0
-1
```



## Note

<p>In the first test case:</p><p>The first operation changes $a$ into $\require{cancel}00111\oplus\cancel{001}11\underline{000}=11111$.</p><p>The second operation changes $a$ into $\require{cancel}11111\oplus\underline{00}111\cancel{11}=11000$.</p><p>The bits with strikethroughs are overflowed bits that are removed. The bits with underline are padded bits.</p><p>In the second test case, $a$ is already equal to $b$, so no operations are needed.</p><p>In the third test case, it can be shown that $a$ cannot be changed into $b$.</p>
