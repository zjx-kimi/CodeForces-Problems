## Description

<div><p>You are given two integers $n$ and $k$.</p><p>For an array of length $n$, let's define its <span class="tex-font-style-it">cost</span> as the maximum number of contiguous subarrays of this array that can be chosen so that: </p><ul> <li> each element belongs to at most one subarray; </li><li> the length of each subarray is exactly $k$; </li><li> each subarray contains each integer from $1$ to $k$ exactly once. </li></ul><p>For example, if $n = 10$, $k = 3$ and the array is $[1, 2, 1, 3, 2, 3, 2, 3, 1, 3]$, its cost is $2$ because, for example, we can choose the subarrays from the $2$-nd element to the $4$-th element and from the $7$-th element to the $9$-th element, and we can show that it's impossible to choose more than $2$ subarrays.</p><p>Calculate the sum of costs over all arrays of length $n$ consisting of integers from $1$ to $k$, and print it modulo $998244353$.</p></div><div class="input-specification"><p>The only line of the input contains two integers $n$ and $k$ ($2 \le k \le n \le 4000$).</p></div><div class="output-specification"><p>Print one integer — the sum of costs of all arrays of length $n$ consisting of integers from $1$ to $k$ taken modulo $998244353$.</p></div>

## Input

<p>The only line of the input contains two integers $n$ and $k$ ($2 \le k \le n \le 4000$).</p>

## Output

<p>Print one integer — the sum of costs of all arrays of length $n$ consisting of integers from $1$ to $k$ taken modulo $998244353$.</p>





```input1
10 3
```




```input2
2 2
```




```input3
1337 42
```




```output1
71712
```




```output2
2
```




```output3
524933698
```


