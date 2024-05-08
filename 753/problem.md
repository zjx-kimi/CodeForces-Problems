## Description

<div><p>You are given an array $a_1, a_2, \ldots, a_n$ of positive integers.</p><p>You can make this operation multiple (possibly zero) times:</p><ul> <li> Choose two indices $i$, $j$ ($1 \leq i, j \leq n$, $i \neq j$). </li><li> Assign $a_i := \lceil \frac{a_i}{a_j} \rceil$. Here $\lceil x \rceil$ denotes $x$ rounded up to the smallest integer $\geq x$. </li></ul><p>Is it possible to make all array elements equal by some sequence of operations (possibly empty)? If yes, print <span class="tex-font-style-bf">any</span> way to do it in at most $30n$ operations.</p><p>It can be proven, that under the problem constraints, if some way exists to make all elements equal, there exists a way with at most $30n$ operations.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \leq t \leq 1000$) — the number of test cases. Descriptions of test cases follow.</p><p>The first line of each test case description contains a single integer $n$ ($1 \leq n \leq 100$).</p><p>The second line of each test case description contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \leq a_i \leq 10^9$).</p><p>It is guaranteed, that the sum of $n$ for all test cases does not exceed $1000$.</p></div><div class="output-specification"><p>For each test case print a single integer $q$ ($-1 \leq q \leq 30n$). If $q=-1$, there is no solution, otherwise $q$ is equal to the number of operations.</p><p>If $q \geq 0$, on the next $q$ lines print two integers $i$, $j$ ($1 \leq i, j \leq n$, $i \neq j$) — descriptions of operations.</p><p>If there are multiple solutions, you can print any.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \leq t \leq 1000$) — the number of test cases. Descriptions of test cases follow.</p><p>The first line of each test case description contains a single integer $n$ ($1 \leq n \leq 100$).</p><p>The second line of each test case description contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \leq a_i \leq 10^9$).</p><p>It is guaranteed, that the sum of $n$ for all test cases does not exceed $1000$.</p>

## Output

<p>For each test case print a single integer $q$ ($-1 \leq q \leq 30n$). If $q=-1$, there is no solution, otherwise $q$ is equal to the number of operations.</p><p>If $q \geq 0$, on the next $q$ lines print two integers $i$, $j$ ($1 \leq i, j \leq n$, $i \neq j$) — descriptions of operations.</p><p>If there are multiple solutions, you can print any.</p>





```input1|2,3,6,7,10,11,14,15,18,19
10
1
100
3
1 1 1
2
2 1
2
5 5
3
4 3 2
4
3 3 4 4
2
2 100
5
5 3 6 7 8
6
3 3 80 3 8 3
4
19 40 19 55
```




```output1
0
0
-1
0
2
1 3
2 1
4
3 1
4 2
1 3
2 4
6
2 1
2 1
2 1
2 1
2 1
2 1
8
5 2
4 2
3 2
1 3
1 3
2 1
4 1
5 1
4
5 1
3 1
3 1
3 1
9
4 2
2 1
1 2
1 2
3 2
3 2
1 4
2 4
3 4
```



## Note

<p>In the first and second, fourth test cases all numbers are equal, so it is possible to do nothing.</p><p>In the third test case, it is impossible to make all numbers equal.</p><p>In the fifth test case: $[\color{red}{4}, 3, \color{blue}{2}] \to [\color{blue}{2}, \color{red}{3}, 2] \to [2, 2, 2]$.</p><p>In the sixth test case: $[\color{blue}{3}, 3, \color{red}{4}, 4] \to [3, \color{blue}{3}, 2, \color{red}{4}] \to [\color{red}{3}, 3, \color{blue}{2}, 2] \to [2, \color{red}{3}, 2, \color{blue}{2}] \to [2, 2, 2, 2]$.</p><p>Here the red numbers are $i$ indices (that will be assigned), blue numbers are $j$ indices.</p>
