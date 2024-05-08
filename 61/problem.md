## Description

<div><p>You are given an array of numbers $a_1, a_2, \ldots, a_n$. Your task is to block some elements of the array in order to minimize its cost. Suppose you block the elements with indices $1 \leq b_1 &lt; b_2 &lt; \ldots &lt; b_m \leq n$. Then the cost of the array is calculated as the maximum of: </p><ul> <li> the sum of the blocked elements, i.e., $a_{b_1} + a_{b_2} + \ldots + a_{b_m}$. </li><li> the maximum sum of the segments into which the array is divided when the blocked elements are removed. That is, the maximum sum of the following ($m + 1$) subarrays: [$1, b_1 − 1$], [$b_1 + 1, b_2 − 1$], [$\ldots$], [$b_{m−1} + 1, b_m - 1$], [$b_m + 1, n$] (the sum of numbers in a subarray of the form [$x,x − 1$] is considered to be $0$). </li></ul><p>For example, if $n = 6$, the original array is [$1, 4, 5, 3, 3, 2$], and you block the elements at positions $2$ and $5$, then the cost of the array will be the maximum of the sum of the blocked elements ($4 + 3 = 7$) and the sums of the subarrays ($1$, $5 + 3 = 8$, $2$), which is $\max(7,1,8,2) = 8$. </p><p>You need to output the minimum cost of the array after blocking.</p></div><div class="input-specification"><p>The first line of the input contains a single integer $t$ ($1 \leq t \leq 30\,000$)&nbsp;— the number of queries.</p><p>Each test case consists of two lines. The first line contains an integer $n$ ($1 \leq n \leq 10^5$)&nbsp;— the length of the array $a$. The second line contains $n$ elements $a_1, a_2, \ldots, a_n$ ($1 \leq a_i \leq 10^9$)&nbsp;— the array $a$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p></div><div class="output-specification"><p>For each test case, output a single number&nbsp;— the minimum cost of blocking the array.</p></div>

## Input

<p>The first line of the input contains a single integer $t$ ($1 \leq t \leq 30\,000$)&nbsp;— the number of queries.</p><p>Each test case consists of two lines. The first line contains an integer $n$ ($1 \leq n \leq 10^5$)&nbsp;— the length of the array $a$. The second line contains $n$ elements $a_1, a_2, \ldots, a_n$ ($1 \leq a_i \leq 10^9$)&nbsp;— the array $a$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p>

## Output

<p>For each test case, output a single number&nbsp;— the minimum cost of blocking the array.</p>





```input1|2,3,6,7
3
6
1 4 5 3 3 2
5
1 2 3 4 5
6
4 1 6 3 10 7
```




```output1
7
5
11
```



## Note

<p>The first test case matches with the array from the statement. To obtain a cost of $7$, you need to block the elements at positions $2$ and $4$. In this case, the cost of the array is calculated as the maximum of:</p><ul> <li> the sum of the blocked elements, which is $a_2 + a_4 = 7$. </li><li> the maximum sum of the segments into which the array is divided when the blocked elements are removed, i.e., the maximum of $a_1$, $a_3$, $a_5 + a_6 = \max(1,5,5) = 5$. </li></ul><p>So the cost is $\max(7,5) = 7$. </p><p>In the second test case, you can block the elements at positions $1$ and $4$.</p><p>In the third test case, to obtain the answer $11$, you can block the elements at positions $2$ and $5$. There are other ways to get this answer, for example, blocking positions $4$ and $6$.</p>
