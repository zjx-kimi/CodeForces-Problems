## Description

<div><p>Let $a$, $b$, and $c$ be integers. We define function $f(a, b, c)$ as follows:</p><p>Order the numbers $a$, $b$, $c$ in such a way that $a \le b \le c$. Then return $\gcd(a, b)$, where $\gcd(a, b)$ denotes the <a href="https://en.wikipedia.org/wiki/Greatest_common_divisor">greatest common divisor (GCD)</a> of integers $a$ and $b$.</p><p>So basically, we take the $\gcd$ of the $2$ smaller values and ignore the biggest one. </p><p>You are given an array $a$ of $n$ elements. Compute the sum of $f(a_i, a_j, a_k)$ for each $i$, $j$, $k$, such that $1 \le i &lt; j &lt; k \le n$. </p><p>More formally, compute $$\sum_{i = 1}^n \sum_{j = i+1}^n \sum_{k =j +1}^n f(a_i, a_j, a_k).$$ </p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($3 \le n \le 8 \cdot 10^4$)&nbsp;— length of the array $a$.</p><p>The second line of each test case contains $n$ integers, $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le 10^5$)&nbsp;— elements of the array $a$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $8 \cdot 10^4$.</p></div><div class="output-specification"><p>For each test case, output a single number&nbsp;— the sum from the problem statement.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($3 \le n \le 8 \cdot 10^4$)&nbsp;— length of the array $a$.</p><p>The second line of each test case contains $n$ integers, $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le 10^5$)&nbsp;— elements of the array $a$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $8 \cdot 10^4$.</p>

## Output

<p>For each test case, output a single number&nbsp;— the sum from the problem statement.</p>





```input1|2,3
2
5
2 3 6 12 17
8
6 12 8 10 15 12 18 16
```




```output1
24
203
```



## Note

<p>In the first test case, the values of $f$ are as follows:</p><ul><li> $i=1$, $j=2$, $k=3$, $f(a_i,a_j,a_k)=f(2,3,6)=\gcd(2,3)=1$; </li><li> $i=1$, $j=2$, $k=4$, $f(a_i,a_j,a_k)=f(2,3,12)=\gcd(2,3)=1$; </li><li> $i=1$, $j=2$, $k=5$, $f(a_i,a_j,a_k)=f(2,3,17)=\gcd(2,3)=1$; </li><li> $i=1$, $j=3$, $k=4$, $f(a_i,a_j,a_k)=f(2,6,12)=\gcd(2,6)=2$; </li><li> $i=1$, $j=3$, $k=5$, $f(a_i,a_j,a_k)=f(2,6,17)=\gcd(2,6)=2$; </li><li> $i=1$, $j=4$, $k=5$, $f(a_i,a_j,a_k)=f(2,12,17)=\gcd(2,12)=2$; </li><li> $i=2$, $j=3$, $k=4$, $f(a_i,a_j,a_k)=f(3,6,12)=\gcd(3,6)=3$; </li><li> $i=2$, $j=3$, $k=5$, $f(a_i,a_j,a_k)=f(3,6,17)=\gcd(3,6)=3$; </li><li> $i=2$, $j=4$, $k=5$, $f(a_i,a_j,a_k)=f(3,12,17)=\gcd(3,12)=3$; </li><li> $i=3$, $j=4$, $k=5$, $f(a_i,a_j,a_k)=f(6,12,17)=\gcd(6,12)=6$.</li></ul> The sum over all triples is $1+1+1+2+2+2+3+3+3+6=24$.<p>In the second test case, there are $56$ ways to choose values of $i$, $j$, $k$. The sum over all $f(a_i,a_j,a_k)$ is $203$.</p>
