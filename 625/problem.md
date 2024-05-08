## Description

<div><p>A permutation is a sequence $n$ integers, where each integer from $1$ to $n$ appears exactly once. For example, $[1]$, $[3,5,2,1,4]$, $[1,3,2]$ are permutations, while $[2,3,2]$, $[4,3,1]$, $[0]$ are not.</p><p>Given a permutation $a$, we construct an array $b$, where $b_i = (a_1 + a_2 +~\dots~+ a_i) \bmod n$.</p><p>A permutation of numbers $[a_1, a_2, \dots, a_n]$ is called a <span class="tex-font-style-it">super-permutation</span> if $[b_1 + 1, b_2 + 1, \dots, b_n + 1]$ is also a permutation of length $n$.</p><p>Grisha became interested whether a <span class="tex-font-style-it">super-permutation</span> of length $n$ exists. Help him solve this non-trivial problem. Output any <span class="tex-font-style-it">super-permutation</span> of length $n$, if it exists. Otherwise, output $-1$.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>Each test case consists of a single line containing one integer $n$ ($1 \le n \le 2 \cdot 10^5$)&nbsp;— the length of the desired permutation.</p><p>The sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output in a separate line:</p><ul> <li> $n$ integers&nbsp;— a <span class="tex-font-style-it">super-permutation</span> of length $n$, if it exists. </li><li> $-1$, otherwise. </li></ul><p>If there are several suitable permutations, output any of them.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>Each test case consists of a single line containing one integer $n$ ($1 \le n \le 2 \cdot 10^5$)&nbsp;— the length of the desired permutation.</p><p>The sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output in a separate line:</p><ul> <li> $n$ integers&nbsp;— a <span class="tex-font-style-it">super-permutation</span> of length $n$, if it exists. </li><li> $-1$, otherwise. </li></ul><p>If there are several suitable permutations, output any of them.</p>





```input1|2,4
4
1
2
3
6
```




```output1
1
2 1
-1
6 5 2 3 4 1
```


