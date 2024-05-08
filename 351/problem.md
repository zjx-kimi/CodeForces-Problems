## Description

<div><p>You are given positive integers $n$ and $k$. For each number from $1$ to $n$, we write its representation in the number system with base $k$ (without leading zeros) and then sort the resulting array in lexicographic order as strings. In the sorted array, we number the elements from $1$ to $n$ (i.e., indexing starts from $1$). Find the number of values $i$ such that the representation of number $i$ is at the $i$-th position in the sorted array of representations.</p><p>Examples of representations: $1$ in any number system is equal to $1$, $7$ with $k = 3$ is written as $21$, and $81$ with $k = 9$ is written as $100$.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \leq t \leq 10^3$) — the number of test cases. This is followed by a description of the test cases.</p><p>The only line of each test case contains integers $n$ and $k$ ($1 \leq n \leq 10^{18}$, $2 \leq k \leq 10^{18}$).</p></div><div class="output-specification"><p>For each test case, output a single integer — the number of values $1 \leq i \leq n$ such that the representation of number $i$ in the number system with base $k$ is at the $i$-th position after sorting.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \leq t \leq 10^3$) — the number of test cases. This is followed by a description of the test cases.</p><p>The only line of each test case contains integers $n$ and $k$ ($1 \leq n \leq 10^{18}$, $2 \leq k \leq 10^{18}$).</p>

## Output

<p>For each test case, output a single integer — the number of values $1 \leq i \leq n$ such that the representation of number $i$ in the number system with base $k$ is at the $i$-th position after sorting.</p>





```input1|2,4,6,8
8
2 2
4 2
6 4
33 2
532 13
780011804570805480 3788
366364720306464627 4702032149561577
293940402103595405 2
```




```output1
2
2
1
3
1
3789
1
7
```



## Note

<p>In the first test case, for numbers $1$ and $2$, their representations are at positions $1$ and $2$ respectively.</p><p>In the second test case, the sorted array is $[1_2 = 1, 10_2 = 2, 100_2 = 4, 11_2 = 3]$, and only the representations of numbers $1$ and $2$ are at the required positions.</p><p>In the third test case, the sorted array is $[1_4 = 1, 10_4 = 4, 11_4 = 5, 12_4 = 6, 2_4 = 2, 3_4 = 3]$, and only the number $1$ is at its position.</p>
