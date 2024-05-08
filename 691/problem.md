## Description

<div><p>For an array $a = [a_1, a_2, \dots, a_n]$, let's denote its <span class="tex-font-style-it">subarray</span> $a[l, r]$ as the array $[a_l, a_{l+1}, \dots, a_r]$.</p><p>For example, the array $a = [1, -3, 1]$ has $6$ non-empty subarrays:</p><ul> <li> $a[1,1] = [1]$; </li><li> $a[1,2] = [1,-3]$; </li><li> $a[1,3] = [1,-3,1]$; </li><li> $a[2,2] = [-3]$; </li><li> $a[2,3] = [-3,1]$; </li><li> $a[3,3] = [1]$. </li></ul><p>You are given two integers $n$ and $k$. Construct an array $a$ consisting of $n$ integers such that:</p><ul> <li> all elements of $a$ are from $-1000$ to $1000$; </li><li> $a$ has exactly $k$ subarrays with positive sums; </li><li> the rest $\dfrac{(n+1) \cdot n}{2}-k$ subarrays of $a$ have negative sums. </li></ul></div><div class="input-specification"><p>The first line contains one integer $t$ ($1 \le t \le 5000$) — the number of test cases.</p><p>Each test case consists of one line containing two integers $n$ and $k$ ($2 \le n \le 30$; $0 \le k \le \dfrac{(n+1) \cdot n}{2}$).</p></div><div class="output-specification"><p>For each test case, print $n$ integers — the elements of the array meeting the constraints. It can be shown that the answer always exists. If there are multiple answers, print any of them.</p></div>

## Input

<p>The first line contains one integer $t$ ($1 \le t \le 5000$) — the number of test cases.</p><p>Each test case consists of one line containing two integers $n$ and $k$ ($2 \le n \le 30$; $0 \le k \le \dfrac{(n+1) \cdot n}{2}$).</p>

## Output

<p>For each test case, print $n$ integers — the elements of the array meeting the constraints. It can be shown that the answer always exists. If there are multiple answers, print any of them.</p>





```input1|2,4
4
3 2
2 0
2 2
4 6
```




```output1
1 -3 1
-13 -42
-13 42
-3 -4 10 -2
```


