## Description

<div><p><span class="tex-font-style-bf">The only difference between this problem and the hard version is the constraints on $t$ and $n$.</span></p><p>You are given an array $a$, consisting of $n$ distinct integers $a_1, a_2, \ldots, a_n$. </p><p>Define the <span class="tex-font-style-it">beauty</span> of an array $p_1, p_2, \ldots p_k$ as the minimum amount of time needed to sort this array using an arbitrary number of <span class="tex-font-style-it">range-sort</span> operations. In each range-sort operation, you will do the following: </p><ul> <li> Choose two integers $l$ and $r$ ($1 \le l &lt; r \le k$). </li><li> Sort the subarray $p_l, p_{l + 1}, \ldots, p_r$ in $r - l$ seconds. </li></ul><p>Please calculate the sum of beauty over all subarrays of array $a$.</p><p>A subarray of an array is defined as a sequence of consecutive elements of the array.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 5 \cdot 10^3$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 5 \cdot 10^3$)&nbsp;— the length of the array $a$.</p><p>The second line of each test case consists of $n$ integers $a_1,a_2,\ldots, a_n$ ($1\le a_i\le 10^9$). It is guaranteed that all elements of $a$ are pairwise distinct.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $5 \cdot 10^3$.</p></div><div class="output-specification"><p>For each test case, output the sum of beauty over all subarrays of array $a$.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 5 \cdot 10^3$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 5 \cdot 10^3$)&nbsp;— the length of the array $a$.</p><p>The second line of each test case consists of $n$ integers $a_1,a_2,\ldots, a_n$ ($1\le a_i\le 10^9$). It is guaranteed that all elements of $a$ are pairwise distinct.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $5 \cdot 10^3$.</p>

## Output

<p>For each test case, output the sum of beauty over all subarrays of array $a$.</p>





```input1|2,3,6,7,10,11
5
2
6 4
3
3 10 6
4
4 8 7 2
5
9 8 2 4 6
12
2 6 13 3 15 5 10 8 16 9 11 18
```




```output1
1
2
8
16
232
```



## Note

<p>In the first test case: </p><ul> <li> The subarray $[6]$ is already sorted, so its beauty is $0$. </li><li> The subarray $[4]$ is already sorted, so its beauty is $0$. </li><li> You can sort the subarray $[6, 4]$ in one operation by choosing $l = 1$ and $r = 2$. Its beauty is equal to $1$. </li></ul> The sum of beauty over all subarrays of the given array is equal to $0 + 0 + 1 = 1$.<p>In the second test case: </p><ul> <li> The subarray $[3]$ is already sorted, so its beauty is $0$. </li><li> The subarray $[10]$ is already sorted, so its beauty is $0$. </li><li> The subarray $[6]$ is already sorted, so its beauty is $0$. </li><li> The subarray $[3, 10]$ is already sorted, so its beauty is $0$. </li><li> You can sort the subarray $[10, 6]$ in one operation by choosing $l = 1$ and $r = 2$. Its beauty is equal to $2 - 1 = 1$. </li><li> You can sort the subarray $[3, 10, 6]$ in one operation by choosing $l = 2$ and $r = 3$. Its beauty is equal to $3 - 2 = 1$. </li></ul> The sum of beauty over all subarrays of the given array is equal to $0 + 0 + 0 + 0 + 1 + 1 = 2$.
