## Description

<div><p>Monocarp is practicing for a big contest. He plans to solve $n$ problems to make sure he's prepared. Each of these problems has a difficulty level: the first problem has a difficulty level of $1$, the second problem has a difficulty level of $2$, and so on, until the last ($n$-th) problem, which has a difficulty level of $n$.</p><p>Monocarp will choose some order in which he is going to solve all $n$ problems. Whenever he solves a problem which is more difficult than the last problem he solved, he gets excited because he feels like he's progressing. He doesn't get excited when he solves the first problem in his chosen order.</p><p>For example, if Monocarp solves the problems in the order $[3, \underline{5}, 4, 1, \underline{6}, 2]$, he gets excited twice (the corresponding problems are underlined).</p><p>Monocarp wants to get excited exactly $k$ times during his practicing session. Help him to choose the order in which he has to solve the problems!</p></div><div class="input-specification"><p>The first line contains one integer $t$ ($1 \le t \le 1000$) — the number of test cases.</p><p>Each test case consists of one line containing two integers $n$ and $k$ ($2 \le n \le 50$; $0 \le k \le n - 1$).</p></div><div class="output-specification"><p>For each test case, print $n$ <span class="tex-font-style-bf">distinct</span> integers from $1$ to $n$, denoting the order in which Monocarp should solve the problems. If there are multiple answers, print any of them.</p><p>It can be shown that under the constraints of the problem, the answer always exists.</p></div>

## Input

<p>The first line contains one integer $t$ ($1 \le t \le 1000$) — the number of test cases.</p><p>Each test case consists of one line containing two integers $n$ and $k$ ($2 \le n \le 50$; $0 \le k \le n - 1$).</p>

## Output

<p>For each test case, print $n$ <span class="tex-font-style-bf">distinct</span> integers from $1$ to $n$, denoting the order in which Monocarp should solve the problems. If there are multiple answers, print any of them.</p><p>It can be shown that under the constraints of the problem, the answer always exists.</p>





```input1|2,4
3
6 2
5 4
5 0
```




```output1
3 5 4 1 6 2
1 2 3 4 5
5 4 3 2 1
```


