## Description

<div><p>Given is a string $s$ of length $n$. In one operation you can select the lexicographically largest$^\dagger$ subsequence of string $s$ and cyclic shift it to the right$^\ddagger$. </p><p>Your task is to calculate the minimum number of operations it would take for $s$ to become sorted, or report that it never reaches a sorted state.</p><p>$^\dagger$A string $a$ is lexicographically smaller than a string $b$ if and only if one of the following holds:</p><ul><li> $a$ is a prefix of $b$, but $a \ne b$;</li><li> In the first position where $a$ and $b$ differ, the string $a$ has a letter that appears earlier in the alphabet than the corresponding letter in $b$.</li></ul><p>$^\ddagger$By cyclic shifting the string $t_1t_2\ldots t_m$ to the right, we get the string $t_mt_1\ldots t_{m-1}$.</p></div><div class="input-specification"><p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$)&nbsp;— the length of the string $s$.</p><p>The second line of each test case contains a single string $s$ of length $n$, consisting of lowercase English letters.</p><p>It is guaranteed that sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output a single integer — the minimum number of operations required to make $s$ sorted, or $-1$ if it's impossible.</p></div>

## Input

<p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$)&nbsp;— the length of the string $s$.</p><p>The second line of each test case contains a single string $s$ of length $n$, consisting of lowercase English letters.</p><p>It is guaranteed that sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output a single integer — the minimum number of operations required to make $s$ sorted, or $-1$ if it's impossible.</p>





```input1|2,3,6,7,10,11
6
5
aaabc
3
acb
3
bac
4
zbca
15
czddeneeeemigec
13
cdefmopqsvxzz
```




```output1
0
1
-1
2
6
0
```



## Note

<p>In the first test case, the string $s$ is already sorted, so we need no operations.</p><p>In the second test case, doing one operation, we will select <span class="tex-font-style-tt">cb</span> and cyclic shift it. The string $s$ is now <span class="tex-font-style-tt">abc</span> which is sorted.</p><p>In the third test case, $s$ cannot be sorted.</p><p>In the fourth test case we will perform the following operations:</p><ul><li> The lexicographically largest subsequence is <span class="tex-font-style-tt">zca</span>. Then $s$ becomes <span class="tex-font-style-tt">abzc</span>.</li><li> The lexicographically largest subsequence is <span class="tex-font-style-tt">zc</span>. Then $s$ becomes <span class="tex-font-style-tt">abcz</span>. The string becomes sorted.</li></ul><p>Thus, we need $2$ operations.</p>
