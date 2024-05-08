## Description

<div><p>You are given an array $a_1,a_2,\ldots, a_n$ of <span class="tex-font-style-bf">pairwise distinct</span> integers from $0$ to $n$. Consider the following operation:</p><ul> <li> consecutively for each $i$ from $1$ to $n$ in this order, replace $a_i$ with $\operatorname{MEX}(a_1, a_2, \ldots, a_n)$. </li></ul><p>Here $\operatorname{MEX}$ of a collection of integers $c_1, c_2, \ldots, c_m$ is defined as the smallest non-negative integer $x$ which does not occur in the collection $c$. For example, $\operatorname{MEX}(0, 2, 2, 1, 4) = 3$ and $\operatorname{MEX}(1, 2) = 0$.</p><p>Print the array after applying $k$ such operations.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^5$). The description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $k$ ($1\le n\le 10^5$, $1\le k\le 10^9$).</p><p>The second line contains $n$ <span class="tex-font-style-bf">pairwise distinct</span> integers $a_1,a_2,\ldots, a_n$ ($0\le a_i\le n$) representing the elements of the array before applying the operations.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p></div><div class="output-specification"><p>For each test case, print all $n$ elements of the array after applying $k$ operations.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^5$). The description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $k$ ($1\le n\le 10^5$, $1\le k\le 10^9$).</p><p>The second line contains $n$ <span class="tex-font-style-bf">pairwise distinct</span> integers $a_1,a_2,\ldots, a_n$ ($0\le a_i\le n$) representing the elements of the array before applying the operations.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p>

## Output

<p>For each test case, print all $n$ elements of the array after applying $k$ operations.</p>





```input1|2,3,6,7,10,11
5
1 2
1
3 1
0 1 3
2 2
0 2
5 5
1 2 3 4 5
10 100
5 3 0 4 2 1 6 9 10 8
```




```output1
1
2 0 1
2 1
2 3 4 5 0
7 5 3 0 4 2 1 6 9 10
```



## Note

<p>In the first test case, here is the entire process:</p><ol> <li> On the first operation, the array changes from $[1]$ to $[0]$, since $\operatorname{MEX}(1) = 0$. </li><li> On the second operation, the array changes from $[0]$ to $[1]$, since $\operatorname{MEX}(0) = 1$. </li></ol><p>Thus, the array becomes $[1]$ after two operations.</p><p>In the second test case, the array changes as follows during one operation: $[{\mkern3mu\underline{\mkern-3mu {\bf 0}\mkern-3mu}\mkern3mu}, 1, 3] \rightarrow [2, {\mkern3mu\underline{\mkern-3mu {\bf 1}\mkern-3mu}\mkern3mu}, 3] \rightarrow [2, 0, {\mkern3mu\underline{\mkern-3mu {\bf 3}\mkern-3mu}\mkern3mu}] \rightarrow [2, 0, 1]$.</p><p>In the third test case, the array changes as follows during one operation: $[{\mkern3mu\underline{\mkern-3mu {\bf 0}\mkern-3mu}\mkern3mu}, 2] \rightarrow [1, {\mkern3mu\underline{\mkern-3mu {\bf 2}\mkern-3mu}\mkern3mu}] \rightarrow [1, 0]$. And during the second operation: $[{\mkern3mu\underline{\mkern-3mu {\bf 1}\mkern-3mu}\mkern3mu}, 0] \rightarrow [2, {\mkern3mu\underline{\mkern-3mu {\bf 0}\mkern-3mu}\mkern3mu}] \rightarrow [2, 1]$.</p>
