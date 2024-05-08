## Description

<div><p>You are given a permutation $p$ of size $n$. You want to minimize the number of subarrays of $p$ that are permutations. In order to do so, you must perform the following operation <span class="tex-font-style-bf">exactly</span> once:</p><ul> <li> Select integers $i$, $j$, where $1 \le i, j \le n$, then </li><li> Swap $p_i$ and $p_j$. </li></ul><p>For example, if $p = [5, 1, 4, 2, 3]$ and we choose $i = 2$, $j = 3$, the resulting array will be $[5, 4, 1, 2, 3]$. If instead we choose $i = j = 5$, the resulting array will be $[5, 1, 4, 2, 3]$.</p><p>Which choice of $i$ and $j$ will minimize the number of subarrays that are permutations?</p><p>A permutation of length $n$ is an array consisting of $n$ distinct integers from $1$ to $n$ in arbitrary order. For example, $[2,3,1,5,4]$ is a permutation, but $[1,2,2]$ is not a permutation ($2$ appears twice in the array), and $[1,3,4]$ is also not a permutation ($n=3$ but there is $4$ in the array).</p><p>An array $a$ is a subarray of an array $b$ if $a$ can be obtained from $b$ by the deletion of several (possibly, zero or all) elements from the beginning and several (possibly, zero or all) elements from the end.</p></div><div class="input-specification"><p>The first line of the input contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($3 \le n \le 2\cdot 10^5$)&nbsp;— the size of the permutation.</p><p>The next line of each test case contains $n$ integers $p_1, p_2, \ldots p_n$ ($1 \le p_i \le n$, all $p_i$ are distinct)&nbsp;— the elements of the permutation $p$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2\cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output two integers $i$ and $j$ ($1 \le i, j \le n$) &nbsp;— the indices to swap in $p$.</p><p>If there are multiple solutions, print any of them.</p></div>

## Input

<p>The first line of the input contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($3 \le n \le 2\cdot 10^5$)&nbsp;— the size of the permutation.</p><p>The next line of each test case contains $n$ integers $p_1, p_2, \ldots p_n$ ($1 \le p_i \le n$, all $p_i$ are distinct)&nbsp;— the elements of the permutation $p$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2\cdot 10^5$.</p>

## Output

<p>For each test case, output two integers $i$ and $j$ ($1 \le i, j \le n$) &nbsp;— the indices to swap in $p$.</p><p>If there are multiple solutions, print any of them.</p>





```input1|2,3,6,7,10,11,14,15
8
3
1 2 3
3
1 3 2
5
1 3 2 5 4
6
4 5 6 1 2 3
9
8 7 6 3 2 1 4 5 9
10
7 10 5 1 9 8 3 2 6 4
10
8 5 10 9 2 1 3 4 6 7
10
2 3 5 7 10 1 8 6 4 9
```




```output1
2 3
1 1
5 2
1 4
9 5
8 8
6 10
5 4
```



## Note

<p>For the first test case, there are four possible arrays after the swap: </p><ul> <li> If we swap $p_1$ and $p_2$, we get the array $[2, 1, 3]$, which has 3 subarrays that are permutations ($[1]$, $[2, 1]$, $[2, 1, 3]$). </li><li> If we swap $p_1$ and $p_3$, we get the array $[3, 2, 1]$, which has 3 subarrays that are permutations ($[1]$, $[2, 1]$, $[3, 2, 1]$). </li><li> If we swap $p_2$ and $p_3$, we get the array $[1, 3, 2]$, which has 2 subarrays that are permutations ($[1]$, $[1, 3, 2]$). </li><li> If we swap any element with itself, we get the array $[1, 2, 3]$, which has 3 subarrays that are permutations ($[1]$, $[1, 2]$, $[1, 2, 3]$). </li></ul> So the best swap to make is positions $2$ and $3$.<p>For the third sample case, after we swap elements at positions $2$ and $5$, the resulting array is $[1, 4, 2, 5, 3]$. The only subarrays that are permutations are $[1]$ and $[1, 4, 2, 5, 3]$. We can show that this is minimal.</p>
