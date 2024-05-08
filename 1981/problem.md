## Description

<div><p>Pchelyonok decided to give Mila a gift. Pchelenok has already bought an array $a$ of length $n$, but gifting an array is too common. Instead of that, he decided to gift Mila the segments of that array!</p><p>Pchelyonok wants his gift to be beautiful, so he decided to choose $k$ non-overlapping segments of the array $[l_1,r_1]$, $[l_2,r_2]$, $\ldots$ $[l_k,r_k]$ such that:</p><ul> <li> the length of the first segment $[l_1,r_1]$ is $k$, the length of the second segment $[l_2,r_2]$ is $k-1$, $\ldots$, the length of the $k$-th segment $[l_k,r_k]$ is $1$ </li><li> for each $i&lt;j$, the $i$-th segment occurs in the array earlier than the $j$-th (i.e. $r_i&lt;l_j$) </li><li> the sums in these segments are strictly increasing (i.e. let $sum(l \ldots r) = \sum\limits_{i=l}^{r} a_i$ — the sum of numbers in the segment $[l,r]$ of the array, then $sum(l_1 \ldots r_1) &lt; sum(l_2 \ldots r_2) &lt; \ldots &lt; sum(l_k \ldots r_k)$). </li></ul><p>Pchelenok also wants his gift to be as beautiful as possible, so he asks you to find the maximal value of $k$ such that he can give Mila a gift!</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 100$) — the number of test cases. The next $2 \cdot t$ lines contain the descriptions of test cases. The description of each test case consists of two lines.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 10^5$) — the length of the array.</p><p>The second line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le 10^9$) — the elements of the array $a$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p></div><div class="output-specification"><p>For each test case, print the maximum possible value of $k$.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 100$) — the number of test cases. The next $2 \cdot t$ lines contain the descriptions of test cases. The description of each test case consists of two lines.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 10^5$) — the length of the array.</p><p>The second line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le 10^9$) — the elements of the array $a$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p>

## Output

<p>For each test case, print the maximum possible value of $k$.</p>





```input1
5
1
1
3
1 2 3
5
1 1 2 2 3
7
1 2 1 1 3 2 6
5
9 6 7 9 7
```




```output1
1
1
2
3
1
```


