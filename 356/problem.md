## Description

<div><p>You are given three non-negative integers $n$, $k$, and $x$. Find the maximum possible sum of elements in an array consisting of non-negative integers, which has $n$ elements, its MEX is equal to $k$, and all its elements do not exceed $x$. If such an array does not exist, output $-1$.</p><p>The MEX (minimum excluded) of an array is the smallest non-negative integer that does not belong to the array. For instance:</p><ul> <li> The MEX of $[2,2,1]$ is $0$, because $0$ does not belong to the array. </li><li> The MEX of $[3,1,0,1]$ is $2$, because $0$ and $1$ belong to the array, but $2$ does not. </li><li> The MEX of $[0,3,1,2]$ is $4$, because $0$, $1$, $2$ and $3$ belong to the array, but $4$ does not. </li></ul></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \leq t \leq 1000$) — the number of test cases. Then follows the description of the test cases.</p><p>The only line of each test case contains three integers $n$, $k$, and $x$ ($1 \leq n, k, x \leq 200$).</p></div><div class="output-specification"><p>For each test case, output a single number — the maximum sum of elements in a valid array, or $-1$, if such an array does not exist.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \leq t \leq 1000$) — the number of test cases. Then follows the description of the test cases.</p><p>The only line of each test case contains three integers $n$, $k$, and $x$ ($1 \leq n, k, x \leq 200$).</p>

## Output

<p>For each test case, output a single number — the maximum sum of elements in a valid array, or $-1$, if such an array does not exist.</p>





```input1|2,4,6,8,10
9
5 3 3
4 7 5
4 2 28
12 10 6
57 51 122
200 1 200
2 2 1
3 2 1
4 7 10
```




```output1
7
-1
57
-1
2007
39800
1
2
-1
```



## Note

<p>In the first test case, the maximum sum is $7$, and one of the valid arrays is $[0, 1, 2, 2, 2]$.</p><p>In the second test case, there are no valid arrays of length $n$.</p><p>In the third test case, the maximum sum is $57$, and one of the valid arrays is $[0, 1, 28, 28]$.</p>
