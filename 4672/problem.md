## Description

<div><p>You are given an array of integers $a_1, a_2, \ldots, a_n$. You need to make it non-decreasing with the minimum number of operations. In one operation, you do the following:</p><ul><li> Choose an index $1 \leq i \leq n$,</li><li> Set $a_i = a_i \cdot 2$.</li></ul><p>An array $b_1, b_2, \ldots, b_n$ is non-decreasing if $b_i \leq b_{i+1}$ for all $1 \leq i &lt; n$.</p></div><div class="input-specification"><p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 10^4$) — the number of test cases. This is followed by their description.</p><p>The first line of each test case contains an integer $n$ ($1 \leq n \leq 10^5$) — the size of the array $a$.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \leq a_i \leq 10^9$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output the minimum number of operations needed to make the array non-decreasing.</p></div>

## Input

<p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 10^4$) — the number of test cases. This is followed by their description.</p><p>The first line of each test case contains an integer $n$ ($1 \leq n \leq 10^5$) — the size of the array $a$.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \leq a_i \leq 10^9$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output the minimum number of operations needed to make the array non-decreasing.</p>





```input1|2,3,6,7,10,11,14,15,18,19
9
1
1
2
2 1
3
3 2 1
4
7 1 5 3
5
11 2 15 7 10
6
1 8 2 16 8 16
2
624323799 708290323
12
2 1 1 3 3 11 12 22 45 777 777 1500
12
12 11 10 9 8 7 6 5 4 3 2 1
```




```output1
0
1
3
6
10
3
0
2
66
```



## Note

<p>No operations are needed in the first test case.</p><p>In the second test case, we need to choose $i = 2$, after which the array will be $[2, 2]$.</p><p>In the third test case, we can apply the following operations:</p><ul><li> Choose $i = 3$, after which the array will be $[3, 2, 2]$,</li><li> Choose $i = 3$, after which the array will be $[3, 2, 4]$,</li><li> Choose $i = 2$, after which the array will be $[3, 4, 4]$.</li></ul>
