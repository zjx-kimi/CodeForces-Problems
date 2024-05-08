## Description

<div><p><span class="tex-font-style-it">She does her utmost to flawlessly carry out a person's last rites and preserve the world's balance of yin and yang.</span></p><p>Hu Tao, being the little prankster she is, has tried to scare you with this graph problem! You are given a connected undirected graph of $n$ nodes with $m$ edges. You also have $q$ queries. Each query consists of two nodes $a$ and $b$.</p><p>Initially, all edges in the graph have a weight of $0$. For each query, you must choose a simple path starting from $a$ and ending at $b$. Then you add $1$ to every edge along this path. Determine if it's possible, after processing all $q$ queries, for all edges in this graph to have an even weight. If so, output the choice of paths for each query. </p><p>If it is not possible, determine the smallest number of extra queries you could add to make it possible. It can be shown that this number will not exceed $10^{18}$ under the given constraints.</p><p>A simple path is defined as any path that does not visit a node more than once.</p><p>An edge is said to have an even weight if its value is divisible by $2$.</p></div><div class="input-specification"><p>The first line contains two integers $n$ and $m$ ($2 \leq n \leq 3 \cdot 10^5$, $n-1 \leq m \leq \min{\left(\frac{n(n-1)}{2}, 3 \cdot 10^5\right)}$).</p><p>Each of the next $m$ lines contains two integers $x$ and $y$ ($1 \leq x, y \leq n$, $x\neq y$) indicating an undirected edge between node $x$ and $y$. The input will not contain self-loops or duplicate edges, and the provided graph will be connected.</p><p>The next line contains a single integer $q$ ($1 \leq q \leq 3 \cdot 10^5$).</p><p>Each of the next $q$ lines contains two integers $a$ and $b$ ($1 \leq a, b \leq n, a \neq b$), the description of each query.</p><p>It is guaranteed that $nq \leq 3 \cdot 10^5$.</p></div><div class="output-specification"><p>If it is possible to force all edge weights to be even, print "<span class="tex-font-style-tt">YES</span>" on the first line, followed by $2q$ lines indicating the choice of path for each query in the same order the queries are given. For each query, the first line should contain a single integer $x$: the number of nodes in the chosen path. The next line should then contain $x$ spaced separated integers $p_i$ indicating the path you take ($p_1 = a, p_x = b$ and all numbers should fall between $1$ and $n$). This path cannot contain duplicate nodes and must be a valid simple path in the graph.</p><p>If it is impossible to force all edge weights to be even, print "<span class="tex-font-style-tt">NO</span>" on the first line and the minimum number of added queries on the second line.</p></div>

## Input

<p>The first line contains two integers $n$ and $m$ ($2 \leq n \leq 3 \cdot 10^5$, $n-1 \leq m \leq \min{\left(\frac{n(n-1)}{2}, 3 \cdot 10^5\right)}$).</p><p>Each of the next $m$ lines contains two integers $x$ and $y$ ($1 \leq x, y \leq n$, $x\neq y$) indicating an undirected edge between node $x$ and $y$. The input will not contain self-loops or duplicate edges, and the provided graph will be connected.</p><p>The next line contains a single integer $q$ ($1 \leq q \leq 3 \cdot 10^5$).</p><p>Each of the next $q$ lines contains two integers $a$ and $b$ ($1 \leq a, b \leq n, a \neq b$), the description of each query.</p><p>It is guaranteed that $nq \leq 3 \cdot 10^5$.</p>

## Output

<p>If it is possible to force all edge weights to be even, print "<span class="tex-font-style-tt">YES</span>" on the first line, followed by $2q$ lines indicating the choice of path for each query in the same order the queries are given. For each query, the first line should contain a single integer $x$: the number of nodes in the chosen path. The next line should then contain $x$ spaced separated integers $p_i$ indicating the path you take ($p_1 = a, p_x = b$ and all numbers should fall between $1$ and $n$). This path cannot contain duplicate nodes and must be a valid simple path in the graph.</p><p>If it is impossible to force all edge weights to be even, print "<span class="tex-font-style-tt">NO</span>" on the first line and the minimum number of added queries on the second line.</p>





```input1
6 7
2 1
2 3
3 5
1 4
6 1
5 6
4 5
3
1 4
5 1
4 5
```




```input2
5 7
4 3
4 5
2 1
1 4
1 3
3 5
3 2
4
4 2
3 5
5 1
4 5
```




```output1
YES
2
1 4
4
5 3 2 1
5
4 1 2 3 5
```




```output2
NO
2
```



## Note

<p>Here is what the queries look like for the first test case (red corresponds to the 1st query, blue 2nd query, and green 3rd query): </p><center> <img class="tex-graphics" src="file://21DzoIhR.png" style="max-width: 100.0%;max-height: 100.0%;"> </center> Notice that every edge in the graph is part of either $0$ or $2$ colored query edges.<p>The graph in the second test case looks like this: </p><center> <img class="tex-graphics" src="file://CY5Hma4s.png" style="max-width: 100.0%;max-height: 100.0%;"> </center> There does not exist an assignment of paths that will force all edges to have even weights with the given queries. One must add at least $2$ new queries to obtain a set of queries that can satisfy the condition.
