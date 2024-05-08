## Description

<div><p>You are given a string $s$ of length $n$ consisting of lowercase English letters, and an integer $k$. In one step you can perform <span class="tex-font-style-bf">any one</span> of the two operations below:</p><ul> <li> Pick an index $i$ ($1 \le i \le n - 2$) and swap $s_{i}$ and $s_{i+2}$. </li><li> Pick an index $i$ ($1 \le i \le n-k+1$) and reverse the order of letters formed by the range $[i,i+k-1]$ of the string. Formally, if the string currently is equal to $s_1\ldots s_{i-1}s_is_{i+1}\ldots s_{i+k-2}s_{i+k-1}s_{i+k}\ldots s_{n-1}s_n$, change it to $s_1\ldots s_{i-1}s_{i+k-1}s_{i+k-2}\ldots s_{i+1}s_is_{i+k}\ldots s_{n-1}s_n$. </li></ul><p>You can make as many steps as you want (possibly, zero). Your task is to find the lexicographically <span class="tex-font-style-bf">smallest</span> string you can obtain after some number of steps. </p><p>A string $a$ is lexicographically smaller than a string $b$ of the same length if and only if the following holds: </p><ul> <li> in the first position where $a$ and $b$ differ, the string $a$ has a letter that appears earlier in the alphabet than the corresponding letter in $b$. </li></ul></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^4$). The description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $k$ ($1 \le k &lt; n \le 10^5$).</p><p>The second line of each test case contains the string $s$ of length $n$ consisting of lowercase English letters.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p></div><div class="output-specification"><p>For each test case, print the lexicographically <span class="tex-font-style-bf">smallest</span> string after doing some (possibly, zero) steps.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^4$). The description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $k$ ($1 \le k &lt; n \le 10^5$).</p><p>The second line of each test case contains the string $s$ of length $n$ consisting of lowercase English letters.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p>

## Output

<p>For each test case, print the lexicographically <span class="tex-font-style-bf">smallest</span> string after doing some (possibly, zero) steps.</p>





```input1|2,3,6,7,10,11
5
4 2
nima
5 3
panda
9 2
theforces
7 3
amirfar
6 4
rounds
```




```output1
aimn
aandp
ceefhorst
aafmirr
dnorsu
```



## Note

<p>In the first test case, we can obtain the string "<span class="tex-font-style-tt">aimn</span>" using the following operations:</p><ol> <li> Reverse the range $[3,4]$. The string turns into "<span class="tex-font-style-tt">niam</span>". </li><li> Swap $s_1$ and $s_3$. The string turns into "<span class="tex-font-style-tt">ainm</span>". </li><li> Reverse the range $[3,4]$. The string turns into "<span class="tex-font-style-tt">aimn</span>". </li></ol><p>It can be proven that we cannot obtain any string lexicographically smaller than "<span class="tex-font-style-tt">aimn</span>". Therefore, "<span class="tex-font-style-tt">aimn</span>" is the answer.</p><p>In the second test case, we can obtain the string "<span class="tex-font-style-tt">aandp</span>" using the following operations:</p><ol> <li> Swap $s_3$ and $s_5$. The string turns into "<span class="tex-font-style-tt">paadn</span>". </li><li> Swap $s_1$ and $s_3$. The string turns into "<span class="tex-font-style-tt">aapdn</span>". </li><li> Swap $s_3$ and $s_5$. The string turns into "<span class="tex-font-style-tt">aandp</span>". </li></ol><p>It can be proven that we cannot obtain any string lexicographically smaller than "<span class="tex-font-style-tt">aandp</span>". Therefore, "<span class="tex-font-style-tt">aandp</span>" is the answer.</p>
