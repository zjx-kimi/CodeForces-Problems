## Description

<div><p>You are given an array of integers $a_1, a_2, \ldots, a_n$. Calculate the number of <span class="tex-font-style-bf">subarrays</span> of this array $1 \leq l \leq r \leq n$, such that:</p><ul><li> The array $b = [a_l, a_{l+1}, \ldots, a_r]$ occurs in the array $a$ as a <span class="tex-font-style-bf">subsequence</span> exactly once. In other words, there is exactly one way to select a set of indices $1 \leq i_1 &lt; i_2 &lt; \ldots &lt; i_{r - l + 1} \leq n$, such that $b_j = a_{i_j}$ for all $1 \leq j \leq r - l + 1$.</li></ul></div><div class="input-specification"><p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 10^4$) — the number of test cases. This is followed by their description.</p><p>The first line of each test case contains an integer $n$ ($1 \leq n \leq 10^5$) — the size of the array $a$.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \leq a_i \leq 10^9$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output the number of suitable <span class="tex-font-style-bf">subarrays</span>.</p></div>

## Input

<p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 10^4$) — the number of test cases. This is followed by their description.</p><p>The first line of each test case contains an integer $n$ ($1 \leq n \leq 10^5$) — the size of the array $a$.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \leq a_i \leq 10^9$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output the number of suitable <span class="tex-font-style-bf">subarrays</span>.</p>





```input1|2,3,6,7,10,11
6
1
1
2
1 1
3
1 2 1
4
2 3 2 1
5
4 5 4 5 4
10
1 7 7 2 3 4 3 2 1 100
```




```output1
1
1
4
7
4
28
```



## Note

<p>In the first test case, there is exactly one subarray $(1, 1)$ that suits us.</p><p>In the second test case, there is exactly one subarray $(1, 2)$ that suits us. Subarrays $(1, 1)$ and $(2, 2)$ do not suit us, as the subsequence $[1]$ occurs twice in the array.</p><p>In the third test case, all subarrays except $(1, 1)$ and $(3, 3)$ are suitable.</p>
