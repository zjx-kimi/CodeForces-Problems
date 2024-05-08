## Description

<div><p>Given an array $a$ of $n$ elements, find the maximum value of the expression:</p><p>$$|a_i - a_j| + |a_j - a_k| + |a_k - a_l| + |a_l - a_i|$$</p><p>where $i$, $j$, $k$, and $l$ are four <span class="tex-font-style-bf">distinct</span> indices of the array $a$, with $1 \le i, j, k, l \le n$.</p><p>Here $|x|$ denotes the absolute value of $x$.</p></div><div class="input-specification"><p>The first line contains one integer $t$ ($1 \le t \le 500$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($4 \le n \le 100$)&nbsp;— the length of the given array.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($-10^6 \le a_i \le 10^6$).</p></div><div class="output-specification"><p>For each test case, print a single integer&nbsp;— the maximum value.</p></div>

## Input

<p>The first line contains one integer $t$ ($1 \le t \le 500$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($4 \le n \le 100$)&nbsp;— the length of the given array.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($-10^6 \le a_i \le 10^6$).</p>

## Output

<p>For each test case, print a single integer&nbsp;— the maximum value.</p>





```input1|2,3,6,7,10,11
5
4
1 1 1 1
5
1 1 2 2 3
8
5 1 3 2 -3 -1 10 3
4
3 3 1 1
4
1 2 2 -1
```




```output1
0
6
38
8
8
```



## Note

<p>In the first test case, for any selection of $i$, $j$, $k$, $l$, the answer will be $0$. For example, $|a_1 - a_2| + |a_2 - a_3| + |a_3 - a_4| + |a_4 - a_1| = |1 - 1| + |1 - 1| + |1 - 1| + |1 - 1| = 0 + 0 + 0 + 0 = 0$.</p><p>In the second test case, for $i = 1$, $j = 3$, $k = 2$, and $l = 5$, the answer will be $6$. $|a_1 - a_3| + |a_3 - a_2| + |a_2 - a_5| + |a_5 - a_1| = |1 - 2| + |2 - 1| + |1 - 3| + |3 - 1| = 1 + 1 + 2 + 2 = 6$.</p>
