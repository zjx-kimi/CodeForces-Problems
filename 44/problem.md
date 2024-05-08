## Description

<div><p>Patrick calls a substring$^\dagger$ of a binary string$^\ddagger$ <span class="tex-font-style-it">good</span> if this substring contains exactly one <span class="tex-font-style-tt">1</span>. </p><p>Help Patrick count the number of binary strings $s$ such that $s$ contains exactly $n$ good substrings and has no good substring of length strictly greater than $k$. Note that substrings are differentiated by their location in the string, so if $s =$ <span class="tex-font-style-tt">1010</span> you should count both occurrences of <span class="tex-font-style-tt">10</span>.</p><p>$^\dagger$ A string $a$ is a substring of a string $b$ if $a$ can be obtained from $b$ by the deletion of several (possibly, zero or all) characters from the beginning and several (possibly, zero or all) characters from the end.</p><p>$^\ddagger$ A binary string is a string that only contains the characters <span class="tex-font-style-tt">0</span> and <span class="tex-font-style-tt">1</span>.</p></div><div class="input-specification"><p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 2500$) — the number of test cases. The description of the test cases follows.</p><p>The only line of each test case contains two integers $n$ and $k$ ($1 \leq n \leq 2500$, $1 \leq k \leq n$) — the number of required good substrings and the maximum allowed length of a good substring. </p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2500$. </p></div><div class="output-specification"><p>For each test case, output a single integer — the number of binary strings $s$ such that $s$ contains exactly $n$ good substrings and has no good substring of length strictly greater than $k$. Since this integer can be too large, output it modulo $998\,244\,353$.</p></div>

## Input

<p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 2500$) — the number of test cases. The description of the test cases follows.</p><p>The only line of each test case contains two integers $n$ and $k$ ($1 \leq n \leq 2500$, $1 \leq k \leq n$) — the number of required good substrings and the maximum allowed length of a good substring. </p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2500$. </p>

## Output

<p>For each test case, output a single integer — the number of binary strings $s$ such that $s$ contains exactly $n$ good substrings and has no good substring of length strictly greater than $k$. Since this integer can be too large, output it modulo $998\,244\,353$.</p>





```input1|2,4,6
6
1 1
3 2
4 2
5 4
6 2
2450 2391
```




```output1
1
3
5
12
9
259280854
```



## Note

<p>In the first test case, the only suitable binary string is <span class="tex-font-style-tt">1</span>. String <span class="tex-font-style-tt">01</span> is not suitable because it contains a substring <span class="tex-font-style-tt">01</span> with length $2 &gt; 1$.</p><p>In the second test case, suitable binary strings are <span class="tex-font-style-tt">011</span>, <span class="tex-font-style-tt">110</span> and <span class="tex-font-style-tt">111</span>.</p><p>In the third test case, suitable binary strings are <span class="tex-font-style-tt">101</span>, <span class="tex-font-style-tt">0110</span>, <span class="tex-font-style-tt">0111</span>, <span class="tex-font-style-tt">1110</span>, and <span class="tex-font-style-tt">1111</span>.</p>
