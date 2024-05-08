## Description

<div><p>Kristina has a string $s$ of length $n$, consisting only of lowercase and uppercase Latin letters. For each pair of lowercase letter and its matching uppercase letter, Kristina can get $1$ burl. However, pairs of characters cannot overlap, so each character can only be in one pair.</p><p>For example, if she has the string $s$ = "aAaaBACacbE", she can get a burl for the following character pairs: </p><ul> <li> $s_1$ = "a" and $s_2$ = "A" </li><li> $s_4$ = "a" and $s_6$ = "A" </li><li> $s_5$ = "B" and $s_{10}$ = "b" </li><li> $s_7$= "C" and $s_9$ = "c" </li></ul><p>Kristina wants to get more burles for her string, so she is going to perform no more than $k$ operations on it. In one operation, she can:</p><ul> <li> either select the lowercase character $s_i$ ($1 \le i \le n$) and make it uppercase. </li><li> or select uppercase character $s_i$ ($1 \le i \le n$) and make it lowercase. </li></ul><p>For example, when $k$ = 2 and $s$ = "aAaaBACacbE" it can perform one operation: choose $s_3$ = "a" and make it uppercase. Then she will get another pair of $s_3$ = "A" and $s_8$ = "a"</p><p>Find <span class="tex-font-style-bf">maximum</span> number of burles Kristina can get for her string.</p></div><div class="input-specification"><p>The first line of input data contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ ($1 \le n \le 2 \cdot 10^5$) and $k$ ($0 \le k \le n$) — the number of characters in the string and the maximum number of operations that can be performed on it.</p><p>The second line of each test case contains a string $s$ of length $n$, consisting only of lowercase and uppercase Latin letters.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, print exactly one integer on a separate line: the maximum number of burles that Kristina can get for her string $s$.</p></div>

## Input

<p>The first line of input data contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ ($1 \le n \le 2 \cdot 10^5$) and $k$ ($0 \le k \le n$) — the number of characters in the string and the maximum number of operations that can be performed on it.</p><p>The second line of each test case contains a string $s$ of length $n$, consisting only of lowercase and uppercase Latin letters.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, print exactly one integer on a separate line: the maximum number of burles that Kristina can get for her string $s$.</p>





```input1|2,3,6,7,10,11
5
11 2
aAaaBACacbE
2 2
ab
4 1
aaBB
6 0
abBAcC
5 3
cbccb
```




```output1
5
0
1
3
2
```



## Note

<p>The first test case is explained in the problem statement.</p><p>In the second test case, it is not possible to get any pair by performing any number of operations.</p>
