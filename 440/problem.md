## Description

<div><p>Given a positive integer $n$, find the maximum size of an interval $[l, r]$ of positive integers such that, for every $i$ in the interval (i.e., $l \leq i \leq r$), $n$ is a multiple of $i$.</p><p>Given two integers $l\le r$, the size of the interval $[l, r]$ is $r-l+1$ (i.e., it coincides with the number of integers belonging to the interval).</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^4$) — the number of test cases.</p><p>The only line of the description of each test case contains one integer $n$ ($1 \leq n \leq 10^{18}$).</p></div><div class="output-specification"><p>For each test case, print a single integer: the maximum size of a valid interval.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^4$) — the number of test cases.</p><p>The only line of the description of each test case contains one integer $n$ ($1 \leq n \leq 10^{18}$).</p>

## Output

<p>For each test case, print a single integer: the maximum size of a valid interval.</p>





```input1|2,4,6,8,10
10
1
40
990990
4204474560
169958913706572972
365988220345828080
387701719537826430
620196883578129853
864802341280805662
1000000000000000000
```




```output1
1
2
3
6
4
22
3
1
2
2
```



## Note

<p>In the first test case, a valid interval with maximum size is $[1, 1]$ (it's valid because $n = 1$ is a multiple of $1$) and its size is $1$.</p><p>In the second test case, a valid interval with maximum size is $[4, 5]$ (it's valid because $n = 40$ is a multiple of $4$ and $5$) and its size is $2$.</p><p>In the third test case, a valid interval with maximum size is $[9, 11]$.</p><p>In the fourth test case, a valid interval with maximum size is $[8, 13]$.</p><p>In the seventh test case, a valid interval with maximum size is $[327869, 327871]$.</p>
