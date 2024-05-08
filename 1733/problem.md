## Description

<div><p>You are given two arrays $a$ and $b$ of $n$ positive integers each. You can apply the following operation to them any number of times:</p><ul> <li> Select an index $i$ ($1\leq i\leq n$) and swap $a_i$ with $b_i$ (i.&nbsp;e. $a_i$ becomes $b_i$ and vice versa). </li></ul><p>Find the <span class="tex-font-style-bf">minimum</span> possible value of $\max(a_1, a_2, \ldots, a_n) \cdot \max(b_1, b_2, \ldots, b_n)$ you can get after applying such operation any number of times (possibly zero). </p></div><div class="input-specification"><p>The input consists of multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 100$) — the number of test cases. Description of the test cases follows.</p><p>The first line of each test case contains an integer $n$ ($1\le n\le 100$) — the length of the arrays.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le 10\,000$) where $a_i$ is the $i$-th element of the array $a$.</p><p>The third line of each test case contains $n$ integers $b_1, b_2, \ldots, b_n$ ($1 \le b_i \le 10\,000$) where $b_i$ is the $i$-th element of the array $b$.</p></div><div class="output-specification"><p>For each test case, print a single integer, the <span class="tex-font-style-bf">minimum</span> possible value of $\max(a_1, a_2, \ldots, a_n) \cdot \max(b_1, b_2, \ldots, b_n)$ you can get after applying such operation any number of times.</p></div>

## Input

<p>The input consists of multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 100$) — the number of test cases. Description of the test cases follows.</p><p>The first line of each test case contains an integer $n$ ($1\le n\le 100$) — the length of the arrays.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le 10\,000$) where $a_i$ is the $i$-th element of the array $a$.</p><p>The third line of each test case contains $n$ integers $b_1, b_2, \ldots, b_n$ ($1 \le b_i \le 10\,000$) where $b_i$ is the $i$-th element of the array $b$.</p>

## Output

<p>For each test case, print a single integer, the <span class="tex-font-style-bf">minimum</span> possible value of $\max(a_1, a_2, \ldots, a_n) \cdot \max(b_1, b_2, \ldots, b_n)$ you can get after applying such operation any number of times.</p>





```input1
3
6
1 2 6 5 1 2
3 4 3 2 2 5
3
3 3 3
3 3 3
2
1 2
2 1
```




```output1
18
9
2
```



## Note

<p>In the first test, you can apply the operations at indices $2$ and $6$, then $a = [1, 4, 6, 5, 1, 5]$ and $b = [3, 2, 3, 2, 2, 2]$, $\max(1, 4, 6, 5, 1, 5) \cdot \max(3, 2, 3, 2, 2, 2) = 6 \cdot 3 = 18$.</p><p>In the second test, no matter how you apply the operations, $a = [3, 3, 3]$ and $b = [3, 3, 3]$ will always hold, so the answer is $\max(3, 3, 3) \cdot \max(3, 3, 3) = 3 \cdot 3 = 9$.</p><p>In the third test, you can apply the operation at index $1$, then $a = [2, 2]$, $b = [1, 1]$, so the answer is $\max(2, 2) \cdot \max(1, 1) = 2 \cdot 1 = 2$.</p>
