## Description

<div><p>Jellyfish is given the non-negative integers $a$, $b$, $c$, $d$ and $m$. Initially $(x,y)=(a,b)$. Jellyfish wants to do several operations so that $(x,y)=(c,d)$.</p><p>For each operation, she can do one of the following:</p><ul> <li> $x := x\,\&amp;\,y$, </li><li> $x := x\,|\,y$, </li><li> $y := x \oplus y$, </li><li> $y := y \oplus m$. </li></ul><p>Here $\&amp;$ denotes the <a href="https://en.wikipedia.org/wiki/Bitwise_operation#AND">bitwise AND operation</a>, $|$ denotes the <a href="https://en.wikipedia.org/wiki/Bitwise_operation#OR">bitwise OR operation</a> and $\oplus$ denotes the <a href="https://en.wikipedia.org/wiki/Bitwise_operation#XOR">bitwise XOR operation</a>.</p><p>Now Jellyfish asks you for the minimum number of operations such that $(x,y)=(c,d)$.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \leq t \leq 10^5$). The description of the test cases follows.</p><p>The only line of each test case contains five integers, $a$, $b$, $c$, $d$ and $m$ ($0 \leq a, b, c, d, m &lt; 2^{30}$).</p></div><div class="output-specification"><p>For each test case, output a single integer&nbsp;— the minimum number of operations. If this cannot be achieved, output $-1$ instead.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \leq t \leq 10^5$). The description of the test cases follows.</p><p>The only line of each test case contains five integers, $a$, $b$, $c$, $d$ and $m$ ($0 \leq a, b, c, d, m &lt; 2^{30}$).</p>

## Output

<p>For each test case, output a single integer&nbsp;— the minimum number of operations. If this cannot be achieved, output $-1$ instead.</p>





```input1|2,4,6,8,10
10
1 0 1 1 1
3 3 1 2 1
1 6 0 7 1
2 4 4 9 8
21 4 0 17 28
50 50 0 0 39
95 33 1 33 110
138 202 174 64 108
78 340 68 340 461
457 291 491 566 766
```




```output1
1
-1
2
-1
-1
2
1
4
1
3
```



## Note

<p>In the first test case, we can do the operation $y = x \oplus y$.</p><p>In the second test case, it is not possible to change $(x,y)=(1,2)$ using any sequence of operations.</p><p>In the third test case, we can do the operation $x = x\,\&amp;\,y$ followed by the operation $y = y \oplus m$.</p>
