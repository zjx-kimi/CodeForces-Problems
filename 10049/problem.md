## Description

<div><p>The Master's Assistance Center has announced an entrance exam, which consists of the following.</p><p>The candidate is given a set $s$ of size $n$ and some strange integer $c$. For this set, it is needed to calculate the number of pairs of integers $(x, y)$ such that $0 \leq x \leq y \leq c$, $x + y$ <span class="tex-font-style-bf">is not</span> contained in the set $s$, and also $y - x$ <span class="tex-font-style-bf">is not</span> contained in the set $s$.</p><p>Your friend wants to enter the Center. Help him pass the exam!</p></div><div class="input-specification"><p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 2 \cdot 10^4$) — the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $c$ ($1 \leq n \leq 3 \cdot 10^5$, $1 \leq c \leq 10^9$) — the size of the set and the strange integer.</p><p>The second line of each test case contains $n$ integers $s_1, s_2, \ldots, s_{n}$ ($0 \leq s_1 &lt; s_2 &lt; \ldots &lt; s_{n} \leq c$) — the elements of the set $s$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $3 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output a single integer — the number of suitable pairs of integers.</p></div>

## Input

<p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 2 \cdot 10^4$) — the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $c$ ($1 \leq n \leq 3 \cdot 10^5$, $1 \leq c \leq 10^9$) — the size of the set and the strange integer.</p><p>The second line of each test case contains $n$ integers $s_1, s_2, \ldots, s_{n}$ ($0 \leq s_1 &lt; s_2 &lt; \ldots &lt; s_{n} \leq c$) — the elements of the set $s$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $3 \cdot 10^5$.</p>

## Output

<p>For each test case, output a single integer — the number of suitable pairs of integers.</p>





```input1|2,3,6,7,10,11,14,15
8
3 3
1 2 3
1 179
57
4 6
0 3 5 6
1 1
1
5 10
0 2 4 8 10
5 10
1 3 5 7 9
4 10
2 4 6 7
3 1000000000
228 1337 998244353
```




```output1
3
16139
10
2
33
36
35
499999998999122959
```



## Note

<p>In the first test case, the following pairs are suitable: $(0, 0)$, $(2, 2)$, $(3, 3)$.</p><p>In the third test case, the following pairs are suitable: $(0, 1)$, $(0, 2)$, $(0, 4)$, $(1, 3)$, $(2, 6)$, $(3, 4)$, $(3, 5)$, $(4, 5)$, $(4, 6)$, $(5, 6)$.</p>
