## Description

<div><p>A <span class="tex-font-style-it">snowflake</span> graph is generated from two integers $x$ and $y$, both greater than $1$, as follows: </p><ul> <li> Start with one central vertex. </li><li> Connect $x$ new vertices to this central vertex. </li><li> Connect $y$ new vertices to <span class="tex-font-style-bf">each</span> of these $x$ vertices. </li></ul> For example, below is a snowflake graph for $x=5$ and $y=3$. <center> <img class="tex-graphics" src="file://sV85kret.png" style="max-width: 100.0%;max-height: 100.0%;"><p><span class="tex-font-size-small">The snowflake graph above has a central vertex $15$, then $x=5$ vertices attached to it ($3$, $6$, $7$, $8$, and $20$), and then $y=3$ vertices attached to each of those.</span> </p></center> Given a snowflake graph, determine the values of $x$ and $y$.</div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \leq t \leq 1000$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains two integers $n$ and $m$ ($2 \leq n \leq 200$; $1 \leq m \leq \min\left(1000, \frac{n(n-1)}{2}\right)$)&nbsp;— the number of vertices and edges in the graph, respectively.</p><p>The next $m$ lines each contain two integers each $u$ and $v$ ($1 \leq u, v \leq n$, $u \neq v$)&nbsp;— the numbers of vertices connected by an edge. The graph does not contain multiple edges and self-loops.</p><p><span class="tex-font-style-bf">It is guaranteed that this graph is a snowflake graph for some integers $x$ and $y$ both greater than $1$.</span></p></div><div class="output-specification"><p>For each test case, on a separate line output the values of $x$ and $y$, in that order, separated by a space.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \leq t \leq 1000$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains two integers $n$ and $m$ ($2 \leq n \leq 200$; $1 \leq m \leq \min\left(1000, \frac{n(n-1)}{2}\right)$)&nbsp;— the number of vertices and edges in the graph, respectively.</p><p>The next $m$ lines each contain two integers each $u$ and $v$ ($1 \leq u, v \leq n$, $u \neq v$)&nbsp;— the numbers of vertices connected by an edge. The graph does not contain multiple edges and self-loops.</p><p><span class="tex-font-style-bf">It is guaranteed that this graph is a snowflake graph for some integers $x$ and $y$ both greater than $1$.</span></p>

## Output

<p>For each test case, on a separate line output the values of $x$ and $y$, in that order, separated by a space.</p>





```input1|2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22,30,31,32,33,34,35,36,37,38
3
21 20
21 20
5 20
13 20
1 3
11 3
10 3
4 8
19 8
14 8
9 7
12 7
17 7
18 6
16 6
2 6
6 15
7 15
8 15
20 15
3 15
7 6
1 2
1 3
2 4
2 5
3 6
3 7
9 8
9 3
3 6
6 2
2 1
5 2
2 7
4 3
3 8
```




```output1
5 3
2 2
2 3
```



## Note

<p>The first test case is pictured in the statement. Note that the output <span class="tex-font-style-tt">3 5</span> is <span class="tex-font-style-bf">incorrect</span>, since $x$ should be output before $y$.</p>
