## Description

<div><p>An array $a_1, a_2, \ldots, a_n$ is <span class="tex-font-style-it">good</span> if and only if for every subsegment $1 \leq l \leq r \leq n$, the following holds: $a_l + a_{l + 1} + \ldots + a_r = \frac{1}{2}(a_l + a_r) \cdot (r - l + 1)$. </p><p>You are given an array of integers $a_1, a_2, \ldots, a_n$. In one operation, you can replace any one element of this array with any real number. Find the minimum number of operations you need to make this array good.</p></div><div class="input-specification"><p>The first line of input contains one integer $t$ ($1 \leq t \leq 100$): the number of test cases.</p><p>Each of the next $t$ lines contains the description of a test case.</p><p>In the first line you are given one integer $n$ ($1 \leq n \leq 70$): the number of integers in the array.</p><p>The second line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($-100 \leq a_i \leq 100$): the initial array.</p></div><div class="output-specification"><p>For each test case, print one integer: the minimum number of elements that you need to replace to make the given array good.</p></div>

## Input

<p>The first line of input contains one integer $t$ ($1 \leq t \leq 100$): the number of test cases.</p><p>Each of the next $t$ lines contains the description of a test case.</p><p>In the first line you are given one integer $n$ ($1 \leq n \leq 70$): the number of integers in the array.</p><p>The second line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($-100 \leq a_i \leq 100$): the initial array.</p>

## Output

<p>For each test case, print one integer: the minimum number of elements that you need to replace to make the given array good.</p>





```input1
5
4
1 2 3 4
4
1 1 2 2
2
0 -1
6
3 -2 4 -1 -4 0
1
-100
```




```output1
0
2
0
3
0
```



## Note

<p>In the first test case, the array is good already.</p><p>In the second test case, one of the possible good arrays is $[1, 1, \underline{1}, \underline{1}]$ (replaced elements are underlined).</p><p>In the third test case, the array is good already.</p><p>In the fourth test case, one of the possible good arrays is $[\underline{-2.5}, -2, \underline{-1.5}, -1, \underline{-0.5}, 0]$.</p>
