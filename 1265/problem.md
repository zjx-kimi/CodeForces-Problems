## Description

<div><p>A <span class="tex-font-style-bf">$\mathbf{0}$-indexed</span> array $a$ of size $n$ is called <span class="tex-font-style-it">good</span> if for all valid indices $i$ ($0 \le i \le n-1$), $a_i + i$ is a perfect square$^\dagger$.</p><p>Given an integer $n$. Find a permutation$^\ddagger$ $p$ of $[0,1,2,\ldots,n-1]$ that is good or determine that no such permutation exists.</p><p>$^\dagger$ An integer $x$ is said to be a perfect square if there exists an integer $y$ such that $x = y^2$.</p><p>$^\ddagger$ An array $b$ is a permutation of an array $a$ if $b$ consists of the elements of $a$ in arbitrary order. For example, $[4,2,3,4]$ is a permutation of $[3,2,4,4]$ while $[1,2,2]$ is not a permutation of $[1,2,3]$.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^4$) — the number of test cases.</p><p>The only line of each test case contains a single integer $n$ ($1 \le n \le 10^5$) — the length of the permutation $p$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p></div><div class="output-specification"><p>For each test case, output $n$ distinct integers $p_0, p_1, \dots, p_{n-1}$ ($0 \le p_i \le n-1$) — the permutation $p$ — if the answer exists, and $-1$ otherwise.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^4$) — the number of test cases.</p><p>The only line of each test case contains a single integer $n$ ($1 \le n \le 10^5$) — the length of the permutation $p$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p>

## Output

<p>For each test case, output $n$ distinct integers $p_0, p_1, \dots, p_{n-1}$ ($0 \le p_i \le n-1$) — the permutation $p$ — if the answer exists, and $-1$ otherwise.</p>





```input1|2,4
3
3
4
7
```




```output1
1 0 2 
0 3 2 1 
1 0 2 6 5 4 3
```



## Note

<p>In the first test case, we have $n=3$. The array $p = [1, 0, 2]$ is good since $1 + 0 = 1^2$, $0 + 1 = 1^2$, and $2 + 2 = 2^2$</p><p>In the second test case, we have $n=4$. The array $p = [0, 3, 2, 1]$ is good since $0 + 0 = 0^2$, $3 + 1 = 2^2$, $2+2 = 2^2$, and $1+3 = 2^2$.</p>
