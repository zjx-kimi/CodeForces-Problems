## Description

<div><p>Given two positive integers $n$ and $m$. Find the sum of all possible values of $a_1\bigoplus a_2\bigoplus\ldots\bigoplus a_m$, where $a_1,a_2,\ldots,a_m$ are non-negative integers such that $a_1+a_2+\ldots+a_m=n$.</p><p>Note that all possible values $a_1\bigoplus a_2\bigoplus\ldots\bigoplus a_m$ should be counted in the sum <span class="tex-font-style-bf">exactly once</span>.</p><p>As the answer may be too large, output your answer modulo $998244353$.</p><p>Here, $\bigoplus$ denotes the <a href="https://en.wikipedia.org/wiki/Bitwise_operation#XOR">bitwise XOR operation</a>.</p></div><div class="input-specification"><p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 10^4$) — the number of test cases. The description of test cases follows.</p><p>The first and only line of each test case contains two integers $n$ and $m$ ($0\le n\le 10^{18}, 1\le m\le 10^5$) — the sum and the number of integers in the set, respectively.</p></div><div class="output-specification"><p>For each test case, output the sum of all possible values of $a_1\bigoplus a_2\bigoplus\ldots\bigoplus a_m$ among all non-negative integers $a_1,a_2,\ldots,a_m$ with $a_1+a_2+\ldots+a_m=n$. As the answer may be too large, output your answer modulo $998244353$.</p></div>

## Input

<p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 10^4$) — the number of test cases. The description of test cases follows.</p><p>The first and only line of each test case contains two integers $n$ and $m$ ($0\le n\le 10^{18}, 1\le m\le 10^5$) — the sum and the number of integers in the set, respectively.</p>

## Output

<p>For each test case, output the sum of all possible values of $a_1\bigoplus a_2\bigoplus\ldots\bigoplus a_m$ among all non-negative integers $a_1,a_2,\ldots,a_m$ with $a_1+a_2+\ldots+a_m=n$. As the answer may be too large, output your answer modulo $998244353$.</p>





```input1|2,4,6,8
7
69 1
5 2
0 10
420 69
12 26
73 34
1000000000000000000 10
```




```output1
69
6
0
44310
42
1369
216734648
```



## Note

<p>For the first test case, we must have $a_1=69$, so it's the only possible value of $a_1$, therefore our answer is $69$.</p><p>For the second test case, $(a_1,a_2)$ can be $(0,5), (1,4), (2,3), (3,2), (4,1)$ or $(5,0)$, in which $a_1\bigoplus a_2$ are $5,5,1,1,5,5$ respectively. So $a_1\bigoplus a_2$ can be $1$ or $5$, therefore our answer is $1+5=6$.</p><p>For the third test case, $a_1,a_2,\ldots,a_{10}$ must be all $0$, so $a_1\bigoplus a_2\bigoplus\ldots\bigoplus a_{10}=0$. Therefore our answer is $0$.</p>
