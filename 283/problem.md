## Description

<div><p><span class="tex-font-style-bf">This is the easy version of the problem. The only difference is that in this version $m = 1$.</span></p><p>You are given two arrays of integers $a_1, a_2, \ldots, a_n$ and $b_1, b_2, \ldots, b_n$. Before applying any operations, you can reorder the elements of each array as you wish. Then, in one operation, you will perform both of the following actions, if the arrays are not empty:</p><ul><li> Choose any element from array $a$ and remove it (all remaining elements are shifted to a new array $a$),</li><li> Choose any element from array $b$ and remove it (all remaining elements are shifted to a new array $b$).</li></ul><p>Let $k$ be the final size of both arrays. You need to find the minimum number of operations required to satisfy $a_i &lt; b_i$ for all $1 \leq i \leq k$.</p><p>This problem was too easy, so the problem author decided to make it more challenging. You are also given a positive integer $m$. Now, you need to find the sum of answers to the problem for $m$ pairs of arrays $(c[i], b)$, where $1 \leq i \leq m$. Array $c[i]$ is obtained from $a$ as follows:</p><ul><li> $c[i]_1 = i$,</li><li> $c[i]_j = a_j$, for $2 \leq j \leq n$.</li></ul></div><div class="input-specification"><p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 10^4$) - the number of sets of input data. This is followed by their description.</p><p>The first line of each test case contains two integers $n$ and $m$ ($2 \leq n \leq 10^5$, $m = 1$) - the size of arrays $a$ and $b$ and the constraints on the value of element $a_1$.</p><p>The second line of each test case contains $n - 1$ integers $a_2, \ldots, a_n$ ($1 \leq a_i \leq 10^9$).</p><p>The third line of each test case contains $n$ integers $b_1, b_2, \ldots, b_n$ ($1 \leq b_i \leq 10^9$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p></div><div class="output-specification"><p>For each test case, output the total number of minimum operations for all pairs of arrays $(c_i, b)$.</p></div>

## Input

<p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 10^4$) - the number of sets of input data. This is followed by their description.</p><p>The first line of each test case contains two integers $n$ and $m$ ($2 \leq n \leq 10^5$, $m = 1$) - the size of arrays $a$ and $b$ and the constraints on the value of element $a_1$.</p><p>The second line of each test case contains $n - 1$ integers $a_2, \ldots, a_n$ ($1 \leq a_i \leq 10^9$).</p><p>The third line of each test case contains $n$ integers $b_1, b_2, \ldots, b_n$ ($1 \leq b_i \leq 10^9$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p>

## Output

<p>For each test case, output the total number of minimum operations for all pairs of arrays $(c_i, b)$.</p>





```input1|2,3,4,8,9,10
4
2 1
1
3 2
4 1
5 1 5
3 8 3 3
8 1
4 3 3 2 2 1 1
1 1 1 1 3 3 3 3
9 1
9 2 8 3 7 4 6 5
1 2 3 2 1 4 5 6 5
```




```output1
0
1
4
4
```



## Note

<p>In the first test case for the pair of arrays $([1, 1], [3, 2])$, the answer is $0$. No operations or reordering of elements are needed.</p>
