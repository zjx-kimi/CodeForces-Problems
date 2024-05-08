## Description

<div><p>Call an array $a$ of length $n$ <span class="tex-font-style-it">sorted</span> if $a_1 \leq a_2 \leq \ldots \leq a_{n-1} \leq a_n$.</p><p>Ntarsis has an array $a$ of length $n$. </p><p>He is allowed to perform one type of operation on it (zero or more times): </p><ul> <li> Choose an index $i$ ($1 \leq i \leq n-1$). </li><li> Add $1$ to $a_1, a_2, \ldots, a_i$. </li><li> Subtract $1$ from $a_{i+1}, a_{i+2}, \ldots, a_n$. </li></ul><p>The values of $a$ can be negative after an operation.</p><p>Determine the minimum operations needed to make $a$ <span class="tex-font-style-bf">not sorted</span>.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 100$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2 \leq n \leq 500$)&nbsp;— the length of the array $a$.</p><p>The next line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \leq a_i \leq 10^9$)&nbsp;— the values of array $a$.</p><p>It is guaranteed that the sum of $n$ across all test cases does not exceed $500$.</p></div><div class="output-specification"><p>Output the minimum number of operations needed to make the array <span class="tex-font-style-bf">not sorted</span>.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 100$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2 \leq n \leq 500$)&nbsp;— the length of the array $a$.</p><p>The next line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \leq a_i \leq 10^9$)&nbsp;— the values of array $a$.</p><p>It is guaranteed that the sum of $n$ across all test cases does not exceed $500$.</p>

## Output

<p>Output the minimum number of operations needed to make the array <span class="tex-font-style-bf">not sorted</span>.</p>





```input1|2,3,6,7
4
2
1 1
4
1 8 10 13
3
1 3 2
3
1 9 14
```




```output1
1
2
0
3
```



## Note

<p>In the first case, we can perform $1$ operation to make the array not sorted: </p><ul> <li> Pick $i = 1$. The array $a$ then becomes $[2, 0]$, which is not sorted. </li></ul><p>In the second case, we can perform $2$ operations to make the array not sorted: </p><ul> <li> Pick $i = 3$. The array $a$ then becomes $[2, 9, 11, 12]$. </li><li> Pick $i = 3$. The array $a$ then becomes $[3, 10, 12, 11]$, which is not sorted. </li></ul><p>It can be proven that $1$ and $2$ operations are the minimal numbers of operations in the first and second test cases, respectively.</p><p>In the third case, the array is <span class="tex-font-style-bf"><span class="tex-font-style-underline">already</span></span> not sorted, so we perform $0$ operations.</p>
