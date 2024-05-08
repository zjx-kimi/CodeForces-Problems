## Description

<div><p>For an array $b$ of $m$ non-negative integers, define $f(b)$ as the <span class="tex-font-style-bf">maximum</span> value of $\max\limits_{i = 1}^{m} (b_i | x) - \min\limits_{i = 1}^{m} (b_i | x)$ over all possible non-negative integers $x$, where $|$ is <a href="https://en.wikipedia.org/wiki/Bitwise_operation#OR">bitwise OR operation</a>.</p><p>You are given integers $n$ and $q$. You start with an empty array $a$. Process the following $q$ queries:</p><ul> <li> $v$: append $v$ to the back of $a$ and then output $f(a)$. It is guaranteed that $0 \leq v &lt; n$. </li></ul><p><span class="tex-font-style-bf">The queries are given in a modified way.</span></p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 2 \cdot 10^5$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $q$ ($1 \leq n \leq 2^{22}$, $1 \leq q \leq 10^6$)&nbsp;— the number of queries.</p><p>The second line of each test case contains $q$ space-separated integers $e_1,e_2,\ldots,e_q$ ($0 \leq e_i &lt; n$)&nbsp;— the encrypted values of $v$.</p><p>Let $\mathrm{last}_i$ equal the output of the $(i-1)$-th query for $i\geq 2$ and $\mathrm{last}_i=0$ for $i=1$. Then the value of $v$ for the $i$-th query is ($e_i + \mathrm{last}_i$) modulo $n$. </p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2^{22}$ and the sum of $q$ over all test cases does not exceed $10^6$.</p></div><div class="output-specification"><p>For each test case, print $q$ integers. The $i$-th integer is the output of the $i$-th query.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 2 \cdot 10^5$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $q$ ($1 \leq n \leq 2^{22}$, $1 \leq q \leq 10^6$)&nbsp;— the number of queries.</p><p>The second line of each test case contains $q$ space-separated integers $e_1,e_2,\ldots,e_q$ ($0 \leq e_i &lt; n$)&nbsp;— the encrypted values of $v$.</p><p>Let $\mathrm{last}_i$ equal the output of the $(i-1)$-th query for $i\geq 2$ and $\mathrm{last}_i=0$ for $i=1$. Then the value of $v$ for the $i$-th query is ($e_i + \mathrm{last}_i$) modulo $n$. </p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2^{22}$ and the sum of $q$ over all test cases does not exceed $10^6$.</p>

## Output

<p>For each test case, print $q$ integers. The $i$-th integer is the output of the $i$-th query.</p>





```input1|2,3
2
5 2
1 2
7 4
3 1 5 2
```




```output1
0 2
0 2 3 5
```



## Note

<p>In the first test case, the final $a=[1,2]$. For $i=1$, the answer is always $0$, irrespective of $x$. For $i=2$, we can select $x=5$.</p><p>In the second test case, the final $a=[3,1,0,5]$.</p>
