## Description

<div><p>You are given an array $a_1, a_2, \dots, a_n$, consisting of $n$ integers. You are also given two integers $k$ and $x$.</p><p>You have to perform the following operation exactly once: add $x$ to the elements on <span class="tex-font-style-bf">exactly</span> $k$ <span class="tex-font-style-bf">distinct</span> positions, and subtract $x$ from all the others.</p><p>For example, if $a = [2, -1, 2, 3]$, $k = 1$, $x = 2$, and we have picked the first element, then after the operation the array $a = [4, -3, 0, 1]$.</p><p>Let $f(a)$ be the maximum possible sum of a subarray of $a$. The subarray of $a$ is a contiguous part of the array $a$, i. e. the array $a_i, a_{i + 1}, \dots, a_j$ for some $1 \le i \le j \le n$. An empty subarray should also be considered, it has sum $0$.</p><p>Let the array $a'$ be the array $a$ after applying the aforementioned operation. Apply the operation in such a way that $f(a')$ is the maximum possible, and print the maximum possible value of $f(a')$.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains three integers $n$, $k$ and $x$ ($1 \le n \le 2 \cdot 10^5$; $0 \le k \le \min(20, n)$; $-10^9 \le x \le 10^9$).</p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($-10^9 \le a_i \le 10^9$). </p><p>The sum of $n$ over all test cases doesn't exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, print one integer&nbsp;— the maximum possible value of $f(a')$.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains three integers $n$, $k$ and $x$ ($1 \le n \le 2 \cdot 10^5$; $0 \le k \le \min(20, n)$; $-10^9 \le x \le 10^9$).</p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($-10^9 \le a_i \le 10^9$). </p><p>The sum of $n$ over all test cases doesn't exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, print one integer&nbsp;— the maximum possible value of $f(a')$.</p>





```input1|2,3,6,7
4
4 1 2
2 -1 2 3
2 2 3
-1 2
3 0 5
3 2 4
6 2 -8
4 -1 9 -3 7 -8
```




```output1
5
7
0
44
```


