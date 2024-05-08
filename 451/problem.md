## Description

<div><p>Ntarsis has an array $a$ of length $n$.</p><p>The <span class="tex-font-style-it">power</span> of a subarray $a_l \dots a_r$ ($1 \leq l \leq r \leq n$) is defined as: </p><ul> <li> The largest value $x$ such that $a_l \dots a_r$ contains $x$ and neither $a_1 \dots a_{l-1}$ nor $a_{r+1} \dots a_n$ contains $x$. </li><li> If no such $x$ exists, the power is $0$. </li></ul><p>Call an array $b$ a <span class="tex-font-style-it">rival</span> to $a$ if the following holds: </p><ul> <li> The length of both $a$ and $b$ are equal to some $n$. </li><li> Over all $l, r$ where $1 \leq l \leq r \leq n$, the power of $a_l \dots a_r$ equals the power of $b_l \dots b_r$. </li><li> The elements of $b$ are positive. </li></ul><p>Ntarsis wants you to find a rival $b$ to $a$ such that the sum of $b_i$ over $1 \leq i \leq n$ is maximized. Help him with this task!</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^5$). The description of the test cases follows.</p><p>The first line of each test case has a single integer $n$ ($1 \leq n \leq 10^5$).</p><p>The next line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \leq a_i \leq 10^9$).</p><p>It is guaranteed that the sum of $n$ across all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output $n$ integers $b_1, b_2, \ldots, b_n$&nbsp;— a valid rival to $a$ such that $b_1 + b_2 + \cdots + b_n$ is maximal. </p><p>If there exist multiple rivals with the maximum sum, output any of them.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^5$). The description of the test cases follows.</p><p>The first line of each test case has a single integer $n$ ($1 \leq n \leq 10^5$).</p><p>The next line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \leq a_i \leq 10^9$).</p><p>It is guaranteed that the sum of $n$ across all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output $n$ integers $b_1, b_2, \ldots, b_n$&nbsp;— a valid rival to $a$ such that $b_1 + b_2 + \cdots + b_n$ is maximal. </p><p>If there exist multiple rivals with the maximum sum, output any of them.</p>





```input1|2,3,6,7,10,11,14,15
7
5
1 4 1 3 3
5
1 4 1 8 8
5
2 1 1 1 2
8
3 2 3 5 2 2 5 3
8
1 1 1 1 4 3 3 3
10
1 9 5 9 8 1 5 8 9 1
16
1 1 1 1 5 5 5 5 9 9 9 9 7 7 7 7
```




```output1
2 4 2 3 3
3 4 3 8 8
2 1 2 1 2
4 2 4 5 5 2 5 4
1 2 2 1 4 3 2 3
7 9 5 9 8 9 5 8 9 7
1 8 8 1 5 8 8 5 9 9 9 9 7 8 8 7
```



## Note

<p>For the first test case, one rival with the maximal sum is $[2, 4, 2, 3, 3]$.</p><p>$[2, 4, 2, 3, 3]$ can be shown to be a rival to $[1, 4, 1, 3, 3]$.</p><p>All possible subarrays of $a$ and $b$ and their corresponding powers are listed below: </p><ul> <li> The power of $a[1:1] = [1] = 0$, the power of $b[1:1] = [2] = 0$. </li><li> The power of $a[1:2] = [1, 4] = 4$, the power of $b[1:2] = [2, 4] = 4$. </li><li> The power of $a[1:3] = [1, 4, 1] = 4$, the power of $b[1:3] = [2, 4, 2] = 4$. </li><li> The power of $a[1:4] = [1, 4, 1, 3] = 4$, the power of $b[1:4] = [2, 4, 2, 3] = 4$. </li><li> The power of $a[1:5] = [1, 4, 1, 3, 3] = 4$, the power of $b[1:5] = [2, 4, 2, 3, 3] = 4$. </li><li> The power of $a[2:2] = [4] = 4$, the power of $b[2:2] = [4] = 4$. </li><li> The power of $a[2:3] = [4, 1] = 4$, the power of $b[2:3] = [4, 2] = 4$. </li><li> The power of $a[2:4] = [4, 1, 3] = 4$, the power of $b[2:4] = [4, 2, 3] = 4$. </li><li> The power of $a[2:5] = [4, 1, 3, 3] = 4$, the power of $b[2:5] = [4, 2, 3, 3] = 4$. </li><li> The power of $a[3:3] = [1] = 0$, the power of $b[3:3] = [2] = 0$. </li><li> The power of $a[3:4] = [1, 3] = 0$, the power of $b[3:4] = [2, 3] = 0$. </li><li> The power of $a[3:5] = [1, 3, 3] = 3$, the power of $b[3:5] = [2, 3, 3] = 3$. </li><li> The power of $a[4:4] = [3] = 0$, the power of $b[4:4] = [3] = 0$. </li><li> The power of $a[4:5] = [3, 3] = 3$, the power of $b[4:5] = [3, 3] = 3$. </li><li> The power of $a[5:5] = [3] = 0$, the power of $b[5:5] = [3] = 0$. </li></ul><p>It can be shown there exists no rival with a greater sum than $2 + 4 + 2 + 3 + 3 = 14$.</p>
