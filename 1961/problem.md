## Description

<div><p>You are given an array $a$ of length $n$.</p><p>Let's define the <span class="tex-font-style-it">eversion</span> operation. Let $x = a_n$. Then array $a$ is partitioned into two parts: left and right. The left part contains the elements of $a$ that are not greater than $x$ ($\le x$). The right part contains the elements of $a$ that are strictly greater than $x$ ($&gt; x$). The order of elements in each part is kept the same as before the operation, i.&nbsp;e. the partition is stable. Then the array is replaced with the concatenation of the left and the right parts.</p><p>For example, if the array $a$ is $[2, 4, 1, 5, 3]$, the eversion goes like this: $[2, 4, 1, 5, 3] \to [2, 1, 3], [4, 5] \to [2, 1, 3, 4, 5]$.</p><p>We start with the array $a$ and perform eversions on this array. We can prove that after several eversions the array $a$ stops changing. Output the minimum number $k$ such that the array stops changing after $k$ eversions.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 100$). Description of the test cases follows.</p><p>The first line contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$).</p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le 10^9$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case print a single integer $k$ — the number of eversions after which the array stops changing.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 100$). Description of the test cases follows.</p><p>The first line contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$).</p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le 10^9$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case print a single integer $k$ — the number of eversions after which the array stops changing.</p>





```input1
3
5
2 4 1 5 3
5
5 3 2 4 1
4
1 1 1 1
```




```output1
1
2
0
```



## Note

<p>Consider the fist example.</p><ul> <li> The first eversion: $a = [1, 4, 2, 5, 3]$, $x = 3$. $[2, 4, 1, 5, 3] \to [2, 1, 3], [4, 5] \to [2, 1, 3, 4, 5]$. </li><li> The second and following eversions: $a = [2, 1, 3, 4, 5]$, $x = 5$. $[2, 1, 3, 4, 5] \to [2, 1, 3, 4, 5], [] \to [2, 1, 3, 4, 5]$. This eversion does not change the array, so the answer is $1$. </li></ul><p>Consider the second example. </p><ul> <li> The first eversion: $a = [5, 3, 2, 4, 1]$, $x = 1$. $[5, 3, 2, 4, 1] \to [1], [5, 3, 2, 4] \to [1, 5, 3, 2, 4]$. </li><li> The second eversion: $a = [1, 5, 3, 2, 4]$, $x = 4$. $[1, 5, 3, 2, 4] \to [1, 3, 2, 4], [5] \to [1, 3, 2, 4, 5]$. </li><li> The third and following eversions: $a = [1, 3, 2, 4, 5]$, $x = 5$. $[1, 3, 2, 4, 5] \to [1, 3, 2, 4, 5], [] \to [1, 3, 2, 4, 5]$. This eversion does not change the array, so the answer is $2$. </li></ul>
