## Description

<div><p>You are given two arrays of integers — $a_1, \ldots, a_n$ of length $n$, and $b_1, \ldots, b_m$ of length $m$. You can choose any element $b_j$ from array $b$ ($1 \leq j \leq m$), and for <span class="tex-font-style-bf">all</span> $1 \leq i \leq n$ perform $a_i = a_i | b_j$. You can perform any number of such operations.</p><p>After all the operations, the value of $x = a_1 \oplus a_2 \oplus \ldots \oplus a_n$ will be calculated. Find the minimum and maximum values of $x$ that could be obtained after performing any set of operations.</p><p>Above, $|$ is the <a href="https://en.wikipedia.org/wiki/Bitwise_operation#OR">bitwise OR operation</a>, and $\oplus$ is the <a href="https://en.wikipedia.org/wiki/Bitwise_operation#XOR">bitwise XOR operation</a>.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \leq t \leq 10^4$) — the number of test cases. This is followed by the description of the test cases.</p><p>The first line of each test case contains two integers $n$ and $m$ ($1 \leq n, m \leq 2 \cdot 10^5$) — the sizes of arrays $a$ and $b$.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($0 \leq a_i \leq 10^9$) — the array $a$.</p><p>The third line of each test case contains $m$ integers $b_1, b_2, \ldots, b_m$ ($0 \leq b_i \leq 10^9$) — the array $b$.</p><p>It is guaranteed that the sum of values of $n$ and $m$ across all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output $2$ numbers: the minimum and maximum possible values of $x$ after performing any set of operations.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \leq t \leq 10^4$) — the number of test cases. This is followed by the description of the test cases.</p><p>The first line of each test case contains two integers $n$ and $m$ ($1 \leq n, m \leq 2 \cdot 10^5$) — the sizes of arrays $a$ and $b$.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($0 \leq a_i \leq 10^9$) — the array $a$.</p><p>The third line of each test case contains $m$ integers $b_1, b_2, \ldots, b_m$ ($0 \leq b_i \leq 10^9$) — the array $b$.</p><p>It is guaranteed that the sum of values of $n$ and $m$ across all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output $2$ numbers: the minimum and maximum possible values of $x$ after performing any set of operations.</p>





```input1|2,3,4
2
2 3
0 1
1 2 3
3 1
1 1 2
1
```




```output1
0 1
2 3
```



## Note

<p>In the first test case, if we apply the operation with element $b_1 = 1$, the array $a$ will become $[1, 1]$, and $x$ will be $0$. If no operations are applied, then $x = 1$.</p><p>In the second test case, if no operations are applied, then $x = 2$. If we apply the operation with $b_1 = 1$, then $a = [1, 1, 3]$, and $x = 3$.</p>
