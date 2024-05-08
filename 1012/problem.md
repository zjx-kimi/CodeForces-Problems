## Description

<div><p>An array $b$ of $m$ positive integers is <span class="tex-font-style-it">good</span> if for all pairs $i$ and $j$ ($1 \leq i,j \leq m$), $\max(b_i,b_j)$ is divisible by $\min(b_i,b_j)$.</p><p>You are given an array $a$ of $n$ positive integers. You can perform the following operation:</p><ul> <li> Select an index $i$ ($1 \leq i \leq n$) and an integer $x$ ($0 \leq x \leq a_i$) and add $x$ to $a_i$, in other words, $a_i := a_i+x$. </li><li> After this operation, $a_i \leq 10^{18}$ should be satisfied. </li></ul><p>You have to construct a sequence of <span class="tex-font-style-bf">at most</span> $n$ operations that will make $a$ good. It can be proven that under the constraints of the problem, such a sequence of operations <span class="tex-font-style-bf">always</span> exists.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 10^4$) — the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \leq n \leq 10^5$) — the length of the array $a$.</p><p>The second line of each test case contains $n$ space-separated integers $a_1,a_2,\ldots,a_n$ ($1 \leq a_i \leq 10^9$) — representing the array $a$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p></div><div class="output-specification"><p>For each test, output a single integer $p$ ($0 \leq p \leq n$) — denoting the number of operations in your solution. </p><p>In each of the following $p$ lines, output two space-separated integers — $i$ and $x$.</p><p>You do not need to minimize the number of operations. It can be proven that a solution always exists.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 10^4$) — the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \leq n \leq 10^5$) — the length of the array $a$.</p><p>The second line of each test case contains $n$ space-separated integers $a_1,a_2,\ldots,a_n$ ($1 \leq a_i \leq 10^9$) — representing the array $a$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p>

## Output

<p>For each test, output a single integer $p$ ($0 \leq p \leq n$) — denoting the number of operations in your solution. </p><p>In each of the following $p$ lines, output two space-separated integers — $i$ and $x$.</p><p>You do not need to minimize the number of operations. It can be proven that a solution always exists.</p>





```input1|2,3,6,7
4
4
2 3 5 5
2
4 8
5
3 4 343 5 6
3
31 5 17
```




```output1
4
1 2
1 1
2 2
3 0
0
5
1 3
1 4
2 1
5 4
3 7
3
1 29
2 5
3 3
```



## Note

<p>In the first test case, array $a$ becomes $[5,5,5,5]$ after the operations. It is easy to see that $[5,5,5,5]$ is <span class="tex-font-style-it">good</span>.</p><p>In the second test case, array $a$ is already <span class="tex-font-style-it">good</span>.</p><p>In the third test case, after performing the operations, array $a$ becomes $[10,5,350,5,10]$, which is <span class="tex-font-style-it">good</span>.</p><p>In the fourth test case, after performing the operations, array $a$ becomes $[60,10,20]$, which is <span class="tex-font-style-it">good</span>.</p>
