## Description

<div><p>You are given a permutation$^\dagger$ $p$ of length $n$ and a positive integer $k \le n$.</p><p>In one operation, you: </p><ul> <li> Choose $k$ <span class="tex-font-style-bf">distinct</span> elements $p_{i_1}, p_{i_2}, \ldots, p_{i_k}$. </li><li> Remove them and then add them sorted in increasing order to the end of the permutation. </li></ul><p>For example, if $p = [2,5,1,3,4]$ and $k = 2$ and you choose $5$ and $3$ as the elements for the operation, then $[2, \color{red}{5}, 1, \color{red}{3}, 4] \rightarrow [2, 1, 4, \color{red}{3},\color{red}{5}]$.</p><p>Find the minimum number of operations needed to sort the permutation in increasing order. It can be proven that it is always possible to do so.</p><p>$^\dagger$ A permutation of length $n$ is an array consisting of $n$ distinct integers from $1$ to $n$ in arbitrary order. For example, $[2,3,1,5,4]$ is a permutation, but $[1,2,2]$ is not a permutation ($2$ appears twice in the array), and $[1,3,4]$ is also not a permutation ($n=3$ but there is $4$ in the array).</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains two integers $n$ and $k$ ($2 \le n \le 10^5$, $1 \le k \le n$).</p><p>The second line of each test case contains $n$ integers $p_1,p_2,\ldots, p_n$ ($1 \le p_i \le n$). It is guaranteed that $p$ is a permutation.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p></div><div class="output-specification"><p>For each test case output a single integer&nbsp;— the minimum number of operations needed to sort the permutation. It can be proven that it is always possible to do so.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains two integers $n$ and $k$ ($2 \le n \le 10^5$, $1 \le k \le n$).</p><p>The second line of each test case contains $n$ integers $p_1,p_2,\ldots, p_n$ ($1 \le p_i \le n$). It is guaranteed that $p$ is a permutation.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p>

## Output

<p>For each test case output a single integer&nbsp;— the minimum number of operations needed to sort the permutation. It can be proven that it is always possible to do so.</p>





```input1|2,3,6,7
4
3 2
1 2 3
3 1
3 1 2
4 2
1 3 2 4
4 2
2 3 1 4
```




```output1
0
1
1
2
```



## Note

<p>In the first test case, the permutation is already sorted.</p><p>In the second test case, you can choose element $3$, and the permutation will become sorted as follows: $[\color{red}{3}, 1, 2] \rightarrow [1, 2, \color{red}{3}]$.</p><p>In the third test case, you can choose elements $3$ and $4$, and the permutation will become sorted as follows: $[1, \color{red}{3}, 2, \color{red}{4}] \rightarrow [1, 2, \color{red}{3},\color{red}{4}]$.</p><p>In the fourth test case, it can be shown that it is impossible to sort the permutation in $1$ operation. However, if you choose elements $2$ and $1$ in the first operation, and choose elements $3$ and $4$ in the second operation, the permutation will become sorted as follows: $[\color{red}{2}, 3, \color{red}{1}, 4] \rightarrow [\color{blue}{3}, \color{blue}{4}, \color{red}{1}, \color{red}{2}] \rightarrow [1,2, \color{blue}{3}, \color{blue}{4}]$.</p>
