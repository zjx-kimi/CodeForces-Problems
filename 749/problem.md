## Description

<div><p>You have an array of positive integers $a_1, a_2, \ldots, a_n$, of length $n$. You are also given a positive integer $b$.</p><p>You are allowed to perform the following operations (possibly several) times in any order: </p><ol> <li> Choose some $1 \le i \le n$, and replace $a_i$ with $\lceil \frac{a_i}{2} \rceil$. Here, $\lceil x \rceil$ denotes the smallest integer not less than $x$. </li><li> Choose some $1 \le i \le n$, and replace $a_i$ with $\max(a_i - b, 0)$. </li></ol><p>However, you must also follow these rules: </p><ul> <li> You can perform at most $k_1$ operations of type 1 in total. </li><li> You can perform at most $k_2$ operations of type 2 in total. </li><li> For all $1 \le i \le n$, you can perform at most $1$ operation of type 1 on element $a_i$. </li><li> For all $1 \le i \le n$, you can perform at most $1$ operation of type 2 on element $a_i$. </li></ul><p>The <span class="tex-font-style-it">cost</span> of an array is the sum of its elements. Find the minimum cost of $a$ you can achieve by performing these operations.</p></div><div class="input-specification"><p>Input consists of multiple test cases. The first line contains a single integer $t$, the number of test cases ($1 \le t \le 5000$).</p><p>The first line of each test case contains $n$, $b$, $k_1$, and $k_2$ ($1 \le n \le 5000$, $1 \le b \le 10^9$, $0 \le k_1, k_2 \le n$).</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ describing the array $a$ ($1 \le a_i \le 10^9$).</p><p>It is guaranteed the sum of $n$ over all test cases does not exceed $5000$.</p></div><div class="output-specification"><p>For each test case, print the minimum cost of $a$ you can achieve by performing the operations.</p></div>

## Input

<p>Input consists of multiple test cases. The first line contains a single integer $t$, the number of test cases ($1 \le t \le 5000$).</p><p>The first line of each test case contains $n$, $b$, $k_1$, and $k_2$ ($1 \le n \le 5000$, $1 \le b \le 10^9$, $0 \le k_1, k_2 \le n$).</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ describing the array $a$ ($1 \le a_i \le 10^9$).</p><p>It is guaranteed the sum of $n$ over all test cases does not exceed $5000$.</p>

## Output

<p>For each test case, print the minimum cost of $a$ you can achieve by performing the operations.</p>





```input1|2,3,6,7,10,11,14,15
7
3 2 1 1
9 3 5
2 1 2 0
1000000000 1
5 3 1 1
2 8 3 19 3
6 9 4 2
1 2 3 4 5 6
3 10 3 3
1 2 3
5 1 0 0
999999999 999999999 999999999 999999999 999999999
5 5 4 3
5 9 10 7 4
```




```output1
11
500000001
23
6
0
4999999995
6
```



## Note

<p>In the first test case, you can do the following: </p><ul> <li> Perform operation 2 on element $a_3$. It changes from $5$ to $3$. </li><li> Perform operation 1 on element $a_1$. It changes from $9$ to $5$. </li></ul><p>After these operations, the array is $a = [5, 3, 3]$ has a cost $5 + 3 + 3 = 11$. We can show that this is the minimum achievable cost.</p><p>In the second test case, note that we are not allowed to perform operation 1 more than once on $a_1$. So it is optimal to apply operation 1 once to each $a_1$ and $a_2$. Alternatively we could apply operation 1 only once to $a_1$, since it has no effect on $a_2$.</p><p>In the third test case, here is one way to achieve a cost of $23$: </p><ul> <li> Apply operation 1 to $a_4$. It changes from $19$ to $10$. </li><li> Apply operation 2 to $a_4$. It changes from $10$ to $7$. </li></ul><p>After these operations, $a = [2, 8, 3, 7, 3]$. The cost of $a$ is $2 + 8 + 3 + 7 + 3 = 23$. We can show that this is the minimum achievable cost.</p>
