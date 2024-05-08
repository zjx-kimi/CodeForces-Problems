## Description

<div><p>You are given a positive integer $n$.</p><p>Find a permutation$^\dagger$ $p$ of length $n$ such that there do <span class="tex-font-style-bf">not</span> exist two <span class="tex-font-style-bf">distinct</span> indices $i$ and $j$ ($1 \leq i, j &lt; n$; $i \neq j$) such that $p_i$ divides $p_j$ and $p_{i+1}$ divides $p_{j+1}$.</p><p>Refer to the Notes section for some examples.</p><p>Under the constraints of this problem, it can be proven that at least one $p$ exists.</p><p>$^\dagger$ A permutation of length $n$ is an array consisting of $n$ distinct integers from $1$ to $n$ in arbitrary order. For example, $[2,3,1,5,4]$ is a permutation, but $[1,2,2]$ is not a permutation ($2$ appears twice in the array), and $[1,3,4]$ is also not a permutation ($n=3$ but there is $4$ in the array).</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 10^3$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($3 \leq n \leq 10^5$)&nbsp;— the length of the permutation $p$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p></div><div class="output-specification"><p>For each test case, output $p_1, p_2, \ldots, p_n$.</p><p>If there are multiple solutions, you may output any one of them.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 10^3$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($3 \leq n \leq 10^5$)&nbsp;— the length of the permutation $p$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p>

## Output

<p>For each test case, output $p_1, p_2, \ldots, p_n$.</p><p>If there are multiple solutions, you may output any one of them.</p>





```input1|2
2
4
3
```




```output1
4 1 2 3
1 2 3
```



## Note

<p>In the first test case, $p=[4,1,2,3]$ is a valid permutation. However, the permutation $p=[1,2,3,4]$ is not a valid permutation as we can choose $i=1$ and $j=3$. Then $p_1=1$ divides $p_3=3$ and $p_2=2$ divides $p_4=4$. Note that the permutation $p=[3, 4, 2, 1]$ is also not a valid permutation as we can choose $i=3$ and $j=2$. Then $p_3=2$ divides $p_2=4$ and $p_4=1$ divides $p_3=2$.</p><p>In the second test case, $p=[1,2,3]$ is a valid permutation. In fact, all $6$ permutations of length $3$ are valid.</p>
