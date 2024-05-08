## Description

<div><p>You are given an array $a$ of length $n$, consisting of positive integers, and an array $x$ of length $q$, also consisting of positive integers.</p><p>There are $q$ modification. On the $i$-th modification ($1 \leq i \leq q$), for each $j$ ($1 \leq j \leq n$), such that $a_j$ is divisible by $2^{x_i}$, you add $2^{x_i-1}$ to $a_j$. <span class="tex-font-style-bf">Note that</span> $x_i$ ($1 \leq x_i \leq 30$) is <span class="tex-font-style-bf">a positive integer not exceeding 30</span>.</p><p>After <span class="tex-font-style-bf">all</span> modification queries, you need to output the final array.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \leq t \leq 10^4$) — the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $q$ ($1 \leq n, q \leq 10^5$) —the length of the array $a$ and the number of queries respectively.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, a_3, \ldots, a_n$ — the elements of the array $a$ ($1 \leq a_i \leq 10^9$).</p><p>The third line of each test case contains $q$ integers $x_1, x_2, x_3, \ldots, x_q$ — the elements of the array $x$ ($1 \leq x_i \leq 30$), which are the modification queries.</p><p>It is guaranteed that the sum of $n$ and the sum of $q$ across all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output the array after all of the modification queries.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \leq t \leq 10^4$) — the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $q$ ($1 \leq n, q \leq 10^5$) —the length of the array $a$ and the number of queries respectively.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, a_3, \ldots, a_n$ — the elements of the array $a$ ($1 \leq a_i \leq 10^9$).</p><p>The third line of each test case contains $q$ integers $x_1, x_2, x_3, \ldots, x_q$ — the elements of the array $x$ ($1 \leq x_i \leq 30$), which are the modification queries.</p><p>It is guaranteed that the sum of $n$ and the sum of $q$ across all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output the array after all of the modification queries.</p>





```input1|2,3,4,8,9,10
4
5 3
1 2 3 4 4
2 3 4
7 3
7 8 12 36 48 6 3
10 4 2
5 4
2 2 2 2 2
1 1 1 1
5 5
1 2 4 8 16
5 2 3 4 1
```




```output1
1 2 3 6 6 
7 10 14 38 58 6 3 
3 3 3 3 3 
1 3 7 11 19
```



## Note

<p>In the first test case, the first query will add $2$ to the integers in positions $4$ and $5$. After this addition, the array would be $[1, 2, 3, 6, 6]$. Other operations will not modify the array.</p><p>In the second test case, the first modification query does not change the array. The second modification query will add $8$ to the integer in position $5$, so that the array would look like this: $[7, 8, 12, 36, 56, 6, 3]$. The third modification query will add $2$ to the integers in positions $2, 3$, $4$ and $5$. The array would then look like this: $[7, 10, 14, 38, 58, 6, 3]$.</p>
