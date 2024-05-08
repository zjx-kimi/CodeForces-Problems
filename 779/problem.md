## Description

<div><p>The <span class="tex-font-style-it">score</span> of a sequence $[s_1, s_2, \ldots, s_d]$ is defined as $\displaystyle \frac{s_1\cdot s_2\cdot \ldots \cdot s_d}{d!}$, where $d!=1\cdot 2\cdot \ldots \cdot d$. In particular, the score of an empty sequence is $1$.</p><p>For a sequence $[s_1, s_2, \ldots, s_d]$, let $m$ be the maximum score among all its subsequences. Its <span class="tex-font-style-it">cost</span> is defined as the maximum length of a subsequence with a score of $m$.</p><p>You are given a <span class="tex-font-style-bf">non-decreasing</span> sequence $[a_1, a_2, \ldots, a_n]$ of integers of length $n$. In other words, the condition $a_1 \leq a_2 \leq \ldots \leq a_n$ is satisfied. For each $k=1, 2, \ldots , n$, find the cost of the sequence $[a_1, a_2, \ldots , a_k]$. </p><p>A sequence $x$ is a subsequence of a sequence $y$ if $x$ can be obtained from $y$ by deletion of several (possibly, zero or all) elements.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^4$). The description of the test cases follows.</p><p>The first line of each test case contains an integer $n$ ($1\le n\le 10^5$)&nbsp;— the length of the given sequence. </p><p>The second line of each test case contains $n$ integers $a_1,a_2,\ldots,a_n$ ($1\le a_i\leq n$)&nbsp;— the given sequence. It is guaranteed that its elements are in non-decreasing order.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $5\cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output $n$ integers&nbsp;— the costs of sequences $[a_1, a_2, \ldots , a_k]$ in ascending order of $k$.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^4$). The description of the test cases follows.</p><p>The first line of each test case contains an integer $n$ ($1\le n\le 10^5$)&nbsp;— the length of the given sequence. </p><p>The second line of each test case contains $n$ integers $a_1,a_2,\ldots,a_n$ ($1\le a_i\leq n$)&nbsp;— the given sequence. It is guaranteed that its elements are in non-decreasing order.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $5\cdot 10^5$.</p>

## Output

<p>For each test case, output $n$ integers&nbsp;— the costs of sequences $[a_1, a_2, \ldots , a_k]$ in ascending order of $k$.</p>





```input1|2,3,6,7
3
3
1 2 3
2
1 1
5
5 5 5 5 5
```




```output1
1 1 2 
1 1 
1 2 3 4 5
```



## Note

<p>In the first test case: </p><ul> <li> The maximum score among the subsequences of $[1]$ is $1$. The subsequences $[1]$ and $[]$ (the empty sequence) are the only ones with this score. Thus, the cost of $[1]$ is $1$. </li><li> The maximum score among the subsequences of $[1, 2]$ is $2$. The only subsequence with this score is $[2]$. Thus, the cost of $[1, 2]$ is $1$. </li><li> The maximum score among the subsequences of $[1, 2, 3]$ is $3$. The subsequences $[2, 3]$ and $[3]$ are the only ones with this score. Thus, the cost of $[1, 2, 3]$ is $2$. </li></ul> Therefore, the answer to this case is $1\:\:1\:\:2$, which are the costs of $[1], [1, 2]$ and $[1, 2, 3]$ in this order.
