## Description

<div><p>Given an array $a$ of $n$ positive integers. You need to perform the following operation <span class="tex-font-style-bf">exactly</span> once:</p><ul><li> Choose $2$ integers $l$ and $r$ ($1 \le l \le r \le n$) and replace the subarray $a[l \ldots r]$ with the single element: the product of all elements in the subarray $(a_l \cdot \ldots \cdot a_r)$.</li></ul><p>For example, if an operation with parameters $l = 2, r = 4$ is applied to the array $[5, 4, 3, 2, 1]$, the array will turn into $[5, 24, 1]$.</p><p>Your task is to maximize the sum of the array after applying this operation. Find the optimal subarray to apply this operation.</p></div><div class="input-specification"><p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. This is followed by the description of the test cases.</p><p>The first line of each test case contains a single number $n$ ($1 \le n \le 2 \cdot 10^5$)&nbsp;— the length of the array $a$.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le 10^9$).</p><p>It is guaranteed that the sum of the values of $n$ for all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output $2$ integers $l$ and $r$ ($1 \le l \le r \le n$)&nbsp;— the boundaries of the subarray to be replaced with the product.</p><p>If there are multiple solutions, output any of them.</p></div>

## Input

<p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. This is followed by the description of the test cases.</p><p>The first line of each test case contains a single number $n$ ($1 \le n \le 2 \cdot 10^5$)&nbsp;— the length of the array $a$.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le 10^9$).</p><p>It is guaranteed that the sum of the values of $n$ for all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output $2$ integers $l$ and $r$ ($1 \le l \le r \le n$)&nbsp;— the boundaries of the subarray to be replaced with the product.</p><p>If there are multiple solutions, output any of them.</p>





```input1|2,3,6,7,10,11,14,15,18,19
9
4
1 3 1 3
4
1 1 2 3
5
1 1 1 1 1
5
10 1 10 1 10
1
1
2
2 2
3
2 1 2
4
2 1 1 3
6
2 1 2 1 1 3
```




```output1
2 4
3 4
1 1
1 5
1 1
1 2
2 2
4 4
1 6
```



## Note

<p>In the first test case, after applying the operation with parameters $l = 2, r = 4$, the array $[1, 3, 1, 3]$ turns into $[1, 9]$, with a sum equal to $10$. It is easy to see that by replacing any other segment with a product, the sum will be less than $10$.</p><p>In the second test case, after applying the operation with parameters $l = 3, r = 4$, the array $[1, 1, 2, 3]$ turns into $[1, 1, 6]$, with a sum equal to $8$. It is easy to see that by replacing any other segment with a product, the sum will be less than $8$.</p><p>In the third test case, it will be optimal to choose any operation with $l = r$, then the sum of the array will remain $5$, and when applying any other operation, the sum of the array will decrease.</p>
