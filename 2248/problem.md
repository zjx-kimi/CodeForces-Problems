## Description

<div><p><span class="tex-font-style-it">Prefix function</span> of string $t = t_1 t_2 \ldots t_n$ and position $i$ in it is defined as the length $k$ of the longest proper (not equal to the whole substring) prefix of substring $t_1 t_2 \ldots t_i$ which is also a suffix of the same substring.</p><p>For example, for string $t = $ <span class="tex-font-style-tt">abacaba</span> the values of the prefix function in positions $1, 2, \ldots, 7$ are equal to $[0, 0, 1, 0, 1, 2, 3]$.</p><p>Let $f(t)$ be equal to the <span class="tex-font-style-it">maximum</span> value of the prefix function of string $t$ over all its positions. For example, $f($<span class="tex-font-style-tt">abacaba</span>$) = 3$.</p><p>You are given a string $s$. Reorder its characters arbitrarily to get a string $t$ (the number of occurrences of any character in strings $s$ and $t$ must be equal). The value of $f(t)$ must be <span class="tex-font-style-it">minimized</span>. Out of all options to minimize $f(t)$, choose the one where string $t$ is the <span class="tex-font-style-it">lexicographically smallest</span>.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^5$). Description of the test cases follows.</p><p>The only line of each test case contains string $s$ ($1 \le |s| \le 10^5$) consisting of lowercase English letters.</p><p>It is guaranteed that the sum of lengths of $s$ over all test cases does not exceed $10^5$.</p></div><div class="output-specification"><p>For each test case print a single string $t$.</p><p>The multisets of letters in strings $s$ and $t$ must be equal. The value of $f(t)$, the maximum of prefix functions in string $t$, must be as small as possible. String $t$ must be the lexicographically smallest string out of all strings satisfying the previous conditions.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^5$). Description of the test cases follows.</p><p>The only line of each test case contains string $s$ ($1 \le |s| \le 10^5$) consisting of lowercase English letters.</p><p>It is guaranteed that the sum of lengths of $s$ over all test cases does not exceed $10^5$.</p>

## Output

<p>For each test case print a single string $t$.</p><p>The multisets of letters in strings $s$ and $t$ must be equal. The value of $f(t)$, the maximum of prefix functions in string $t$, must be as small as possible. String $t$ must be the lexicographically smallest string out of all strings satisfying the previous conditions.</p>





```input1
3
vkcup
abababa
zzzzzz
```




```output1
ckpuv
aababab
zzzzzz
```



## Note

<p>A string $a$ is lexicographically smaller than a string $b$ if and only if one of the following holds:</p><ul><li> $a$ is a prefix of $b$, but $a \ne b$;</li><li> in the first position where $a$ and $b$ differ, the string $a$ has a letter that appears earlier in the alphabet than the corresponding letter in $b$.</li></ul><p>In the first test case, $f(t) = 0$ and the values of prefix function are $[0, 0, 0, 0, 0]$ for any permutation of letters. String <span class="tex-font-style-tt">ckpuv</span> is the lexicographically smallest permutation of letters of string <span class="tex-font-style-tt">vkcup</span>.</p><p>In the second test case, $f(t) = 1$ and the values of prefix function are $[0, 1, 0, 1, 0, 1, 0]$.</p><p>In the third test case, $f(t) = 5$ and the values of prefix function are $[0, 1, 2, 3, 4, 5]$.</p>
