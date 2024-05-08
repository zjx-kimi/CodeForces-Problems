## Description

<div><p>In the Master's Assistance Center, Nyam-Nyam was given a homework assignment in informatics.</p><p>There is an array $a$ of length $n$, and you want to divide it into $k &gt; 1$ subsegments$^{\dagger}$ in such a way that the $\operatorname{MEX} ^{\ddagger}$ on each subsegment is equal to the same integer.</p><p>Help Nyam-Nyam find any suitable division, or determine that it does not exist.</p><p>$^{\dagger}$A division of an array into $k$ subsegments is defined as $k$ pairs of integers $(l_1, r_1), (l_2, r_2), \ldots, (l_k, r_k)$ such that $l_i \le r_i$ and for each $1 \le j \le k - 1$, $l_{j + 1} = r_j + 1$, and also $l_1 = 1$ and $r_k = n$. These pairs represent the subsegments themselves.</p><p>$^{\ddagger}\operatorname{MEX}$ of an array is the smallest non-negative integer that does not belong to the array.</p><p>For example: </p><ul> <li> $\operatorname{MEX}$ of the array $[2, 2, 1]$ is $0$, because $0$ does not belong to the array. </li><li> $\operatorname{MEX}$ of the array $[3, 1, 0, 1]$ is $2$, because $0$ and $1$ belong to the array, but $2$ does not. </li><li> $\operatorname{MEX}$ of the array $[0, 3, 1, 2]$ is $4$, because $0$, $1$, $2$, and $3$ belong to the array, but $4$ does not. </li></ul></div><div class="input-specification"><p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 10^4$) — the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2 \le n \le 10^5$) — the length of the array $a$.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($0 \le a_i &lt; n$) — the elements of the array $a$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p></div><div class="output-specification"><p>For each test case, output a single integer $-1$ if a suitable division does not exist.</p><p>Otherwise, on the first line, output an integer $k$ ($2 \le k \le n$) — the number of subsegments in the division.</p><p>Then output $k$ lines — the division into subsegments. The $i$-th line should contain two integers $l_i$ and $r_i$ ($1 \le l_i \le r_i \le n$) — the boundaries of the $i$-th subsegment.</p><p>The following conditions must be satisfied:</p><ul><li> For all $1 \le j \le k - 1$, $l_{j + 1} = r_j + 1$;</li><li> $l_1 = 1$, $r_k = n$.</li></ul><p>If there are multiple possible solutions, output any of them.</p></div>

## Input

<p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 10^4$) — the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2 \le n \le 10^5$) — the length of the array $a$.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($0 \le a_i &lt; n$) — the elements of the array $a$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p>

## Output

<p>For each test case, output a single integer $-1$ if a suitable division does not exist.</p><p>Otherwise, on the first line, output an integer $k$ ($2 \le k \le n$) — the number of subsegments in the division.</p><p>Then output $k$ lines — the division into subsegments. The $i$-th line should contain two integers $l_i$ and $r_i$ ($1 \le l_i \le r_i \le n$) — the boundaries of the $i$-th subsegment.</p><p>The following conditions must be satisfied:</p><ul><li> For all $1 \le j \le k - 1$, $l_{j + 1} = r_j + 1$;</li><li> $l_1 = 1$, $r_k = n$.</li></ul><p>If there are multiple possible solutions, output any of them.</p>





```input1|2,3,6,7,10,11
5
2
0 0
5
0 1 2 3 4
8
0 1 7 1 0 1 0 3
3
2 2 2
4
0 1 2 0
```




```output1
2
1 1
2 2
-1
3
1 3
4 5
6 8
3
1 1
2 2
3 3
-1
```



## Note

<p>In the first test case, the array $a$ can be divided into $2$ subsegments with boundaries $[1, 1]$ and $[2, 2]$: </p><ul> <li> $\operatorname{MEX}$ of the first subsegment $[0]$ is $1$, as $0$ belongs to the subsegment, but $1$ does not. </li><li> $\operatorname{MEX}$ of the second subsegment $[0]$ is $1$, as $0$ belongs to the subsegment, but $1$ does not. </li></ul><p>In the second test case, it can be proven that the required division does not exist.</p><p>In the third test case, the array $a$ can be divided into $3$ subsegments with boundaries $[1, 3]$, $[4, 5]$, $[6, 8]$: </p><ul> <li> $\operatorname{MEX}$ of the first subsegment $[0, 1, 7]$ is $2$, as $0$ and $1$ belong to the subsegment, but $2$ does not. </li><li> $\operatorname{MEX}$ of the second subsegment $[1, 0]$ is $2$, as $0$ and $1$ belong to the subsegment, but $2$ does not. </li><li> $\operatorname{MEX}$ of the third subsegment $[1, 0, 3]$ is $2$, as $0$ and $1$ belong to the subsegment, but $2$ does not. </li></ul>
