## Description

<div><p>For a collection of integers $S$, define $\operatorname{mex}(S)$ as the smallest non-negative integer that does not appear in $S$.</p><p>NIT, the cleaver, decides to destroy the universe. He is not so powerful as Thanos, so he can only destroy the universe by snapping his fingers several times.</p><p>The universe can be represented as a 1-indexed array $a$ of length $n$. When NIT snaps his fingers, he does the following operation on the array:</p><ul> <li> He selects positive integers $l$ and $r$ such that $1\le l\le r\le n$. Let $w=\operatorname{mex}(\{a_l,a_{l+1},\dots,a_r\})$. Then, for all $l\le i\le r$, set $a_i$ to $w$. </li></ul><p>We say the universe is destroyed if and only if for all $1\le i\le n$, $a_i=0$ holds.</p><p>Find the minimum number of times NIT needs to snap his fingers to destroy the universe. That is, find the minimum number of operations NIT needs to perform to make all elements in the array equal to $0$.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^4$). Description of the test cases follows.</p><p>The first line of each test case contains one integer $n$ ($1\le n\le 10^5$).</p><p>The second line of each test case contains $n$ integers $a_1$, $a_2$, $\ldots$, $a_n$ ($0\le a_i\le 10^9$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2\cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, print one integer — the answer to the problem.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^4$). Description of the test cases follows.</p><p>The first line of each test case contains one integer $n$ ($1\le n\le 10^5$).</p><p>The second line of each test case contains $n$ integers $a_1$, $a_2$, $\ldots$, $a_n$ ($0\le a_i\le 10^9$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2\cdot 10^5$.</p>

## Output

<p>For each test case, print one integer — the answer to the problem.</p>





```input1|2,3,6,7
4
4
0 0 0 0
5
0 1 2 3 4
7
0 2 3 0 1 2 0
1
1000000000
```




```output1
0
1
2
1
```



## Note

<p>In the first test case, we do $0$ operations and all elements in the array are already equal to $0$.</p><p>In the second test case, one optimal way is doing the operation with $l=2$, $r=5$.</p><p>In the third test case, one optimal way is doing the operation twice, respectively with $l=4$, $r=4$ and $l=2$, $r=6$.</p><p>In the fourth test case, one optimal way is doing the operation with $l=1$, $r=1$.</p>
