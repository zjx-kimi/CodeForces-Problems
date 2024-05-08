## Description

<div><p>Consider an array of integers $b_0, b_1, \ldots, b_{n-1}$. Your goal is to make all its elements equal. To do so, you can perform the following operation several (possibly, zero) times:</p><ul><li> Pick a pair of indices $0 \le l \le r \le n-1$, then for each $l \le i \le r$ increase $b_i$ by $1$ (i.&nbsp;e. replace $b_i$ with $b_i + 1$).</li><li> After performing this operation you receive $(r - l + 1)^2$ coins. </li></ul><p>The value $f(b)$ is defined as a pair of integers $(cnt, cost)$, where $cnt$ is the <span class="tex-font-style-bf">smallest</span> number of operations required to make all elements of the array equal, and $cost$ is the <span class="tex-font-style-bf">largest</span> total number of coins you can receive among all possible ways to make all elements equal within $cnt$ operations. In other words, first, you need to minimize the number of operations, second, you need to maximize the total number of coins you receive.</p><p>You are given an array of integers $a_0, a_1, \ldots, a_{n-1}$. Please, find the value of $f$ for all cyclic shifts of $a$.</p><p>Formally, for each $0 \le i \le n-1$ you need to do the following:</p><ul><li> Let $c_j = a_{(j + i) \pmod{n}}$ for each $0 \le j \le n-1$.</li><li> Find $f(c)$. Since $cost$ can be very large, output it modulo $(10^9 + 7)$.</li></ul><p>Please note that under a fixed $cnt$ you need to maximize the total number of coins $cost$, not its remainder modulo $(10^9 + 7)$.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 2 \cdot 10^4$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 10^6$).</p><p>The second line of each test case contains $n$ integers $a_0, a_1, \ldots, a_{n-1}$ ($1 \le a_i \le 10^9$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^6$.</p></div><div class="output-specification"><p>For each test case, for each $0 \le i \le n-1$ output the value of $f$ for the $i$-th cyclic shift of array $a$: first, output $cnt$ (the minimum number of operations), then output $cost$ (the maximum number of coins these operations can give) modulo $10^9 + 7$.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 2 \cdot 10^4$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 10^6$).</p><p>The second line of each test case contains $n$ integers $a_0, a_1, \ldots, a_{n-1}$ ($1 \le a_i \le 10^9$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^6$.</p>

## Output

<p>For each test case, for each $0 \le i \le n-1$ output the value of $f$ for the $i$-th cyclic shift of array $a$: first, output $cnt$ (the minimum number of operations), then output $cost$ (the maximum number of coins these operations can give) modulo $10^9 + 7$.</p>





```input1|2,3,6,7,10,11
5
1
1
3
1 3 2
5
3 2 4 5 1
8
6 5 6 4 2 6 2 2
4
10 10 10 10
```




```output1
0 0
3 3
2 5
2 5
7 18
7 16
6 22
5 28
5 28
9 27
9 27
9 27
9 27
11 23
9 27
9 27
13 19
0 0
0 0
0 0
0 0
```



## Note

<p>In the first test case, there is only one cycle shift, which is equal to $[1]$, and all its elements are already equal.</p><p>In the second test case, you need to find the answer for three arrays: </p><ol> <li> $f([1, 3, 2]) = (3, 3)$. </li><li> $f([3, 2, 1]) = (2, 5)$. </li><li> $f([2, 1, 3]) = (2, 5)$. </li></ol><p>Consider the case of $[2, 1, 3]$. To make all elements equal, we can pick $l = 1$ and $r = 1$ on the first operation, which results in $[2, 2, 3]$. On the second operation we can pick $l = 0$ and $r = 1$, which results in $[3, 3, 3]$. We have used $2$ operations, and the total number of coins received is $1^2 + 2^2 = 5$.</p>
