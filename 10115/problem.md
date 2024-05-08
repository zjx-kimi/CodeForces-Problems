## Description

<div><p>A contest contains $n$ problems and the difficulty of the $i$-th problem is expected to be <span class="tex-font-style-bf">at most</span> $b_i$. There are already $n$ problem proposals and the difficulty of the $i$-th problem is $a_i$. Initially, both $a_1, a_2, \ldots, a_n$ and $b_1, b_2, \ldots, b_n$ are sorted in non-decreasing order.</p><p>Some of the problems may be more difficult than expected, so the writers must propose more problems. When a new problem with difficulty $w$ is proposed, the most difficult problem will be deleted from the contest, and the problems will be sorted in a way that the difficulties are non-decreasing.</p><p>In other words, in each operation, you choose an integer $w$, insert it into the array $a$, sort array $a$ in non-decreasing order, and remove the last element from it.</p><p>Find the minimum number of new problems to make $a_i\le b_i$ for all $i$.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1\le t\le 100$). The description of the test cases follows.</p><p>The first line of each test case contains only one positive integer $n$ ($1 \leq n \leq 100$), representing the number of problems.</p><p>The second line of each test case contains an array $a$ of length $n$ ($1\le a_1\le a_2\le\cdots\le a_n\le 10^9$).</p><p>The third line of each test case contains an array $b$ of length $n$ ($1\le b_1\le b_2\le\cdots\le b_n\le 10^9$).</p></div><div class="output-specification"><p>For each test case, print an integer as your answer in a new line.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1\le t\le 100$). The description of the test cases follows.</p><p>The first line of each test case contains only one positive integer $n$ ($1 \leq n \leq 100$), representing the number of problems.</p><p>The second line of each test case contains an array $a$ of length $n$ ($1\le a_1\le a_2\le\cdots\le a_n\le 10^9$).</p><p>The third line of each test case contains an array $b$ of length $n$ ($1\le b_1\le b_2\le\cdots\le b_n\le 10^9$).</p>

## Output

<p>For each test case, print an integer as your answer in a new line.</p>





```input1|2,3,4
2
6
1000 1400 2000 2000 2200 2700
800 1200 1500 1800 2200 3000
6
4 5 6 7 8 9
1 2 3 4 5 6
```




```output1
2
3
```



## Note

<p>In the first test case:</p><ul> <li> Propose a problem with difficulty $w=800$ and $a$ becomes $[800,1000,1400,2000,2000,2200]$. </li><li> Propose a problem with difficulty $w=1800$ and $a$ becomes $[800,1000,1400,1800,2000,2000]$. </li></ul><p>It can be proved that it's impossible to reach the goal by proposing fewer new problems.</p><p>In the second test case:</p><ul> <li> Propose a problem with difficulty $w=1$ and $a$ becomes $[1,4,5,6,7,8]$. </li><li> Propose a problem with difficulty $w=2$ and $a$ becomes $[1,2,4,5,6,7]$. </li><li> Propose a problem with difficulty $w=3$ and $a$ becomes $[1,2,3,4,5,6]$. </li></ul><p>It can be proved that it's impossible to reach the goal by proposing fewer new problems.</p>
