## Description

<div><p>You are given an array $a$ of $n$ elements. You can apply the following operation to it any number of times:</p><ul> <li> Select some subarray from $a$ of even size $2k$ that begins at position $l$ ($1\le l \le l+2\cdot{k}-1\le n$, $k \ge 1$) and for each $i$ between $0$ and $k-1$ (inclusive), assign the value $a_{l+k+i}$ to $a_{l+i}$. </li></ul><p>For example, if $a = [2, 1, 3, 4, 5, 3]$, then choose $l = 1$ and $k = 2$, applying this operation the array will become $a = [3, 4, 3, 4, 5, 3]$.</p><p>Find the minimum number of operations (possibly zero) needed to make all the elements of the array equal.</p></div><div class="input-specification"><p>The input consists of multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 2 \cdot 10^4$) — the number of test cases. Description of the test cases follows.</p><p>The first line of each test case contains an integer $n$ ($1 \leq n \leq 2 \cdot 10^5$) — the length of the array.</p><p>The second line of each test case consists of $n$ integers $a_1, a_2, \dots, a_n$ ($1 \leq a_i \leq n$) — the elements of the array $a$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>Print $t$ lines, each line containing the answer to the corresponding test case — the minimum number of operations needed to make equal all the elements of the array with the given operation.</p></div>

## Input

<p>The input consists of multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 2 \cdot 10^4$) — the number of test cases. Description of the test cases follows.</p><p>The first line of each test case contains an integer $n$ ($1 \leq n \leq 2 \cdot 10^5$) — the length of the array.</p><p>The second line of each test case consists of $n$ integers $a_1, a_2, \dots, a_n$ ($1 \leq a_i \leq n$) — the elements of the array $a$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>Print $t$ lines, each line containing the answer to the corresponding test case — the minimum number of operations needed to make equal all the elements of the array with the given operation.</p>





```input1
5
3
1 1 1
2
2 1
5
4 4 4 2 4
4
4 2 1 3
1
1
```




```output1
0
1
1
2
0
```



## Note

<p>In the first test, all elements are equal, therefore no operations are needed.</p><p>In the second test, you can apply one operation with $k=1$ and $l=1$, set $a_1 := a_2$, and the array becomes $[1, 1]$ with $1$ operation.</p><p>In the third test, you can apply one operation with $k=1$ and $l=4$, set $a_4 := a_5$, and the array becomes $[4, 4, 4, 4, 4]$.</p><p>In the fourth test, you can apply one operation with $k=1$ and $l=3$, set $a_3 := a_4$, and the array becomes $[4, 2, 3, 3]$, then you can apply another operation with $k=2$ and $l=1$, set $a_1 := a_3$, $a_2 := a_4$, and the array becomes $[3, 3, 3, 3]$.</p><p>In the fifth test, there is only one element, therefore no operations are needed.</p>
