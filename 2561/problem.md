## Description

<div><p>You are given an array $a$ of length $n$, and an integer $x$. You can perform the following operation as many times as you would like (possibly zero): replace two adjacent elements of the array by their sum. For example, if the initial array was $[3, 6, 9]$, in a single operation one can replace the last two elements by their sum, yielding an array $[3, 15]$, or replace the first two elements to get an array $[9, 9]$. Note that the size of the array decreases after each operation.</p><p>The <span class="tex-font-style-it">beauty</span> of an array $b=[b_1, \ldots, b_k]$ is defined as $\sum_{i=1}^k \left\lceil \frac{b_i}{x} \right\rceil$, which means that we divide each element by $x$, round it up to the nearest integer, and sum up the resulting values. For example, if $x = 3$, and the array is $[4, 11, 6]$, the beauty of the array is equal to $\left\lceil \frac{4}{3} \right\rceil + \left\lceil \frac{11}{3} \right\rceil + \left\lceil \frac{6}{3} \right\rceil = 2 + 4 + 2 = 8$.</p><p>Please determine the minimum and the maximum beauty you can get by performing some operations on the original array.</p></div><div class="input-specification"><p>The first input line contains a single integer $t$&nbsp;— the number of test cases ($1 \le t \le 1000$).</p><p>The first line of each test case contains two integers $n$ and $x$ ($1 \leq n \leq 10^5$, $1 \leq x \leq 10^9$).</p><p>The next line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \leq a_i \leq 10^9$), the elements of the array $a$. </p><p>It is guaranteed that the sum of values of $n$ over all test cases does not exceed $10^5$.</p></div><div class="output-specification"><p>For each test case output two integers&nbsp;— the minimal and the maximal possible beauty.</p></div>

## Input

<p>The first input line contains a single integer $t$&nbsp;— the number of test cases ($1 \le t \le 1000$).</p><p>The first line of each test case contains two integers $n$ and $x$ ($1 \leq n \leq 10^5$, $1 \leq x \leq 10^9$).</p><p>The next line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \leq a_i \leq 10^9$), the elements of the array $a$. </p><p>It is guaranteed that the sum of values of $n$ over all test cases does not exceed $10^5$.</p>

## Output

<p>For each test case output two integers&nbsp;— the minimal and the maximal possible beauty.</p>





```input1
2
3 3
3 6 9
3 3
6 4 11
```




```output1
6 6
7 8
```



## Note

<p>In the first test case the beauty of the array does not change if we perform any operations.</p><p>In the second example we can leave the array unchanged to attain the maximum beauty, and to get the minimum beauty one can replace two elements $4$ and $11$ with their sum, yielding an array $[6, 15]$, which has its beauty equal to $7$.</p>
