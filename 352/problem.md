## Description

<div><p>You are given an array of integers $a$ of size $n$. You can choose a set of non-overlapping subarrays of the given array (note that some elements may be not included in any subarray, this is allowed). For each selected subarray, calculate the MEX of its elements, and then calculate the <a href="https://en.wikipedia.org/wiki/Bitwise_operation#XOR">bitwise XOR</a> of all the obtained MEX values. What is the maximum bitwise XOR that can be obtained?</p><p>The MEX (minimum excluded) of an array is the smallest non-negative integer that does not belong to the array. For instance: </p><ul> <li> The MEX of $[2,2,1]$ is $0$, because $0$ does not belong to the array. </li><li> The MEX of $[3,1,0,1]$ is $2$, because $0$ and $1$ belong to the array, but $2$ does not. </li><li> The MEX of $[0,3,1,2]$ is $4$, because $0$, $1$, $2$ and $3$ belong to the array, but $4$ does not. </li></ul></div><div class="input-specification"><p>The first line contains an integer $t$ ($1 \leq t \leq 5000$) — the number of test cases. This is followed by the description of the test cases.</p><p>The first line of each test case contains an integer $n$ ($1 \leq n \leq 5000$) — the size of the array $a$.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($0 \leq a_i \leq n$) — the array $a$.</p><p>It is guaranteed that the sum of all $n$ values across all test cases does not exceed $5000$.</p></div><div class="output-specification"><p>For each test case, output a single number — the maximum possible XOR of the MEX values of the selected subarrays.</p></div>

## Input

<p>The first line contains an integer $t$ ($1 \leq t \leq 5000$) — the number of test cases. This is followed by the description of the test cases.</p><p>The first line of each test case contains an integer $n$ ($1 \leq n \leq 5000$) — the size of the array $a$.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($0 \leq a_i \leq n$) — the array $a$.</p><p>It is guaranteed that the sum of all $n$ values across all test cases does not exceed $5000$.</p>

## Output

<p>For each test case, output a single number — the maximum possible XOR of the MEX values of the selected subarrays.</p>





```input1|2,3,6,7
4
2
1 0
10
1 2 0 7 1 2 0 2 4 3
10
2 1 0 7 1 2 0 2 4 3
3
1 2 1
```




```output1
2
6
7
0
```



## Note

<p>In the first test case, the maximum XOR is $2$ if we take the entire array, $\operatorname{MEX}([1, 0]) = 2$.</p><p>In the second test case, the maximum XOR is $6$ if we partition the array into segments $[1, 2, 0]$ and $[7, 1, 2, 0, 2, 4, 3]$: </p><ul> <li> $\operatorname{MEX}([1, 2, 0]) = 3$, </li><li> $\operatorname{MEX}([7, 1, 2, 0, 2, 4, 3]) = 5$, </li></ul> therefore, the XOR is $5 \oplus 3=6$.<p>In the third test case, the maximum XOR is $7$ if we partition the array into segments $[1, 0]$ and $[7, 1, 2, 0, 2, 4, 3]$: </p><ul> <li> $\operatorname{MEX}([1, 0]) = 2$, </li><li> $\operatorname{MEX}([7, 1, 2, 0, 2, 4, 3]) = 5$, </li></ul> therefore, the XOR is $5 \oplus 2 = 7$.
