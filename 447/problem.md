## Description

<div><div class="epigraph"><div class="epigraph-text"><span class="tex-font-style-it"><a href="https://soundcloud.com/popskyy/popskyy-tiasu-dual">Popskyy &amp; tiasu - Dual</a></span></div><div class="epigraph-source">⠀</div></div><p><span class="tex-font-style-bf">The only difference between the two versions of this problem is the constraint on the maximum number of operations. You can make hacks only if all versions of the problem are solved.</span></p><p>You are given an array $a_1, a_2,\dots, a_n$ of integers (positive, negative or $0$). You can perform multiple operations on the array (possibly $0$ operations).</p><p>In one operation, you choose $i, j$ ($1 \leq i, j \leq n$, they can be equal) and set $a_i := a_i + a_j$ (i.e., add $a_j$ to $a_i$).</p><p>Make the array non-decreasing (i.e., $a_i \leq a_{i+1}$ for $1 \leq i \leq n-1$) in at most $50$ operations. You do not need to minimize the number of operations.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 500$). The description of the test cases follows.</p><p>The first line contains a single integer $n$ ($1 \le n \le 20$) — the length of the array.</p><p>The second line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($-20 \le a_i \le 20$) — the array before performing the operations.</p></div><div class="output-specification"><p>For each test case, output your operations in the following format.</p><p>The first line should contain an integer $k$ ($0 \le k \le 50$) — the number of operations.</p><p>The next $k$ lines represent the $k$ operations in order. Each of these $k$ lines should contain two integers $i$ and $j$ ($1 \leq i, j \leq n$) — the corresponding operation consists in adding $a_j$ to $a_i$.</p><p>After all the operations, the array $a_1, a_2,\dots, a_n$ must be non-decreasing.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 500$). The description of the test cases follows.</p><p>The first line contains a single integer $n$ ($1 \le n \le 20$) — the length of the array.</p><p>The second line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($-20 \le a_i \le 20$) — the array before performing the operations.</p>

## Output

<p>For each test case, output your operations in the following format.</p><p>The first line should contain an integer $k$ ($0 \le k \le 50$) — the number of operations.</p><p>The next $k$ lines represent the $k$ operations in order. Each of these $k$ lines should contain two integers $i$ and $j$ ($1 \leq i, j \leq n$) — the corresponding operation consists in adding $a_j$ to $a_i$.</p><p>After all the operations, the array $a_1, a_2,\dots, a_n$ must be non-decreasing.</p>





```input1|2,3,6,7,10,11,14,15,18,19
10
2
2 1
4
1 2 -10 3
5
2 1 1 1 1
8
0 0 0 0 0 0 0 0
5
1 2 -4 3 -10
10
11 12 13 14 15 -15 -16 -17 -18 -19
7
1 9 3 -4 -3 -2 -1
3
10 9 8
20
1 -14 2 -10 6 -5 10 -13 10 7 -14 19 -5 19 1 18 -16 -7 12 8
20
-15 -17 -13 8 14 -13 10 -4 11 -4 -16 -6 15 -4 -2 7 -9 5 -5 17
```




```output1
1
2 1
3
4 4
4 4
3 4
4
2 1
3 1
4 1
5 1
0
7
3 4
3 4
5 4
5 4
5 4
5 4
5 4
15
6 1
6 1
6 1
7 2
7 2
7 2
8 3
8 3
8 3
9 4
9 4
9 4
10 5
10 5
10 5
8
3 4
3 4
2 4
2 4
2 4
2 4
1 4
1 4
3
2 1
3 1
3 1
31
14 1
18 7
13 11
15 11
6 4
5 17
19 6
19 12
10 5
11 12
1 17
15 19
16 10
14 2
16 11
20 7
7 6
9 5
3 6
6 14
17 18
18 14
12 3
17 16
8 18
13 16
9 8
14 8
16 2
11 8
12 7
31
5 12
19 13
9 1
5 17
18 19
6 16
15 8
6 9
15 14
7 10
19 7
17 20
14 4
15 20
4 3
1 8
16 12
16 15
5 6
12 10
11 15
20 3
20 19
13 14
11 14
18 10
7 3
12 17
4 7
13 2
11 13
```



## Note

<p>In the first test case, by adding $a_1 = 2$ to $a_2$, we get the array $[2, 3]$ which is non-decreasing.</p><p>In the second test case, the array changes as: </p><ul> <li> $[1, 2, -10, 3]$ </li><li> $[1, 2, -10, 6]$ </li><li> $[1, 2, -10, 12]$ </li><li> $[1, 2, 2, 12]$ </li></ul><p>In the third test case, the final array is $[2, 3, 3, 3, 3]$.</p>
