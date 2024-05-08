## Description

<div><p>You are given an array $a$ of length $n$, consisting of <span class="tex-font-style-bf">positive integers</span>. </p><p>You can perform the following operation on this array any number of times (possibly zero): </p><ul> <li> choose three integers $l$, $r$ and $x$ such that $1 \le l \le r \le n$, and multiply every $a_i$ such that $l \le i \le r$ by $x$. </li></ul><p>Note that you can choose <span class="tex-font-style-bf">any</span> integer as $x$, it doesn't have to be positive.</p><p>You have to calculate the minimum number of operations to make the array $a$ sorted in <span class="tex-font-style-bf">strictly ascending</span> order (i. e. the condition $a_1 &lt; a_2 &lt; \dots &lt; a_n$ must be satisfied).</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^4$) &nbsp;— the number of test cases.</p><p>The first line of each test case contains one integer $n$ ($1 \le n \le 2 \cdot 10^5$) &nbsp;— the length of the array $a$.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le 10^9$)&nbsp;— the array $a$.</p><p>Additional constraint on the input: the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, print one integer — the minimum number of operations required to make $a$ sorted in strictly ascending order.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^4$) &nbsp;— the number of test cases.</p><p>The first line of each test case contains one integer $n$ ($1 \le n \le 2 \cdot 10^5$) &nbsp;— the length of the array $a$.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le 10^9$)&nbsp;— the array $a$.</p><p>Additional constraint on the input: the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, print one integer — the minimum number of operations required to make $a$ sorted in strictly ascending order.</p>





```input1|2,3,6,7
3
5
1 1 2 2 2
6
5 4 3 2 5 1
3
1 2 3
```




```output1
3
2
0
```



## Note

<p>In the first test case, we can perform the operations as follows: </p><ul> <li> $l = 2$, $r = 4$, $x = 3$; </li><li> $l = 4$, $r = 4$, $x = 2$; </li><li> $l = 5$, $r = 5$, $x = 10$. </li></ul> After these operations, the array $a$ becomes $[1, 3, 6, 12, 20]$.<p>In the second test case, we can perform one operation as follows: </p><ul> <li> $l = 1$, $r = 4$, $x = -2$; </li><li> $l = 6$, $r = 6$, $x = 1337$. </li></ul> After these operations, the array $a$ becomes $[-10, -8, -6, -4, 5, 1337]$.<p>In the third test case, the array $a$ is already sorted.</p>
