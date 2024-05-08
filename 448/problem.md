## Description

<div><p>Ntarsis has received two integers $n$ and $k$ for his birthday. He wonders how many fibonacci-like sequences of length $k$ can be formed with <span class="tex-font-style-bf">$n$ as the $k$-th element</span> of the sequence. </p><p>A sequence of <span class="tex-font-style-bf">non-decreasing non-negative</span> integers is considered fibonacci-like if $f_i = f_{i-1} + f_{i-2}$ for all $i &gt; 2$, where $f_i$ denotes the $i$-th element in the sequence. Note that $f_1$ and $f_2$ can be arbitrary.</p><p>For example, sequences such as $[4,5,9,14]$ and $[0,1,1]$ are considered fibonacci-like sequences, while $[0,0,0,1,1]$, $[1, 2, 1, 3]$, and $[-1,-1,-2]$ are not: the first two do not always satisfy $f_i = f_{i-1} + f_{i-2}$, the latter does not satisfy that the elements are non-negative.</p><p>Impress Ntarsis by helping him with this task.</p></div><div class="input-specification"><p>The first line contains an integer $t$ ($1 \leq t \leq 2 \cdot 10^5$), the number of test cases. The description of each test case is as follows.</p><p>Each test case contains two integers, $n$ and $k$ ($1 \leq n \leq 2 \cdot 10^5$, $3 \leq k \leq 10^9$).</p><p>It is guaranteed the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case output an integer, the number of fibonacci-like sequences of length $k$ such that the $k$-th element in the sequence is $n$. That is, output the number of sequences $f$ of length $k$ so $f$ is a fibonacci-like sequence and $f_k = n$. It can be shown this number is finite.</p></div>

## Input

<p>The first line contains an integer $t$ ($1 \leq t \leq 2 \cdot 10^5$), the number of test cases. The description of each test case is as follows.</p><p>Each test case contains two integers, $n$ and $k$ ($1 \leq n \leq 2 \cdot 10^5$, $3 \leq k \leq 10^9$).</p><p>It is guaranteed the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case output an integer, the number of fibonacci-like sequences of length $k$ such that the $k$-th element in the sequence is $n$. That is, output the number of sequences $f$ of length $k$ so $f$ is a fibonacci-like sequence and $f_k = n$. It can be shown this number is finite.</p>





```input1|2,4,6,8
8
22 4
3 9
55 11
42069 6
69420 4
69 1434
1 3
1 4
```




```output1
4
0
1
1052
11571
0
1
0
```



## Note

<p>There are $4$ valid fibonacci-like sequences for $n = 22$, $k = 4$:</p><ul> <li> $[6,8,14,22]$, </li><li> $[4,9,13,22]$, </li><li> $[2,10,12,22]$, </li><li> $[0,11,11,22]$. </li></ul><p>For $n = 3$, $k = 9$, it can be shown that there are no fibonacci-like sequences satisfying the given conditions.</p><p>For $n = 55$, $k = 11$, $[0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55]$ is the only fibonacci-like sequence.</p>
