## Description

<div><p>Consider the insertion sort algorithm used to sort an integer sequence $[a_1, a_2, \ldots, a_n]$ of length $n$ in non-decreasing order.</p><p>For each $i$ in order from $2$ to $n$, do the following. If $a_i \ge a_{i-1}$, do nothing and move on to the next value of $i$. Otherwise, find the smallest $j$ such that $a_i &lt; a_j$, shift the elements on positions from $j$ to $i-1$ by one position to the right, and write down the initial value of $a_i$ to position $j$. In this case we'll say that we performed an <span class="tex-font-style-it">insertion</span> of an element from position $i$ to position $j$.</p><p>It can be noticed that after processing any $i$, the prefix of the sequence $[a_1, a_2, \ldots, a_i]$ is sorted in non-decreasing order, therefore, the algorithm indeed sorts any sequence.</p><p>For example, sorting $[4, 5, 3, 1, 3]$ proceeds as follows: </p><ul> <li> $i = 2$: $a_2 \ge a_1$, do nothing; </li><li> $i = 3$: $j = 1$, insert from position $3$ to position $1$: $[3, 4, 5, 1, 3]$; </li><li> $i = 4$: $j = 1$, insert from position $4$ to position $1$: $[1, 3, 4, 5, 3]$; </li><li> $i = 5$: $j = 3$, insert from position $5$ to position $3$: $[1, 3, 3, 4, 5]$. </li></ul><p>You are given an integer $n$ and a list of $m$ integer pairs $(x_i, y_i)$. We are interested in sequences such that if you sort them using the above algorithm, exactly $m$ insertions will be performed: first from position $x_1$ to position $y_1$, then from position $x_2$ to position $y_2$, ..., finally, from position $x_m$ to position $y_m$.</p><p>How many sequences of length $n$ consisting of (not necessarily distinct) integers between $1$ and $n$, inclusive, satisfy the above condition? Print this number modulo $998\,244\,353$.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^5$). Description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $m$ ($2 \le n \le 2 \cdot 10^5$; $0 \le m &lt; n$)&nbsp;— the length of the sequence and the number of insertions.</p><p>The $i$-th of the following $m$ lines contains two integers $x_i$ and $y_i$ ($2 \le x_1 &lt; x_2 &lt; \ldots &lt; x_m \le n$; $1 \le y_i &lt; x_i$). These lines describe the sequence of insertions in chronological order.</p><p>It is guaranteed that the sum of $m$ over all test cases does not exceed $2 \cdot 10^5$. <span class="tex-font-style-bf">Note that there is no constraint on the sum of $n$ of the same kind.</span></p></div><div class="output-specification"><p>For each test case, print the number of sequences of length $n$ consisting of integers from $1$ to $n$ such that sorting them with the described algorithm produces the given sequence of insertions, modulo $998\,244\,353$.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^5$). Description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $m$ ($2 \le n \le 2 \cdot 10^5$; $0 \le m &lt; n$)&nbsp;— the length of the sequence and the number of insertions.</p><p>The $i$-th of the following $m$ lines contains two integers $x_i$ and $y_i$ ($2 \le x_1 &lt; x_2 &lt; \ldots &lt; x_m \le n$; $1 \le y_i &lt; x_i$). These lines describe the sequence of insertions in chronological order.</p><p>It is guaranteed that the sum of $m$ over all test cases does not exceed $2 \cdot 10^5$. <span class="tex-font-style-bf">Note that there is no constraint on the sum of $n$ of the same kind.</span></p>

## Output

<p>For each test case, print the number of sequences of length $n$ consisting of integers from $1$ to $n$ such that sorting them with the described algorithm produces the given sequence of insertions, modulo $998\,244\,353$.</p>





```input1
3
3 0
3 2
2 1
3 1
5 3
3 1
4 1
5 3
```




```output1
10
1
21
```



## Note

<p>In the first test case, the algorithm performs no insertions&nbsp;— therefore, the initial sequence is already sorted in non-decreasing order. There are $10$ such sequences: $[1, 1, 1], [1, 1, 2], [1, 1, 3], [1, 2, 2], [1, 2, 3], [1, 3, 3], [2, 2, 2], [2, 2, 3], [2, 3, 3], [3, 3, 3]$.</p><p>In the second test case, the only sequence satisfying the conditions is $[3, 2, 1]$.</p><p>In the third test case, $[4, 5, 3, 1, 3]$ is one of the sought sequences.</p>
