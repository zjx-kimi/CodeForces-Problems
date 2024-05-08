## Description

<div><p>You are given a positive integer $n$.</p><p>In this problem, the $\operatorname{MEX}$ of a collection of integers $c_1,c_2,\dots,c_k$ is defined as the smallest <span class="tex-font-style-bf">positive</span> integer $x$ which does not occur in the collection $c$. </p><p>The <span class="tex-font-style-it">primality</span> of an array $a_1,\dots,a_n$ is defined as the number of pairs $(l,r)$ such that $1 \le l \le r \le n$ and $\operatorname{MEX}(a_l,\dots,a_r)$ is a prime number. </p><p>Find any permutation of $1,2,\dots,n$ with the maximum possible primality among all permutations of $1,2,\dots,n$. </p><p>Note: </p><ul> <li> A prime number is a number greater than or equal to $2$ that is not divisible by any positive integer except $1$ and itself. For example, $2,5,13$ are prime numbers, but $1$ and $6$ are not prime numbers. </li><li> A permutation of $1,2,\dots,n$ is an array consisting of $n$ distinct integers from $1$ to $n$ in arbitrary order. For example, $[2,3,1,5,4]$ is a permutation, but $[1,2,2]$ is not a permutation ($2$ appears twice in the array), and $[1,3,4]$ is also not a permutation ($n=3$ but there is $4$ in the array). </li></ul></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^4$). The description of the test cases follows.</p><p>The only line of each test case contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output $n$ integers: a permutation of $1,2,\dots,n$ that achieves the maximum possible primality.</p><p>If there are multiple solutions, print any of them.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^4$). The description of the test cases follows.</p><p>The only line of each test case contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output $n$ integers: a permutation of $1,2,\dots,n$ that achieves the maximum possible primality.</p><p>If there are multiple solutions, print any of them.</p>





```input1|2,4
3
2
1
5
```




```output1
2 1
1
5 2 1 4 3
```



## Note

<p>In the first test case, there are $3$ pairs $(l,r)$ with $1 \le l \le r \le 2$, out of which $2$ have a prime $\operatorname{MEX}(a_l,\dots,a_r)$: </p><ul> <li> $(l,r) = (1,1)$: $\operatorname{MEX}(2) = 1$, which is not prime. </li><li> $(l,r) = (1,2)$: $\operatorname{MEX}(2,1) = 3$, which is prime. </li><li> $(l,r) = (2,2)$: $\operatorname{MEX}(1) = 2$, which is prime. </li></ul> Therefore, the primality is $2$.<p>In the second test case, $\operatorname{MEX}(1) = 2$ is prime, so the primality is $1$.</p><p>In the third test case, the maximum possible primality is $8$.</p>
