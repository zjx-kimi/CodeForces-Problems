## Description

<div><p>You are given an undirected, connected graph of $n$ nodes and $m$ edges. All nodes $u$ of the graph satisfy the following:</p><ul> <li> Let $S_u$ be the set of vertices in the longest simple cycle starting and ending at $u$. </li><li> Let $C_u$ be the union of the sets of vertices in any simple cycle starting and ending at $u$. </li><li> $S_u = C_u$. </li></ul><p>You need to answer $q$ queries.</p><p>For each query, you will be given node $a$ and node $b$. Out of all the edges that belong to any simple path from $a$ to $b$, count the number of edges such that if you remove that edge, $a$ and $b$ are reachable from each other.</p></div><div class="input-specification"><p>The first line contains two integers $n$ and $m$ ($2 \le n \le 2 \cdot 10^5$, $1 \le m \le \min$($2 \cdot 10^5$, $(n \cdot (n-1))/2$)) — the total number of nodes and edges in the graph, respectively.</p><p>The next $m$ lines contain two integers $u$ and $v$ ($1 \le$ $u$, $v$ $\le n$, $u \neq v$) — describing an edge, implying that nodes $u$ and $v$ are connected to each other.</p><p>It is guaranteed that there is at most one edge between any pair of vertices in the graph and the given graph is connected.</p><p>The next line contains a single integer $q$ ($1 \le q \le 2 \cdot 10^5$) — the number of queries.</p><p>Then $q$ lines follow, each representing a query. Each query contains two integers $a$ and $b$ ($1 \le$ $a$, $b$ $\le n$).</p></div><div class="output-specification"><p>For each query, output a single integer — answer to the query.</p></div>

## Input

<p>The first line contains two integers $n$ and $m$ ($2 \le n \le 2 \cdot 10^5$, $1 \le m \le \min$($2 \cdot 10^5$, $(n \cdot (n-1))/2$)) — the total number of nodes and edges in the graph, respectively.</p><p>The next $m$ lines contain two integers $u$ and $v$ ($1 \le$ $u$, $v$ $\le n$, $u \neq v$) — describing an edge, implying that nodes $u$ and $v$ are connected to each other.</p><p>It is guaranteed that there is at most one edge between any pair of vertices in the graph and the given graph is connected.</p><p>The next line contains a single integer $q$ ($1 \le q \le 2 \cdot 10^5$) — the number of queries.</p><p>Then $q$ lines follow, each representing a query. Each query contains two integers $a$ and $b$ ($1 \le$ $a$, $b$ $\le n$).</p>

## Output

<p>For each query, output a single integer — answer to the query.</p>





```input1
10 11
1 2
2 3
3 4
4 5
5 3
2 7
7 9
9 10
10 6
6 7
1 8
5
1 4
5 10
3 5
2 8
7 10
```




```input2
13 15
1 2
2 3
3 4
4 1
2 4
3 5
5 6
6 7
6 8
7 9
9 10
8 7
10 11
10 12
10 13
6
9 11
1 5
1 8
5 2
5 12
12 13
```




```output1
3
7
3
0
4
```




```output2
0
5
8
5
3
0
```



## Note

<p>The graph in the first sample is : </p><center> <img class="tex-graphics" src="file://eD8PE2v9.png" style="max-width: 100.0%;max-height: 100.0%;"> </center><p>The first query is $(1, 4)$. There are $5$ total edges that belong to any simple path from $1$ to $4$. Edges $(3, 4), (4, 5), (5, 3)$ will be counted in the answer to the query.</p><p>The fourth query is $(2, 8)$. There is only one simple path from $2$ to $8$, thus none of the edges will be counted in the answer to the query.</p><p>The fifth query is $(7, 10)$. There are $4$ total edges that belong to any simple path from $7$ to $10$, all of them will be counted in the answer to the query.</p>
