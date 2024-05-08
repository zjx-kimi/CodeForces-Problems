## Description

<div><p>You are given an array $a$ of $n$ integers, where all elements $a_i$ lie in the range $[1, k]$. How many different arrays $b$ of $m$ integers, where all elements $b_i$ lie in the range $[1, k]$, contain $a$ as a subsequence? Two arrays are considered different if they differ in at least one position.</p><p>A sequence $x$ is a subsequence of a sequence $y$ if $x$ can be obtained from $y$ by the deletion of several (possibly, zero or all) elements.</p><p>Since the answer may be large, print it modulo $10^9 + 7$.</p></div><div class="input-specification"><p>The first line of the input contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains three integers $n$, $m$, $k$ ($1 \le n \le 2\cdot 10^5$, $n \le m \le 10^9$, $1 \le k \le 10^9$)&nbsp;— the size of $a$, the size of $b$, and the maximum value allowed in the arrays, respectively.</p><p>The next line of each test case contains $n$ integers $a_1, a_2, \ldots a_n$ ($1\le a_i \le k$)&nbsp;— the elements of the array $a$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2\cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output a single integer&nbsp;— the number of suitable arrays $b$, modulo $10^9+7$.</p></div>

## Input

<p>The first line of the input contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains three integers $n$, $m$, $k$ ($1 \le n \le 2\cdot 10^5$, $n \le m \le 10^9$, $1 \le k \le 10^9$)&nbsp;— the size of $a$, the size of $b$, and the maximum value allowed in the arrays, respectively.</p><p>The next line of each test case contains $n$ integers $a_1, a_2, \ldots a_n$ ($1\le a_i \le k$)&nbsp;— the elements of the array $a$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2\cdot 10^5$.</p>

## Output

<p>For each test case, output a single integer&nbsp;— the number of suitable arrays $b$, modulo $10^9+7$.</p>





```input1|2,3,6,7,10,11,14,15
7
1 1000000 1
1
3 4 3
1 2 2
5 7 8
1 2 3 4 1
6 6 18
18 2 2 5 2 16
1 10 2
1
8 10 1234567
1 1 2 1 2 2 2 1
5 1000000000 1000000000
525785549 816356460 108064697 194447117 725595511
```




```output1
1
9
1079
1
1023
906241579
232432822
```



## Note

<p>For the first example, since $k=1$, there is only one array of size $m$ consisting of the integers $[1, k]$. This array ($[1, 1, \ldots, 1]$) contains the original array as a subsequence, so the answer is 1.</p><p>For the second example, the $9$ arrays are $[1, 1, 2, 2]$, $[1, 2, 1, 2]$, $[1, 2, 2, 1]$, $[1, 2, 2, 2]$, $[1, 2, 2, 3]$, $[1, 2, 3, 2]$, $[1, 3, 2, 2]$, $[2, 1, 2, 2]$, $[3, 1, 2, 2]$.</p><p>For the fourth example, since $m=n$, the only array of size $m$ that contains $a$ as a subsequence is $a$ itself.</p>
