## Description

<div><p>There are $n$ cities in Byteland, some of which are connected by roads, which can be traversed in any direction. The $i$-th road has its own hardness parameter $w_i$. Time spent on traversing a road with its hardness equal to $w_i$ is $\lceil\frac{w_i}{c}\rceil$, where $c$ is the current driving skill.</p><p>The travel network of Byteland is a tree. In other words, between any pair of cities, there is exactly one path that passes through each city at most once.</p><p>In some cities you can visit driving courses. A single course takes $T$ time to complete, and after completing the course the driver's skill $c$ is increased by $2$ times. Notice that the time $T$ required to complete a course is the same in all cities, and courses can be completed in the same city more than once.</p><p>You need to answer the $q$ queries: what is the minimum time it takes to get from the city $a$ to city $b$ if you start the travelling with driving skill $c = 1$?</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 10^4$) — the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $T$ ($1 \le n \le 10^5, 1 \le T \le 10^6$) - the number of cities and time required to complete a single driving course.</p><p>The following $n - 1$ lines each contain three integers $u_i$, $v_i$ and $w_i$ ($1 \le u_i, v_i \le n, 1 \le w_i \le 10^6, u_i \neq v_i$), which mean that there exists a road connecting towns $u_i$ and $v_i$ with hardness equal to $w_i$ .</p><p>The next line contains a binary string $s$ of length $n$, consisting only of symbols $0$ and $1$. If $s_i = 1$ ($1 \le i \le n$), then you can visit driving courses in the $i$-th city. If $s_i = 0$ ($1 \le i \le n$), then you cannot visit driving courses in the $i$-th city.</p><p>The next line contains a single integer $q$ ($1 \le q \le 10^5$) — the number of queries you are required to answer.</p><p>The next $q$ lines contain two integers $a_j$, $b_j$ ($1 \le a_j, b_j \le n, 1 \le j \le q$) — the cities you are required to process in the $j$-th query.</p><p>It is guaranteed that the given graph is a tree. It is guaranteed that the sum of $n$ and the sum of $q$ over all test cases does not exceed $10^5$.</p></div><div class="output-specification"><p>For each query, print one integer in a separate line — the minimum time it takes to get in the corresponding query.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 10^4$) — the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $T$ ($1 \le n \le 10^5, 1 \le T \le 10^6$) - the number of cities and time required to complete a single driving course.</p><p>The following $n - 1$ lines each contain three integers $u_i$, $v_i$ and $w_i$ ($1 \le u_i, v_i \le n, 1 \le w_i \le 10^6, u_i \neq v_i$), which mean that there exists a road connecting towns $u_i$ and $v_i$ with hardness equal to $w_i$ .</p><p>The next line contains a binary string $s$ of length $n$, consisting only of symbols $0$ and $1$. If $s_i = 1$ ($1 \le i \le n$), then you can visit driving courses in the $i$-th city. If $s_i = 0$ ($1 \le i \le n$), then you cannot visit driving courses in the $i$-th city.</p><p>The next line contains a single integer $q$ ($1 \le q \le 10^5$) — the number of queries you are required to answer.</p><p>The next $q$ lines contain two integers $a_j$, $b_j$ ($1 \le a_j, b_j \le n, 1 \le j \le q$) — the cities you are required to process in the $j$-th query.</p><p>It is guaranteed that the given graph is a tree. It is guaranteed that the sum of $n$ and the sum of $q$ over all test cases does not exceed $10^5$.</p>

## Output

<p>For each query, print one integer in a separate line — the minimum time it takes to get in the corresponding query.</p>





```input1
2
2 3
1 2 1
11
1
1 2
5 3
1 4 5
1 3 8
2 3 8
4 5 10
11001
5
1 5
2 5
5 1
3 4
4 2
```




```output1
1
11
14
11
13
15
```



## Note

<p>In the only query of the first test case, it is optimal to ignore the driving courses. Then the minimum time required is equal to the distance between vertexes $1$ and $2$, which is $1$.</p><p>In the first query of the second test case, we can spend $3$ time in city number $1$ visiting the driving courses, then go to vertex $5$. Then the minimum time required is $3 + \lceil\frac{5}{2}\rceil + \lceil\frac{10}{2}\rceil = 11$.</p>
