## Description

<div><p>Jack has a graph of $n$ vertices and $m$ edges. All edges are bidirectional and of unit length. The graph is connected, i.&nbsp;e. there exists a path between any two of its vertices. There can be more than one edge connecting the same pair of vertices. The graph can contain self-loops, i.&nbsp;e. edges connecting a node to itself.</p><p>The distance between vertices $u$ and $v$ is denoted as $\rho(u, v)$ and equals the minimum possible number of edges on a path between $u$ and $v$. The diameter of graph $G$ is defined as the maximum possible distance between some pair of its vertices. We denote it as $d(G)$. In other words, $$d(G) = \max_{1 \le u, v \le n}{\rho(u, v)}.$$</p><p>Jack plans to consecutively apply $q$ updates to his graph. Each update adds exactly one edge to the graph. Denote as $G_i$ the graph after exactly $i$ updates are made. Jack wants to calculate $q + 1$ values $d(G_0), d(G_1), d(G_2), \ldots, d(G_q)$.</p><p>However, Jack suspects that finding the exact diameters of $q + 1$ graphs might be a difficult task, so he is fine with approximate answers that differ from the correct answers no more than twice. Formally, Jack wants to find a sequence of positive integers $a_0, a_1, a_2, \ldots, a_q$ such that $$\left\lceil \frac{d(G_i)}{2} \right\rceil \le a_i \le 2 \cdot d(G_i)$$ for each $i$.</p><p><span class="tex-font-style-bf">Hacks</span></p><p>You cannot make hacks in this problem.</p></div><div class="input-specification"><p>The first line of the input contains three integers $n$, $m$, and $q$ ($2 \leq n \leq 10^5$, $n - 1 \leq m \leq 10^5$, $0 \leq q \leq 10^5$), the number of vertices in the given graph, the number of edges and the number of updates, respectively.</p><p>Then follow $m$ lines describing the initial edges of the graph. The $i$-th of these lines contains two integers $u_i$ and $v_i$ ($1 \leq u_i, v_i \leq n$), the indexes of the vertices connected by the $i$-th edge.</p><p>Then follow $q$ lines describing the updates. The $i$-th of these lines contains two integers $u'_i$ and $v'_i$ ($1 \leq u'_i, v'_i \leq n$), the indexes of the vertices connected by the edge that is added to the graph in the $i$-th update.</p><p><span class="tex-font-style-bf">Important note.</span> For testing purposes, the input data <span class="tex-font-style-bf">may</span> contain some extra lines after the mentioned input format. These will be used by the checker to verify your answer. They are not a part of the test data, you should not use them in any way and you can even omit reading them. </p></div><div class="output-specification"><p>Print a sequence of $q + 1$ positive integers $a_0, a_1, a_2, \ldots, a_q$. The $i$-th of these integers should differ from the diameter of graph $G_i$ no more than twice.</p></div>

## Input

<p>The first line of the input contains three integers $n$, $m$, and $q$ ($2 \leq n \leq 10^5$, $n - 1 \leq m \leq 10^5$, $0 \leq q \leq 10^5$), the number of vertices in the given graph, the number of edges and the number of updates, respectively.</p><p>Then follow $m$ lines describing the initial edges of the graph. The $i$-th of these lines contains two integers $u_i$ and $v_i$ ($1 \leq u_i, v_i \leq n$), the indexes of the vertices connected by the $i$-th edge.</p><p>Then follow $q$ lines describing the updates. The $i$-th of these lines contains two integers $u'_i$ and $v'_i$ ($1 \leq u'_i, v'_i \leq n$), the indexes of the vertices connected by the edge that is added to the graph in the $i$-th update.</p><p><span class="tex-font-style-bf">Important note.</span> For testing purposes, the input data <span class="tex-font-style-bf">may</span> contain some extra lines after the mentioned input format. These will be used by the checker to verify your answer. They are not a part of the test data, you should not use them in any way and you can even omit reading them. </p>

## Output

<p>Print a sequence of $q + 1$ positive integers $a_0, a_1, a_2, \ldots, a_q$. The $i$-th of these integers should differ from the diameter of graph $G_i$ no more than twice.</p>





```input1
9 10 8
1 2
2 3
2 4
3 5
4 5
5 6
5 7
6 8
7 8
8 9
3 4
6 7
2 8
1 9
1 6
4 9
3 9
7 1
```




```input2
8 7 9
1 2
2 3
3 4
4 5
5 6
6 7
7 8
1 5
3 7
2 4
4 6
6 8
8 2
5 4
2 4
3 3
1 652997 124613 653029 653029 124613 124613 124613 648901 124613 653029
```




```output1
10 6 5 6 2 4 2 2 1
```




```output2
7 5 4 4 4 3 3 3 3 3
```



## Note

<p>In the first example, the correct sequence of $d(G_0), d(G_1), d(G_2), \ldots, d(G_q)$ is $6, 6, 6, 3, 3, 3, 2, 2, 2$. </p><p>In the second example, the input contains an extra line that you can omit reading. It is not a part of the test and will be used for verifying your answer. The output of the second example contains the correct values of $d(G_i)$.</p>
