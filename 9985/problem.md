## Description

<div><p><span class="tex-font-style-bf">This is the easy version of the problem. The only difference between the two versions is the constraint on $t$ and $n$. You can make hacks only if both versions of the problem are solved.</span></p><p>For a binary$^\dagger$ <span class="tex-font-style-it">pattern</span> $p$ and a binary string $q$, both of length $m$, $q$ is called $p$-<span class="tex-font-style-it">good</span> if for every $i$ ($1 \leq i \leq m$), there exist indices $l$ and $r$ such that: </p><ul> <li> $1 \leq l \leq i \leq r \leq m$, and </li><li> $p_i$ is a mode$^\ddagger$ of the string $q_l q_{l+1} \ldots q_{r}$. </li></ul><p>For a pattern $p$, let $f(p)$ be the minimum possible number of $\mathtt{1}$s in a $p$-good binary string (of the same length as the pattern).</p><p>You are given a binary string $s$ of size $n$. Find $$\sum_{i=1}^{n} \sum_{j=i}^{n} f(s_i s_{i+1} \ldots s_j).$$ In other words, you need to sum the values of $f$ over all $\frac{n(n+1)}{2}$ substrings of $s$.</p><p>$^\dagger$ A binary <span class="tex-font-style-it">pattern</span> is a string that only consists of characters $\mathtt{0}$ and $\mathtt{1}$.</p><p>$^\ddagger$ Character $c$ is a mode of string $t$ of length $m$ if the number of occurrences of $c$ in $t$ is at least $\lceil \frac{m}{2} \rceil$. For example, $\mathtt{0}$ is a mode of $\mathtt{010}$, $\mathtt{1}$ is not a mode of $\mathtt{010}$, and both $\mathtt{0}$ and $\mathtt{1}$ are modes of $\mathtt{011010}$.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 500$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 100$)&nbsp;— the length of the binary string $s$.</p><p>The second line of each test case contains a binary string $s$ of length $n$ consisting of only characters $\mathtt{0}$ and $\mathtt{1}$.</p><p>It is guaranteed that the sum of $n^2$ over all test cases does not exceed $10^4$.</p></div><div class="output-specification"><p>For each test case, output the sum of values of $f$ over all substrings of $s$.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 500$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 100$)&nbsp;— the length of the binary string $s$.</p><p>The second line of each test case contains a binary string $s$ of length $n$ consisting of only characters $\mathtt{0}$ and $\mathtt{1}$.</p><p>It is guaranteed that the sum of $n^2$ over all test cases does not exceed $10^4$.</p>

## Output

<p>For each test case, output the sum of values of $f$ over all substrings of $s$.</p>





```input1|2,3,6,7
4
1
1
2
10
5
00000
20
11110110000000111111
```




```output1
1
2
0
346
```



## Note

<p>In the first test case, the only $\mathtt{1}$-good string is $\mathtt{1}$. Thus, $f(\mathtt{1})=1$.</p><p>In the second test case, $f(\mathtt{10})=1$ because $\mathtt{01}$ is $\mathtt{10}$-good, and $\mathtt{00}$ is not $\mathtt{10}$-good. Thus, the answer is $f(\mathtt{1})+f(\mathtt{10})+f(\mathtt{0}) = 1 + 1 + 0 = 2$.</p><p>In the third test case, $f$ equals to $0$ for all $1 \leq i \leq j \leq 5$. Thus, the answer is $0$.</p>
