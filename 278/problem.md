## Description

<div><p>You are given an array of integers $a_1, a_2, \ldots, a_n$.</p><p>A pair of integers $(i, j)$, such that $1 \le i &lt; j \le n$, is called <span class="tex-font-style-it">good</span>, if there <span class="tex-font-style-bf">does not exist</span> an integer $k$ ($1 \le k \le n$) such that $a_i$ is divisible by $a_k$ and $a_j$ is divisible by $a_k$ at the same time.</p><p>Please, find the number of good pairs.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 2 \cdot 10^4$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 10^6$).</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le n$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^6$.</p></div><div class="output-specification"><p>For each test case, output the number of good pairs.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 2 \cdot 10^4$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 10^6$).</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le n$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^6$.</p>

## Output

<p>For each test case, output the number of good pairs.</p>





```input1|2,3,6,7,10,11
6
4
2 4 4 4
4
2 3 4 4
9
6 8 9 4 6 8 9 4 9
9
7 7 4 4 9 9 6 2 9
18
10 18 18 15 14 4 5 6 8 9 10 12 15 16 18 17 13 11
21
12 19 19 18 18 12 2 18 19 12 12 3 12 12 12 18 19 16 18 19 12
```




```output1
0
3
26
26
124
82
```



## Note

<p>In the first test case, there are no good pairs. </p><p>In the second test case, here are all the good pairs: $(1, 2)$, $(2, 3)$, and $(2, 4)$.</p>
