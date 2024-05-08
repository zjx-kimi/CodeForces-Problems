## Description

<div><p>Sam started playing with round buckets in the sandbox, while also scattering pebbles. His mom decided to buy him a new bucket, so she needs to solve the following task.</p><p>You are given $n$ distinct points with integer coordinates $A_1, A_2, \ldots, A_n$. All points were generated from the square $[-10^8, 10^8] \times [-10^8, 10^8]$ uniformly and independently.</p><p>You are given positive integers $k$, $l$, such that $k \leq l \leq n$. You want to select a subsegment $A_i, A_{i+1}, \ldots, A_{i+l-1}$ of the points array (for some $1 \leq i \leq n + 1 - l$), and some circle on the plane, containing $\geq k$ points of the selected subsegment (inside or on the border).</p><p>What is the smallest possible radius of that circle?</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 10^4$) — the number of test cases. Descriptions of test cases follow.</p><p>The first line of each test case contains three integers $n$, $l$, $k$ ($2 \leq k \leq l \leq n \leq 50\,000$, $k \leq 20$).</p><p>Each of the next $n$ lines contains two integers $x_i$, $y_i$ ($-10^8 \leq x_i, y_i \leq 10^8$) — the coordinates of the point $A_i$. It is guaranteed that all points are distinct and were generated independently from uniform distribution on $[-10^8, 10^8] \times [-10^8, 10^8]$.</p><p>It is guaranteed that the sum of $n$ for all test cases does not exceed $50\,000$.</p><p>In the first test, points were not generated from the uniform distribution on $[-10^8, 10^8] \times [-10^8, 10^8]$ for simplicity. It is <span class="tex-font-style-bf">the only</span> such test and your solution <span class="tex-font-style-bf">must</span> pass it.</p><p><span class="tex-font-style-bf">Hacks are disabled in this problem.</span></p></div><div class="output-specification"><p>For each test case print a single real number — the answer to the problem.</p><p>Your answer will be considered correct if its absolute or relative error does not exceed $10^{-9}$. Formally let your answer be $a$, jury answer be $b$. Your answer will be considered correct if $\frac{|a - b|}{\max{(1, |b|)}} \le 10^{-9}$.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 10^4$) — the number of test cases. Descriptions of test cases follow.</p><p>The first line of each test case contains three integers $n$, $l$, $k$ ($2 \leq k \leq l \leq n \leq 50\,000$, $k \leq 20$).</p><p>Each of the next $n$ lines contains two integers $x_i$, $y_i$ ($-10^8 \leq x_i, y_i \leq 10^8$) — the coordinates of the point $A_i$. It is guaranteed that all points are distinct and were generated independently from uniform distribution on $[-10^8, 10^8] \times [-10^8, 10^8]$.</p><p>It is guaranteed that the sum of $n$ for all test cases does not exceed $50\,000$.</p><p>In the first test, points were not generated from the uniform distribution on $[-10^8, 10^8] \times [-10^8, 10^8]$ for simplicity. It is <span class="tex-font-style-bf">the only</span> such test and your solution <span class="tex-font-style-bf">must</span> pass it.</p><p><span class="tex-font-style-bf">Hacks are disabled in this problem.</span></p>

## Output

<p>For each test case print a single real number — the answer to the problem.</p><p>Your answer will be considered correct if its absolute or relative error does not exceed $10^{-9}$. Formally let your answer be $a$, jury answer be $b$. Your answer will be considered correct if $\frac{|a - b|}{\max{(1, |b|)}} \le 10^{-9}$.</p>





```input1
4
3 2 2
0 0
0 4
3 0
5 4 3
1 1
0 0
2 2
0 2
2 0
8 3 2
0 3
1 0
0 2
1 1
0 1
1 2
0 0
1 3
5 4 4
1 1
-3 3
2 2
5 3
5 5
```




```output1
2.00000000000000000000
1.00000000000000000000
0.50000000000000000000
4.00000000000000000000
```



## Note

<p>In the first test case, we can select subsegment $A_1, A_2$ and a circle with center $(0, 2)$ and radius $2$.</p><p>In the second test case, we can select subsegment $A_1, A_2, A_3, A_4$ and a circle with center $(1, 2)$ and radius $1$.</p>
