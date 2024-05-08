## Description

<div><p>Andrey is just starting to come up with problems, and it's difficult for him. That's why he came up with a strange problem about permutations$^{\dagger}$ and asks you to solve it. Can you do it?</p><p>Let's call the <span class="tex-font-style-it">cost</span> of a permutation $p$ of length $n$ the value of the expression:</p><center> <span>$(\sum_{i = 1}^{n} p_i \cdot i) - (\max_{j = 1}^{n} p_j \cdot j)$</span>. </center><p>Find the maximum cost among all permutations of length $n$.</p><p>$^{\dagger}$A permutation of length $n$ is an array consisting of $n$ distinct integers from $1$ to $n$ in arbitrary order. For example, $[2,3,1,5,4]$ is a permutation, but $[1,2,2]$ is not a permutation ($2$ appears twice in the array), and $[1,3,4]$ is also not a permutation ($n=3$ but there is $4$ in the array).</p></div><div class="input-specification"><p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 30$) — the number of test cases. The description of the test cases follows.</p><p>The only line of each test case contains a single integer $n$ ($2 \le n \le 250$) — the length of the permutation.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $500$.</p></div><div class="output-specification"><p>For each test case, output a single integer — the maximum cost among all permutations of length $n$.</p></div>

## Input

<p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 30$) — the number of test cases. The description of the test cases follows.</p><p>The only line of each test case contains a single integer $n$ ($2 \le n \le 250$) — the length of the permutation.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $500$.</p>

## Output

<p>For each test case, output a single integer — the maximum cost among all permutations of length $n$.</p>





```input1|2,4,6
5
2
4
3
10
20
```




```output1
2
17
7
303
2529
```



## Note

<p>In the first test case, the permutation with the maximum cost is $[2, 1]$. The cost is equal to $2 \cdot 1 + 1 \cdot 2 - \max (2 \cdot 1, 1 \cdot 2)= 2 + 2 - 2 = 2$.</p><p>In the second test case, the permutation with the maximum cost is $[1, 2, 4, 3]$. The cost is equal to $1 \cdot 1 + 2 \cdot 2 + 4 \cdot 3 + 3 \cdot 4 - 4 \cdot 3 = 17$.</p>
