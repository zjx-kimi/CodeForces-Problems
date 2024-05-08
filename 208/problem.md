## Description

<div><p>You are given a permutation$^\dagger$ $a$ of size $n$. We call an index $i$ <span class="tex-font-style-it">good</span> if $a_i=i$ is satisfied. After each second, we rotate all indices that are not good to the right by one position. Formally,</p><ul> <li> Let $s_1,s_2,\ldots,s_k$ be the indices of $a$ that are <span class="tex-font-style-bf">not</span> good in increasing order. That is, $s_j &lt; s_{j+1}$ and if index $i$ is not good, then there exists $j$ such that $s_j=i$. </li><li> For each $i$ from $1$ to $k$, we assign $a_{s_{(i \% k+1)}} := a_{s_i}$ all at once. </li></ul><p>For each $i$ from $1$ to $n$, find the first time that index $i$ becomes good.</p><p> $^\dagger$ A permutation is an array consisting of $n$ distinct integers from $1$ to $n$ in arbitrary order. For example, $[2,3,1,5,4]$ is a permutation, but $[1,2,2]$ is not a permutation ($2$ appears twice in the array) and $[1,3,4]$ is also not a permutation ($n=3$ but there is $4$ in the array).</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^4$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 10^6$)&nbsp;— the size of permutation $a$.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le n$)&nbsp;— the elements of permutation $a$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^6$.</p></div><div class="output-specification"><p>For each test case, output a single line containing $n$ integers where the $i$-th integer represents the first time that index $i$ becomes good.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^4$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 10^6$)&nbsp;— the size of permutation $a$.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le n$)&nbsp;— the elements of permutation $a$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^6$.</p>

## Output

<p>For each test case, output a single line containing $n$ integers where the $i$-th integer represents the first time that index $i$ becomes good.</p>





```input1|2,3
2
5
3 2 4 1 5
6
2 1 4 6 5 3
```




```output1
1 0 1 1 0 
2 1 2 1 0 1
```



## Note

<p>In the first test case, $2$ and $5$ are already in the correct position so indices $2$ and $5$ become good at $0$ second. After $1$ second, a cyclic shift will be done with $s=[1, 3, 4]$, resulting in array $a=[1, 2, 3, 4, 5]$. Notice that indices $1$, $3$ and $4$ become good at $1$ second.</p><p>In the second test case, $5$ is already in the correct position, so index $5$ becomes good at $0$ second. After $1$ second, a cyclic shift will be done with $s=[1, 2, 3, 4, 6]$, resulting in array $a=[3, 2, 1, 4, 5, 6]$. Notice that indices $2$, $4$ and $6$ become good at $1$ second. After $2$ seconds, a cyclic shift will be done with $s=[1, 3]$, resulting in array $a=[1, 2, 3, 4, 5, 6]$. Notice that indices $1$ and $3$ become good at $2$ second.</p>
