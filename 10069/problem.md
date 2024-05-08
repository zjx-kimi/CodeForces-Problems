## Description

<div><p>You are given a binary string$^\dagger$ $s$ of length $n$.</p><p>A binary string $p$ of the same length $n$ is called <span class="tex-font-style-bf">good</span> if for every $i$ ($1 \leq i \leq n$), there exist indices $l$ and $r$ such that: </p><ul> <li> $1 \leq l \leq i \leq r \leq n$ </li><li> $s_i$ is a mode$^\ddagger$ of the string $p_lp_{l+1}\ldots p_r$ </li></ul><p>You are given another binary string $t$ of length $n$. Find the minimum Hamming distance$^\S$ between $t$ and any <span class="tex-font-style-bf">good</span> string $g$.</p><p>$^\dagger$ A binary string is a string that only consists of characters $\mathtt{0}$ and $\mathtt{1}$.</p><p>$^\ddagger$ Character $c$ is a mode of string $p$ of length $m$ if the number of occurrences of $c$ in $p$ is at least $\lceil \frac{m}{2} \rceil$. For example, $\mathtt{0}$ is a mode of $\mathtt{010}$, $\mathtt{1}$ is not a mode of $\mathtt{010}$, and both $\mathtt{0}$ and $\mathtt{1}$ are modes of $\mathtt{011010}$.</p><p>$^\S$ The Hamming distance of strings $a$ and $b$ of length $m$ is the number of indices $i$ such that $1 \leq i \leq m$ and $a_i \neq b_i$.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^5$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 10^4$)&nbsp;— the length of the binary string $s$.</p><p>The second line of each test case contains a binary string $s$ of length $n$ consisting of characters <span class="tex-font-style-tt">0</span> and <span class="tex-font-style-tt">1</span>.</p><p>The third line of each test case contains a binary string $t$ of length $n$ consisting of characters <span class="tex-font-style-tt">0</span> and <span class="tex-font-style-tt">1</span>.</p><p>It is guaranteed that the <span class="tex-font-style-bf">sum of $n$</span> over all test cases does not exceed $10^6$, with the additional assurance that the <span class="tex-font-style-bf">sum of $n^2$</span> over all test cases does not exceed $10^8$</p></div><div class="output-specification"><p>For each test case, print the minimum Hamming distance between $t$ and any <span class="tex-font-style-bf">good</span> string $g$.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^5$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 10^4$)&nbsp;— the length of the binary string $s$.</p><p>The second line of each test case contains a binary string $s$ of length $n$ consisting of characters <span class="tex-font-style-tt">0</span> and <span class="tex-font-style-tt">1</span>.</p><p>The third line of each test case contains a binary string $t$ of length $n$ consisting of characters <span class="tex-font-style-tt">0</span> and <span class="tex-font-style-tt">1</span>.</p><p>It is guaranteed that the <span class="tex-font-style-bf">sum of $n$</span> over all test cases does not exceed $10^6$, with the additional assurance that the <span class="tex-font-style-bf">sum of $n^2$</span> over all test cases does not exceed $10^8$</p>

## Output

<p>For each test case, print the minimum Hamming distance between $t$ and any <span class="tex-font-style-bf">good</span> string $g$.</p>





```input1|2,3,4,8,9,10
3
3
000
000
4
0000
1111
6
111111
000100
```




```output1
0
2
1
```



## Note

<p>In the first test case, $g=\mathtt{000}$ is a good string which has Hamming distance $0$ from $t$.</p><p>In the second test case, $g=\mathtt{0011}$ is a good string which has Hamming distance $2$ from $t$. It can be proven that there are no good strings with Hamming distance less than $2$ from $t$.</p><p>In the third test case, $g=\mathtt{001100}$ is a good string which has Hamming distance $1$ from $t$.</p>
