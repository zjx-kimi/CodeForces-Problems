## Description

<div><p>You are given an array $a$ consisting of $n$ integers and an integer $k$.</p><p>A pair $(l,r)$ is <span class="tex-font-style-it">good</span> if there exists a sequence of indices $i_1, i_2, \dots, i_m$ such that </p><ul> <li> $i_1=l$ and $i_m=r$; </li><li> $i_j &lt; i_{j+1}$ for all $1 \leq j &lt; m$; and </li><li> $|a_{i_j}-a_{i_{j+1}}| \leq k$ for all $1 \leq j &lt; m$. </li></ul><p>Find the number of pairs $(l,r)$ ($1 \leq l \leq r \leq n$) that are <span class="tex-font-style-it">good</span>.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 10^5$) — the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains two space-separated integers $n$ and $k$ ($1 \leq n \leq 5 \cdot 10^5$; $0 \leq k \leq 10^5$) — the length of the array $a$ and the integer $k$.</p><p>The second line of each test case contains $n$ space-separated integers $a_1,a_2,\ldots,a_n$ ($1 \leq a_i \leq 10^5$) — representing the array $a$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $5 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, print the number of <span class="tex-font-style-it">good</span> pairs.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 10^5$) — the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains two space-separated integers $n$ and $k$ ($1 \leq n \leq 5 \cdot 10^5$; $0 \leq k \leq 10^5$) — the length of the array $a$ and the integer $k$.</p><p>The second line of each test case contains $n$ space-separated integers $a_1,a_2,\ldots,a_n$ ($1 \leq a_i \leq 10^5$) — representing the array $a$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $5 \cdot 10^5$.</p>

## Output

<p>For each test case, print the number of <span class="tex-font-style-it">good</span> pairs.</p>





```input1|2,3,6,7
4
3 0
1 1 1
4 2
4 8 6 8
6 4
7 2 5 8 3 8
20 23
110 57 98 14 20 1 60 82 108 37 82 73 8 46 38 35 106 115 58 112
```




```output1
6
9
18
92
```



## Note

<p>In the first test case, <span class="tex-font-style-it">good</span> pairs are $(1,1)$, $(1,2)$, $(1,3)$, $(2,2)$, $(2,3)$, and $(3,3)$.</p><p>In the second test case, <span class="tex-font-style-it">good</span> pairs are $(1,1)$, $(1,3)$, $(1,4)$, $(2,2)$, $(2,3)$, $(2,4)$, $(3,3)$, $(3,4)$ and $(4,4)$. Pair $(1,4)$ is <span class="tex-font-style-it">good</span> because there exists a sequence of indices $1, 3, 4$ which satisfy the given conditions.</p>
