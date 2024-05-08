## Description

<div><p>There is a hidden array $a$ of size $n$ consisting of only $1$ and $-1$. Let $p$ be the prefix sums of array $a$. More formally, $p$ is an array of length $n$ defined as $p_i = a_1 + a_2 + \ldots + a_i$. Afterwards, array $p$ is sorted in non-decreasing order. For example, if $a = [1, -1, -1, 1, 1]$, then $p = [1, 0, -1, 0, 1]$ before sorting and $p = [-1, 0, 0, 1, 1]$ after sorting.</p><p>You are given the prefix sum array $p$ after sorting, but you do not know what array $a$ is. Your task is to count the number of initial arrays $a$ such that the above process results in the given sorted prefix sum array $p$. As this number can be large, you are only required to find it modulo $998\,244\,353$.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 1000$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 5000$)&nbsp;— the size of the hidden array $a$.</p><p>The second line of each test case contains $n$ integers $p_1, p_2, \ldots, p_n$ ($|p_i| \le n$)&nbsp;— the $n$ prefix sums of $a$ sorted in non-decreasing order.</p><p>It is guaranteed that $p_1 \le p_2 \le \ldots \le p_n$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $5000$.</p></div><div class="output-specification"><p>For each test case, output the answer modulo $998\,244\,353$.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 1000$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 5000$)&nbsp;— the size of the hidden array $a$.</p><p>The second line of each test case contains $n$ integers $p_1, p_2, \ldots, p_n$ ($|p_i| \le n$)&nbsp;— the $n$ prefix sums of $a$ sorted in non-decreasing order.</p><p>It is guaranteed that $p_1 \le p_2 \le \ldots \le p_n$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $5000$.</p>

## Output

<p>For each test case, output the answer modulo $998\,244\,353$.</p>





```input1|2,3,6,7,10,11
5
1
0
1
1
3
-1 1 2
5
-1 0 0 1 1
5
-4 -3 -3 -2 -1
```




```output1
0
1
0
3
1
```



## Note

<p>In the first two test cases, the only possible arrays $a$ for $n = 1$ are $a = [1]$ and $a = [-1]$. Their respective sorted prefix sum arrays $p$ are $p = [1]$ and $p = [-1]$. Hence, there is no array $a$ that can result in the sorted prefix sum array $p = [0]$ and there is exactly $1$ array $a$ that can result in the sorted prefix sum array $p = [1]$.</p><p>In the third test case, it can be proven that there is no array $a$ that could result in the sorted prefix sum array $p = [-1, 1, 2]$.</p><p>In the fourth test case, the $3$ possible arrays $a$ that could result in the sorted prefix sum array $p = [-1, 0, 0, 1, 1]$ are:</p><ul> <li> $a = [1, -1, 1, -1, -1]$. The prefix sum array before sorting is $p = [1, 0, 1, 0, -1]$, which after sorting gives $p = [-1, 0, 0, 1, 1]$. </li><li> $a = [1, -1, -1, 1, 1]$. The prefix sum array before sorting is $p = [1, 0, -1, 0, 1]$, which after sorting gives $p = [-1, 0, 0, 1, 1]$. </li><li> $a = [-1, 1, 1, -1, 1]$. The prefix sum array before sorting is $p = [-1, 0, 1, 0, 1]$, which after sorting gives $p = [-1, 0, 0, 1, 1]$. </li></ul><p>For the fifth test case, the only possible array $a$ that could result in the sorted prefix sum array $p = [-4, -3, -3, -2, -1]$ is $a = [-1, -1, -1, -1, 1]$.</p>
