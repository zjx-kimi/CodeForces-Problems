## Description

<div><p>You are given an integer array $a_1, a_2, \dots, a_n$ ($1 \le a_i \le n$).</p><p>Find the number of subarrays of $a$ whose $\operatorname{XOR}$ has an even number of divisors. In other words, find all pairs of indices $(i, j)$ ($i \le j$) such that $a_i \oplus a_{i + 1} \oplus \dots \oplus a_j$ has an even number of divisors.</p><p>For example, numbers $2$, $3$, $5$ or $6$ have an even number of divisors, while $1$ and $4$&nbsp;— odd. Consider that $0$ has an odd number of divisors in this task.</p><p>Here $\operatorname{XOR}$ (or $\oplus$) denotes the <a href="https://en.wikipedia.org/wiki/Bitwise_operation#XOR">bitwise XOR operation</a>.</p><p><span class="tex-font-style-striked">Print the number of subarrays but multiplied by 2022...</span> Okay, let's stop. Just print the actual answer.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \leq t \leq 10^4$). Description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2 \leq n \leq 2 \cdot 10^5$)&nbsp;— the length of the array $a$.</p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \leq a_i \leq n$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$. </p></div><div class="output-specification"><p>For each test case, print the number of subarrays, whose $\operatorname{XOR}$ has an even number of divisors.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \leq t \leq 10^4$). Description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2 \leq n \leq 2 \cdot 10^5$)&nbsp;— the length of the array $a$.</p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \leq a_i \leq n$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$. </p>

## Output

<p>For each test case, print the number of subarrays, whose $\operatorname{XOR}$ has an even number of divisors.</p>





```input1|2,3,6,7
4
3
3 1 2
5
4 2 1 5 3
4
4 4 4 4
7
5 7 3 7 1 7 3
```




```output1
4
11
0
20
```



## Note

<p>In the first test case, there are $4$ subarrays whose $\operatorname{XOR}$ has an even number of divisors: $[3]$, $[3,1]$, $[1,2]$, $[2]$.</p><p>In the second test case, there are $11$ subarrays whose $\operatorname{XOR}$ has an even number of divisors: $[4,2]$, $[4,2,1]$, $[4,2,1,5]$, $[2]$, $[2,1]$, $[2,1,5]$, $[2,1,5,3]$, $[1,5,3]$, $[5]$, $[5,3]$, $[3]$.</p><p>In the third test case, there is no subarray whose $\operatorname{XOR}$ has an even number of divisors since $\operatorname{XOR}$ of any subarray is either $4$ or $0$.</p>
