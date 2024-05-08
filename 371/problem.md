## Description

<div><p>You are given a binary string $s$ of length $n$ (a string that consists only of $0$ and $1$). A number $x$ is good if there exists a binary string $l$ of length $n$, containing $x$ ones, such that if each symbol $s_i$ is replaced by $s_i \oplus l_i$ (where $\oplus$ denotes the <a href="https://en.wikipedia.org/wiki/Bitwise_operation#XOR">bitwise XOR operation</a>), then the string $s$ becomes a palindrome.</p><p>You need to output a binary string $t$ of length $n+1$, where $t_i$ ($0 \leq i \leq n$) is equal to $1$ if number $i$ is good, and $0$ otherwise.</p><p>A palindrome is a string that reads the same from left to right as from right to left. For example, <span class="tex-font-style-tt">01010</span>, <span class="tex-font-style-tt">1111</span>, <span class="tex-font-style-tt">0110</span> are palindromes.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^5$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 10^5$).</p><p>The second line of each test case contains a binary string $s$ of length $n$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p></div><div class="output-specification"><p>For each test case, output a single line containing a binary string $t$ of length $n+1$ - the answer to the problem.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^5$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 10^5$).</p><p>The second line of each test case contains a binary string $s$ of length $n$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p>

## Output

<p>For each test case, output a single line containing a binary string $t$ of length $n+1$ - the answer to the problem.</p>





```input1|2,3,6,7,10,11
5
6
101011
5
00000
9
100100011
3
100
1
1
```




```output1
0010100
111111
0011111100
0110
11
```



## Note

<p>Consider the first example. </p><ul> <li> $t_2 = 1$ because we can choose $l = $ <span class="tex-font-style-tt">010100</span>, then the string $s$ becomes <span class="tex-font-style-tt">111111</span>, which is a palindrome. </li><li> $t_4 = 1$ because we can choose $l = $ <span class="tex-font-style-tt">101011</span>. </li><li> It can be shown that for all other $i$, there is no answer, so the remaining symbols are $0$. </li></ul>
