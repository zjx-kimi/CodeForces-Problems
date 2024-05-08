## Description

<div><p>A subarray of array $a$ from index $l$ to the index $r$ is the array $[a_l, a_{l+1}, \dots, a_{r}]$. The number of occurrences of the array $b$ in the array $a$ is the number of subarrays of $a$ such that they are equal to $b$.</p><p>You are given $n$ arrays $A_1, A_2, \dots, A_n$; the elements of these arrays are integers from $1$ to $k$. You have to build an array $a$ consisting of $m$ integers from $1$ to $k$ in such a way that, for <span class="tex-font-style-bf">every</span> given subarray $A_i$, the number of occurrences of $A_i$ in the array $a$ is <span class="tex-font-style-bf">not less</span> than the number of occurrences of each non-empty subarray of $A_i$ in $a$. Note that if $A_i$ doesn't occur in $a$, and no subarray of $A_i$ occurs in $a$, this condition is still met for $A_i$.</p><p>Your task is to calculate the number of different arrays $a$ you can build, and print it modulo $998244353$.</p></div><div class="input-specification"><p>The first line contains three integers $n$, $m$ and $k$ ($1 \le n, m, k \le 3 \cdot 10^5$) — the number of the given arrays, the desired length of the array $a$, and the upper bound on the values in the arrays.</p><p>Then $n$ lines follow. The $i$-th line represents the array $A_i$. The first integer in the $i$-th line is $c_i$ ($1 \le c_i \le m$) — the number of elements in $A_i$; then, $c_i$ integers from $1$ to $k$ follow — the elements of the array $A_i$.</p><p>Additional constraint on the input: $\sum\limits_{i=1}^n c_i \le 3 \cdot 10^5$; i. e., the number of elements in the given arrays in total does not exceed $3 \cdot 10^5$.</p></div><div class="output-specification"><p>Print one integer — the number of different arrays $a$ you can build, taken modulo $998244353$.</p></div>

## Input

<p>The first line contains three integers $n$, $m$ and $k$ ($1 \le n, m, k \le 3 \cdot 10^5$) — the number of the given arrays, the desired length of the array $a$, and the upper bound on the values in the arrays.</p><p>Then $n$ lines follow. The $i$-th line represents the array $A_i$. The first integer in the $i$-th line is $c_i$ ($1 \le c_i \le m$) — the number of elements in $A_i$; then, $c_i$ integers from $1$ to $k$ follow — the elements of the array $A_i$.</p><p>Additional constraint on the input: $\sum\limits_{i=1}^n c_i \le 3 \cdot 10^5$; i. e., the number of elements in the given arrays in total does not exceed $3 \cdot 10^5$.</p>

## Output

<p>Print one integer — the number of different arrays $a$ you can build, taken modulo $998244353$.</p>





```input1
2 4 3
2 1 2
1 3
```




```input2
2 4 3
2 1 2
3 3 2 1
```




```input3
1 42 1337
2 13 31
```




```output1
5
```




```output2
0
```




```output3
721234447
```


