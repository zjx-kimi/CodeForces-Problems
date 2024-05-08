## Description

<div><p>Toxel likes arrays. Before traveling to the Paldea region, Serval gave him an array $a$ as a gift. This array has $n$ <span class="tex-font-style-bf">pairwise distinct</span> elements.</p><p>In order to get more arrays, Toxel performed $m$ operations with the initial array. In the $i$-th operation, he modified the $p_{i}$-th element of the $(i-1)$-th array to $v_{i}$, resulting in the $i$-th array (the initial array $a$ is numbered as $0$). During modifications, Toxel guaranteed that the elements of each array are still <span class="tex-font-style-bf">pairwise distinct</span> after each operation.</p><p>Finally, Toxel got $m+1$ arrays and denoted them as $A_{0}=a, A_{1},\ldots,A_{m}$. For each pair $(i,j)$ ($0\le i&lt;j\le m$), Toxel defines its value as the number of distinct elements of the concatenation of $A_{i}$ and $A_{j}$. Now Toxel wonders, what is the sum of the values of all pairs? Please help him to calculate the answer.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1\le t\le10^{4}$). The description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $m$ ($1\le n,m\le2\cdot10^{5}$) — the length of the array and the number of operations.</p><p>The second line of each test case contains $n$ integers $a_{1},a_{2},\dots,a_{n}$ ($1\le a_{i}\le n+m$). It is guaranteed that all $a_i$ are pairwise distinct.</p><p>Each of the next $m$ lines of each test case contains two integers $p_{i}$ and $v_{i}$ ($1\le p_{i}\le n$, $1\le v_{i}\le n+m$) — the position of the modified element and its new value. It is guaranteed that the elements of each array are still pairwise distinct after each modification.</p><p>It is guaranteed that the sum of $n$ and the sum of $m$ over all test cases do not exceed $2\cdot10^{5}$.</p></div><div class="output-specification"><p>For each test case, print a single integer — the sum of the values of all pairs of arrays.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1\le t\le10^{4}$). The description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $m$ ($1\le n,m\le2\cdot10^{5}$) — the length of the array and the number of operations.</p><p>The second line of each test case contains $n$ integers $a_{1},a_{2},\dots,a_{n}$ ($1\le a_{i}\le n+m$). It is guaranteed that all $a_i$ are pairwise distinct.</p><p>Each of the next $m$ lines of each test case contains two integers $p_{i}$ and $v_{i}$ ($1\le p_{i}\le n$, $1\le v_{i}\le n+m$) — the position of the modified element and its new value. It is guaranteed that the elements of each array are still pairwise distinct after each modification.</p><p>It is guaranteed that the sum of $n$ and the sum of $m$ over all test cases do not exceed $2\cdot10^{5}$.</p>

## Output

<p>For each test case, print a single integer — the sum of the values of all pairs of arrays.</p>





```input1|2,3,4,5,9,10,11,12,13,14,15,16,17,18,19,20
3
3 2
1 2 3
1 4
2 5
1 1
1
1 1
10 10
4 6 9 12 16 20 2 10 19 7
1 3
5 4
2 17
2 18
6 11
7 1
8 17
5 5
5 5
2 2
```




```output1
13
1
705
```



## Note

<p>In the first test case, the arrays change as follows: $[1,2,3]\to[\underline{4},2,3]\to[4,\underline{5},3]$.</p><p>The concatenation of the $0$-th array and the $1$-st array is $\require{cancel}[1,2,3,4,\cancel{2},\cancel{3}]$. There are $4$ distinct elements.</p><p>The concatenation of the $0$-th array and the $2$-nd array is $\require{cancel}[1,2,3,4,5,\cancel{3}]$. There are $5$ distinct elements.</p><p>The concatenation of the $1$-st array and the $2$-nd array is $\require{cancel}[4,2,3,\cancel{4},5,\cancel{3}]$. There are $4$ distinct elements.</p><p>Strikethrough elements are duplicates in the array.</p><p>Therefore, the answer is $4+5+4=13$.</p><p>In the second test case, note that the array may remain unchanged after operations.</p>
