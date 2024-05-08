## Description

<div><p>Sasha wants to take a walk with his girlfriend in the city. The city consists of $n$ intersections, numbered from $1$ to $n$. Some of them are connected by roads, and from any intersection, there is exactly one simple path$^{\dagger}$ to any other intersection. In other words, the intersections and the roads between them form a tree.</p><p>Some of the intersections are considered dangerous. Since it is unsafe to walk alone in the city, Sasha does not want to visit three or more dangerous intersections during the walk.</p><p>Sasha calls a set of intersections <span class="tex-font-style-it">good</span> if the following condition is satisfied:</p><ul><li> If in the city only the intersections contained in this set are dangerous, then any simple path in the city contains <span class="tex-font-style-bf">no more than two</span> dangerous intersections.</li></ul><p>However, Sasha does not know which intersections are dangerous, so he is interested in the number of different good sets of intersections in the city. Since this number can be very large, output it modulo $998\,244\,353$.</p><p>$^{\dagger}$A simple path is a path that passes through each intersection at most once.</p></div><div class="input-specification"><p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 10^4$) — the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2 \le n \leq 3 \cdot 10^5$) — the number of intersections in the city.</p><p>The next $(n - 1)$ lines describe the roads. The $i$-th line contains two integers $u_i$ and $v_i$ ($1 \leq u_i, v_i \leq n$, $u_i \ne v_i$) — the numbers of the intersections connected by the $i$-th road.</p><p>It is guaranteed that these roads form a tree.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $3 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output a single integer — the number of good sets of intersections modulo $998\,244\,353$.</p></div>

## Input

<p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 10^4$) — the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2 \le n \leq 3 \cdot 10^5$) — the number of intersections in the city.</p><p>The next $(n - 1)$ lines describe the roads. The $i$-th line contains two integers $u_i$ and $v_i$ ($1 \leq u_i, v_i \leq n$, $u_i \ne v_i$) — the numbers of the intersections connected by the $i$-th road.</p><p>It is guaranteed that these roads form a tree.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $3 \cdot 10^5$.</p>

## Output

<p>For each test case, output a single integer — the number of good sets of intersections modulo $998\,244\,353$.</p>





```input1|2,3,4,9,10,11,12,13
4
3
1 3
3 2
4
3 4
2 3
3 1
5
1 2
3 4
5 1
2 3
4
1 2
2 3
3 4
```




```output1
7
12
16
11
```



## Note

<p>In the first test case, there are $2^3 = 8$ sets of intersections. All of them are good, except for the set $\{1, 2, 3\}$, because if intersections $1, 2$, and $3$ are dangerous, then the simple path $1 - 2 - 3$ contains $3$ dangerous intersections. Thus, there are $7$ good sets.</p><p>In the second test case, there are $2^4 = 16$ sets of intersections. Among them, the sets $\{1, 2, 3, 4\}$, $\{1, 2, 3\}$, $\{1, 3, 4\}$, $\{2, 3, 4\}$ are not good. Thus, there are a total of $12$ good sets. The city layout is shown below:</p><center> <img class="tex-graphics" src="file://5TiEVaZI.png" style="max-width: 100.0%;max-height: 100.0%;"> </center>
