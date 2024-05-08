## Description

<div><p>You are given an <span class="tex-font-style-bf">unsorted</span> permutation $p_1, p_2, \ldots, p_n$. To sort the permutation, you choose a constant $k$ ($k \ge 1$) and do some operations on the permutation. In one operation, you can choose two integers $i$, $j$ ($1 \le j &lt; i \le n$) such that $i - j = k$, then swap $p_i$ and $p_j$.</p><p>What is the <span class="tex-font-style-bf">maximum</span> value of $k$ that you can choose to sort the given permutation?</p><p>A permutation is an array consisting of $n$ distinct integers from $1$ to $n$ in arbitrary order. For example, $[2, 3, 1, 5, 4]$ is a permutation, but $[1, 2, 2]$ is not a permutation ($2$ appears twice in the array) and $[1, 3, 4]$ is also not a permutation ($n = 3$ but there is $4$ in the array).</p><p>An unsorted permutation $p$ is a permutation such that there is at least one position $i$ that satisfies $p_i \ne i$.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^4$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2 \le n \le 10^{5}$)&nbsp;— the length of the permutation $p$.</p><p>The second line of each test case contains $n$ distinct integers $p_1, p_2, \ldots, p_n$ ($1 \le p_i \le n$)&nbsp;— the permutation $p$. It is guaranteed that the given numbers form a permutation of length $n$ and the given permutation is <span class="tex-font-style-bf">unsorted</span>.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^{5}$.</p></div><div class="output-specification"><p>For each test case, output the maximum value of $k$ that you can choose to sort the given permutation.</p><p>We can show that an answer always exists.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^4$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2 \le n \le 10^{5}$)&nbsp;— the length of the permutation $p$.</p><p>The second line of each test case contains $n$ distinct integers $p_1, p_2, \ldots, p_n$ ($1 \le p_i \le n$)&nbsp;— the permutation $p$. It is guaranteed that the given numbers form a permutation of length $n$ and the given permutation is <span class="tex-font-style-bf">unsorted</span>.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^{5}$.</p>

## Output

<p>For each test case, output the maximum value of $k$ that you can choose to sort the given permutation.</p><p>We can show that an answer always exists.</p>





```input1|2,3,6,7,10,11,14,15
7
3
3 1 2
4
3 4 1 2
7
4 2 6 7 5 3 1
9
1 6 7 4 9 2 3 8 5
6
1 5 3 4 2 6
10
3 10 5 2 9 6 7 8 1 4
11
1 11 6 4 8 3 7 5 9 10 2
```




```output1
1
2
3
4
3
2
3
```



## Note

<p>In the first test case, the maximum value of $k$ you can choose is $1$. The operations used to sort the permutation are: </p><ul> <li> Swap $p_2$ and $p_1$ ($2 - 1 = 1$) $\rightarrow$ $p = [1, 3, 2]$ </li><li> Swap $p_2$ and $p_3$ ($3 - 2 = 1$) $\rightarrow$ $p = [1, 2, 3]$ </li></ul><p>In the second test case, the maximum value of $k$ you can choose is $2$. The operations used to sort the permutation are: </p><ul> <li> Swap $p_3$ and $p_1$ ($3 - 1 = 2$) $\rightarrow$ $p = [1, 4, 3, 2]$ </li><li> Swap $p_4$ and $p_2$ ($4 - 2 = 2$) $\rightarrow$ $p = [1, 2, 3, 4]$ </li></ul>
