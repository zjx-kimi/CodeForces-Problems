## Description

<div><p>Let's call an array $a$ of $n$ non-negative integers <span class="tex-font-style-it">fancy</span> if the following conditions hold: </p><ul> <li> at least one from the numbers $x$, $x + 1$, ..., $x+k-1$ appears in the array; </li><li> consecutive elements of the array differ by at most $k$ (i.e. $|a_i-a_{i-1}| \le k$ for each $i \in [2, n]$). </li></ul><p>You are given $n$, $x$ and $k$. Your task is to calculate the number of <span class="tex-font-style-it">fancy</span> arrays of length $n$. Since the answer can be large, print it modulo $10^9+7$.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 50$)&nbsp;— the number of test cases.</p><p>The only line of each test case contains three integers $n$, $x$ and $k$ ($1 \le n, k \le 10^9$; $0 \le x \le 40$).</p></div><div class="output-specification"><p>For each test case, print a single integer&nbsp;— the number of <span class="tex-font-style-it">fancy</span> arrays of length $n$, taken modulo $10^9+7$.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 50$)&nbsp;— the number of test cases.</p><p>The only line of each test case contains three integers $n$, $x$ and $k$ ($1 \le n, k \le 10^9$; $0 \le x \le 40$).</p>

## Output

<p>For each test case, print a single integer&nbsp;— the number of <span class="tex-font-style-it">fancy</span> arrays of length $n$, taken modulo $10^9+7$.</p>





```input1|2,4
4
3 0 1
1 4 25
4 7 2
1000000000 40 1000000000
```




```output1
9
25
582
514035484
```



## Note

<p>In the first test case of the example, the following arrays are fancy:</p><ul> <li> $[0, 0, 0]$; </li><li> $[0, 0, 1]$; </li><li> $[0, 1, 0]$; </li><li> $[0, 1, 1]$; </li><li> $[0, 1, 2]$; </li><li> $[1, 0, 0]$; </li><li> $[1, 0, 1]$; </li><li> $[1, 1, 0]$; </li><li> $[2, 1, 0]$. </li></ul>
