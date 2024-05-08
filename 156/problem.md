## Description

<div><p>For an array $a$, define its <span class="tex-font-style-it">cost</span> as $\sum_{i=1}^{n} \operatorname{mex} ^\dagger ([a_1,a_2,\ldots,a_i])$.</p><p>You are given a permutation$^\ddagger$ $p$ of the set $\{0,1,2,\ldots,n-1\}$. Find the maximum cost across all cyclic shifts of $p$.</p><p>$^\dagger\operatorname{mex}([b_1,b_2,\ldots,b_m])$ is the smallest non-negative integer $x$ such that $x$ does not occur among $b_1,b_2,\ldots,b_m$.</p><p>$^\ddagger$A permutation of the set $\{0,1,2,...,n-1\}$ is an array consisting of $n$ distinct integers from $0$ to $n-1$ in arbitrary order. For example, $[1,2,0,4,3]$ is a permutation, but $[0,1,1]$ is not a permutation ($1$ appears twice in the array), and $[0,2,3]$ is also not a permutation ($n=3$ but there is $3$ in the array).</p></div><div class="input-specification"><p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 10^5$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 10^6$)&nbsp;— the length of the permutation $p$.</p><p>The second line of each test case contain $n$ distinct integers $p_1, p_2, \ldots, p_n$ ($0 \le p_i &lt; n$) — the elements of the permutation $p$.</p><p>It is guaranteed that sum of $n$ over all test cases does not exceed $10^6$.</p></div><div class="output-specification"><p>For each test case, output a single integer — the maximum cost across all cyclic shifts of $p$.</p></div>

## Input

<p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 10^5$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 10^6$)&nbsp;— the length of the permutation $p$.</p><p>The second line of each test case contain $n$ distinct integers $p_1, p_2, \ldots, p_n$ ($0 \le p_i &lt; n$) — the elements of the permutation $p$.</p><p>It is guaranteed that sum of $n$ over all test cases does not exceed $10^6$.</p>

## Output

<p>For each test case, output a single integer — the maximum cost across all cyclic shifts of $p$.</p>





```input1|2,3,6,7
4
6
5 4 3 2 1 0
3
2 1 0
8
2 3 6 7 0 1 4 5
1
0
```




```output1
15
5
31
1
```



## Note

<p>In the first test case, the cyclic shift that yields the maximum cost is $[2,1,0,5,4,3]$ with cost $0+0+3+3+3+6=15$.</p><p>In the second test case, the cyclic shift that yields the maximum cost is $[0,2,1]$ with cost $1+1+3=5$.</p>
