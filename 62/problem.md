## Description

<div><p>You are given integers $a$, $b$, $r$. Find the smallest value of $|({a \oplus x}) - ({b \oplus x})|$ among all $0 \leq x \leq r$.</p><p>$\oplus$ is the operation of <a href="https://en.wikipedia.org/wiki/Bitwise_operation#XOR">bitwise XOR</a>, and $|y|$ is <a href="https://en.wikipedia.org/wiki/Absolute_value">absolute value</a> of $y$.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>Each test case contains integers $a$, $b$, $r$ ($0 \le a, b, r \le 10^{18}$).</p></div><div class="output-specification"><p>For each test case, output a single number&nbsp;— the smallest possible value.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>Each test case contains integers $a$, $b$, $r$ ($0 \le a, b, r \le 10^{18}$).</p>

## Output

<p>For each test case, output a single number&nbsp;— the smallest possible value.</p>





```input1|2,4,6,8,10
10
4 6 0
0 3 2
9 6 10
92 256 23
165 839 201
1 14 5
2 7 2
96549 34359 13851
853686404475946 283666553522252166 127929199446003072
735268590557942972 916721749674600979 895150420120690183
```




```output1
2
1
1
164
542
5
3
37102
27934920819538516
104449824168870225
```



## Note

<p>In the first test, when $r = 0$, then $x$ is definitely equal to $0$, so the answer is $|{4 \oplus 0} - {6 \oplus 0}| = |4 - 6| = 2$.</p><p>In the second test:</p><ul> <li> When $x = 0$, $|{0 \oplus 0} - {3 \oplus 0}| = |0 - 3| = 3$. </li><li> When $x = 1$, $|{0 \oplus 1} - {3 \oplus 1}| = |1 - 2| = 1$. </li><li> When $x = 2$, $|{0 \oplus 2} - {3 \oplus 2}| = |2 - 1| = 1$. </li></ul><p>Therefore, the answer is $1$.</p><p>In the third test, the minimum is achieved when $x = 1$.</p>
