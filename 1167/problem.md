## Description

<div><p>You are given an initially empty undirected graph with $n$ nodes, numbered from $1$ to $n$ (i.&nbsp;e. $n$ nodes and $0$ edges). You want to add $m$ edges to the graph, so the graph won't contain any self-loop or multiple edges.</p><p>If an edge connecting two nodes $u$ and $v$ is added, its weight must be equal to the greatest common divisor of $u$ and $v$, i.&nbsp;e. $\gcd(u, v)$.</p><p>In order to add edges to the graph, you can repeat the following process any number of times (possibly zero): </p><ul> <li> choose an integer $k \ge 1$; </li><li> add exactly $k$ edges to the graph, each having a weight equal to $k + 1$. Adding these $k$ edges costs $k + 1$ in total. </li></ul> Note that you can't create self-loops or multiple edges. Also, if you can't add $k$ edges of weight $k + 1$, you can't choose such $k$.<p>For example, if you can add $5$ more edges to the graph of weight $6$, you may add them, and it will cost $6$ for the whole pack of $5$ edges. But if you can only add $4$ edges of weight $6$ to the graph, you can't perform this operation for $k = 5$.</p><p>Given two integers $n$ and $m$, find the minimum total cost to form a graph of $n$ vertices and exactly $m$ edges using the operation above. If such a graph can't be constructed, output $-1$.</p><p>Note that the final graph may consist of several connected components.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \leq t \leq 10^4$). Description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $m$ ($2 \leq n \leq 10^6$; $1 \leq m \leq \frac{n(n-1)}{2}$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^6$. </p></div><div class="output-specification"><p>For each test case, print the minimum cost to build the graph, or $-1$ if you can't build such a graph.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \leq t \leq 10^4$). Description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $m$ ($2 \leq n \leq 10^6$; $1 \leq m \leq \frac{n(n-1)}{2}$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^6$. </p>

## Output

<p>For each test case, print the minimum cost to build the graph, or $-1$ if you can't build such a graph.</p>





```input1|2,4
4
4 1
6 10
9 4
10 11
```




```output1
2
-1
7
21
```



## Note

<p>In the first test case, we can add an edge between the vertices $2$ and $4$ with $\gcd = 2$. This is the only possible way to add $1$ edge that will cost $2$.</p><p>In the second test case, there is no way to add $10$ edges, so the answer is $-1$.</p><p>In the third test case, we can add the following edges: </p><ul> <li> $k = 1$: edge of weight $2$ between vertices $2$ and $4$ ($\gcd(2, 4) = 2$). Cost: $2$; </li><li> $k = 1$: edge of weight $2$ between vertices $4$ and $6$ ($\gcd(4, 6) = 2$). Cost: $2$; </li><li> $k = 2$: edges of weight $3$: $(3, 6)$ and $(3, 9)$ ($\gcd(3, 6) = \gcd(3, 9) = 3$). Cost: $3$. </li></ul> As a result, we added $1 + 1 + 2 = 4$ edges with total cost $2 + 2 + 3 = 7$, which is the minimal possible cost.
