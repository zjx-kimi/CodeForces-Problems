## Description

<div><p><span class="tex-font-style-bf">This is the hard version of the problem. The only difference between the two versions is the constraint on $n$. You can make hacks only if both versions of the problem are solved.</span></p><p>An array $b$ of $m$ non-negative integers is said to be <span class="tex-font-style-it">good</span> if all the elements of $b$ can be made equal to $0$ using the following operation some (possibly, zero) times: </p><ul> <li> Select two <span class="tex-font-style-bf">distinct</span> indices $l$ and $r$ ($1 \leq l \color{red}{&lt;} r \leq m$) and subtract $1$ from all $b_i$ such that $l \leq i \leq r$. </li></ul><p>You are given two positive integers $n$, $k$ and a prime number $p$.</p><p>Over all $(k+1)^n$ arrays of length $n$ such that $0 \leq a_i \leq k$ for all $1 \leq i \leq n$, count the number of good arrays.</p><p>Since the number might be too large, you are only required to find it modulo $p$.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 10^3$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains three positive integers $n$, $k$ and $p$ ($3 \leq n \leq 3000$, $1 \leq k \leq n$, $10^8 &lt; p &lt; 10^9$)&nbsp;— the length of the array $a$, the upper bound on the elements of $a$ and modulus $p$.</p><p>It is guaranteed that the sum of $n^2$ over all test cases does not exceed $10^7$, and $p$ is prime.</p></div><div class="output-specification"><p>For each test case, on a new line, output the number of good arrays modulo $p$.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 10^3$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains three positive integers $n$, $k$ and $p$ ($3 \leq n \leq 3000$, $1 \leq k \leq n$, $10^8 &lt; p &lt; 10^9$)&nbsp;— the length of the array $a$, the upper bound on the elements of $a$ and modulus $p$.</p><p>It is guaranteed that the sum of $n^2$ over all test cases does not exceed $10^7$, and $p$ is prime.</p>

## Output

<p>For each test case, on a new line, output the number of good arrays modulo $p$.</p>





```input1|2,4
4
3 1 998244853
4 1 998244353
3 2 998244353
343 343 998244353
```




```output1
4
7
10
456615865
```



## Note

<p>In the first test case, the $4$ good arrays $a$ are: </p><ul> <li> $[0,0,0]$; </li><li> $[0,1,1]$; </li><li> $[1,1,0]$; </li><li> $[1,1,1]$. </li></ul>
