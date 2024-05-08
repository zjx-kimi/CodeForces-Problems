## Description

<div><p>Let's define the anti-beauty of a multiset $\{b_1, b_2, \ldots, b_{len}\}$ as the number of occurrences of the number $len$ in the multiset.</p><p>You are given $m$ multisets, where the $i$-th multiset contains $n_i$ distinct elements, specifically: $c_{i, 1}$ copies of the number $a_{i,1}$, $c_{i, 2}$ copies of the number $a_{i,2}, \ldots, c_{i, n_i}$ copies of the number $a_{i, n_i}$. It is guaranteed that $a_{i, 1} &lt; a_{i, 2} &lt; \ldots &lt; a_{i, n_i}$. You are also given numbers $l_1, l_2, \ldots, l_m$ and $r_1, r_2, \ldots, r_m$ such that $1 \le l_i \le r_i \le c_{i, 1} + \ldots + c_{i, n_i}$.</p><p>Let's create a multiset $X$, initially empty. Then, for each $i$ from $1$ to $m$, you must perform the following action <span class="tex-font-style-bf">exactly once</span>:</p><ol><li> Choose some $v_i$ such that $l_i \le v_i \le r_i$</li><li> Choose any $v_i$ numbers from the $i$-th multiset and add them to the multiset $X$.</li></ol><p>You need to choose $v_1, \ldots, v_m$ and the added numbers in such a way that the resulting multiset $X$ has the <span class="tex-font-style-bf">minimum possible</span> anti-beauty.</p></div><div class="input-specification"><p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $m$ ($1 \le m \le 10^5$)&nbsp;— the number of given multisets.</p><p>Then, for each $i$ from $1$ to $m$, a data block consisting of three lines is entered.</p><p>The first line of each block contains three integers $n_i, l_i, r_i$ ($1 \le n_i \le 10^5, 1 \le l_i \le r_i \le c_{i, 1} + \ldots + c_{i, n_i} \le 10^{17}$)&nbsp;— the number of distinct numbers in the $i$-th multiset and the limits on the number of elements to be added to $X$ from the $i$-th multiset.</p><p>The second line of the block contains $n_i$ integers $a_{i, 1}, \ldots, a_{i, n_i}$ ($1 \le a_{i, 1} &lt; \ldots &lt; a_{i, n_i} \le 10^{17}$)&nbsp;— the distinct elements of the $i$-th multiset.</p><p>The third line of the block contains $n_i$ integers $c_{i, 1}, \ldots, c_{i, n_i}$ ($1 \le c_{i, j} \le 10^{12}$)&nbsp;— the number of copies of the elements in the $i$-th multiset.</p><p>It is guaranteed that the sum of the values of $m$ for all test cases does not exceed $10^5$, and also the sum of $n_i$ for all blocks of all test cases does not exceed $10^5$.</p></div><div class="output-specification"><p>For each test case, output the minimum possible anti-beauty of the multiset $X$ that you can achieve.</p></div>

## Input

<p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $m$ ($1 \le m \le 10^5$)&nbsp;— the number of given multisets.</p><p>Then, for each $i$ from $1$ to $m$, a data block consisting of three lines is entered.</p><p>The first line of each block contains three integers $n_i, l_i, r_i$ ($1 \le n_i \le 10^5, 1 \le l_i \le r_i \le c_{i, 1} + \ldots + c_{i, n_i} \le 10^{17}$)&nbsp;— the number of distinct numbers in the $i$-th multiset and the limits on the number of elements to be added to $X$ from the $i$-th multiset.</p><p>The second line of the block contains $n_i$ integers $a_{i, 1}, \ldots, a_{i, n_i}$ ($1 \le a_{i, 1} &lt; \ldots &lt; a_{i, n_i} \le 10^{17}$)&nbsp;— the distinct elements of the $i$-th multiset.</p><p>The third line of the block contains $n_i$ integers $c_{i, 1}, \ldots, c_{i, n_i}$ ($1 \le c_{i, j} \le 10^{12}$)&nbsp;— the number of copies of the elements in the $i$-th multiset.</p><p>It is guaranteed that the sum of the values of $m$ for all test cases does not exceed $10^5$, and also the sum of $n_i$ for all blocks of all test cases does not exceed $10^5$.</p>

## Output

<p>For each test case, output the minimum possible anti-beauty of the multiset $X$ that you can achieve.</p>





```input1|2,3,4,5,6,7,8,9,10,11,16,17,18,19,27,28,29,30,38,39,40,41,42,43,44
7
3
3 5 6
10 11 12
3 3 1
1 1 3
12
4
2 4 4
12 13
1 5
1
7 1000 1006
1000 1001 1002 1003 1004 1005 1006
147 145 143 143 143 143 142
1
2 48 50
48 50
25 25
2
1 1 1
1
1
1 1 1
2
1
1
1 1 1
1
2
2
1 1 1
1
1
2 1 1
1 2
1 1
2
4 8 10
11 12 13 14
3 3 3 3
2 3 4
11 12
2 2
```




```output1
1
139
0
1
1
0
0
```



## Note

<p>In the first test case, the multisets have the following form:</p><ol><li> $\{10, 10, 10, 11, 11, 11, 12\}$. From this multiset, you need to select between $5$ and $6$ numbers.</li><li> $\{12, 12, 12, 12\}$. From this multiset, you need to select between $1$ and $3$ numbers.</li><li> $\{12, 13, 13, 13, 13, 13\}$. From this multiset, you need to select $4$ numbers.</li></ol><p>You can select the elements $\{10, 11, 11, 11, 12\}$ from the first multiset, $\{12\}$ from the second multiset, and $\{13, 13, 13, 13\}$ from the third multiset. Thus, $X = \{10, 11, 11, 11, 12, 12, 13, 13, 13, 13\}$. The size of $X$ is $10$, the number $10$ appears exactly $1$ time in $X$, so the anti-beauty of $X$ is $1$. It can be shown that it is not possible to achieve an anti-beauty less than $1$.</p>
