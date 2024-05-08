## Description

<div><p>Today Alex was brought array $a_1, a_2, \dots, a_n$ of length $n$. He can apply as many operations as he wants (including zero operations) to change the array elements.</p><p>In $1$ operation Alex can choose any $l$ and $r$ such that $1 \leq l \leq r \leq n$, and multiply all elements of the array from $l$ to $r$ inclusive by $-1$. In other words, Alex can replace the subarray $[a_l, a_{l + 1}, \dots, a_r]$ by $[-a_l, -a_{l + 1}, \dots, -a_r]$ in $1$ operation.</p><p>For example, let $n = 5$, the array is $[1, -2, 0, 3, -1]$, $l = 2$ and $r = 4$, then after the operation the array will be $[1, 2, 0, -3, -1]$.</p><p>Alex is late for school, so you should help him find the maximum possible sum of numbers in the array, which can be obtained by making any number of operations, as well as the minimum number of operations that must be done for this.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \leq t \leq 10^4$)&nbsp;— number of test cases. Then the descriptions of the test cases follow.</p><p>The first line of each test case contains one integer $n$ ($1 \leq n \leq 2 \cdot 10^5$)&nbsp;— length of the array.</p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($-10^9 \leq a_i \leq 10^9$)&nbsp;— elements of the array.</p><p>It is guaranteed that the sum of $n$ for all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case output two space-separated numbers: the maximum possible sum of numbers in the array and the minimum number of operations to get this sum.</p><p>Pay attention that an answer may not fit in a standard integer type, so do not forget to use 64-bit integer type.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \leq t \leq 10^4$)&nbsp;— number of test cases. Then the descriptions of the test cases follow.</p><p>The first line of each test case contains one integer $n$ ($1 \leq n \leq 2 \cdot 10^5$)&nbsp;— length of the array.</p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($-10^9 \leq a_i \leq 10^9$)&nbsp;— elements of the array.</p><p>It is guaranteed that the sum of $n$ for all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case output two space-separated numbers: the maximum possible sum of numbers in the array and the minimum number of operations to get this sum.</p><p>Pay attention that an answer may not fit in a standard integer type, so do not forget to use 64-bit integer type.</p>





```input1|2,3,6,7,10,11
5
6
-1 7 -4 -2 5 -8
8
-1 0 0 -2 1 0 -3 0
5
2 -1 0 -3 -7
5
0 -17 0 1 0
4
-1 0 -2 -1
```




```output1
27 3
7 2
13 1
18 1
4 1
```



## Note

<p>Below, for each test case, only one of the possible shortest sequences of operations is provided among many. There are others that have the same length and lead to the maximum sum of elements.</p><p>In the first test case, Alex can make operations: $(1, 4)$, $(2, 2)$, $(6, 6)$.</p><p>In the second test case, to get the largest sum you need to make operations: $(1, 8)$, $(5, 6)$.</p><p>In the fourth test case, it is necessary to make only one operation: $(2, 3)$.</p>
