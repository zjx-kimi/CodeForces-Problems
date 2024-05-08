## Description

<div><p>You are given a <span class="tex-font-style-bf">directed</span> graph $G$ with $n$ vertices and $m$ edges between them.</p><p>Initially, graph $H$ is the same as graph $G$. Then you decided to perform the following actions: </p><ul> <li> If there exists a triple of vertices $a$, $b$, $c$ of $H$, such that there is an edge from $a$ to $b$ and an edge from $b$ to $c$, but there is no edge from $a$ to $c$, add an edge from $a$ to $c$. </li><li> Repeat the previous step as long as there are such triples. </li></ul><p>Note that the number of edges in $H$ can be up to $n^2$ after performing the actions.</p><p>You also wrote some values on vertices of graph $H$. More precisely, vertex $i$ has the value of $a_i$ written on it.</p><p>Consider a simple path consisting of $k$ <span class="tex-font-style-bf">distinct</span> vertices with indexes $v_1, v_2, \ldots, v_k$. The length of such a path is $k$. The value of that path is defined as $\sum_{i = 1}^k a_{v_i}$.</p><p>A simple path is considered the longest if there is no other simple path in the graph with greater length.</p><p>Among all the longest simple paths in $H$, find the one with the smallest value.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^4$). The description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $m$ ($1 \le n,m \le 2 \cdot 10^5$)&nbsp;— the number of vertices and the number of edges.</p><p>The second line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($0 \le a_i \le 10^9$)&nbsp;— the numbers written on the vertices of graph $H$.</p><p>The $i$-th of the next $m$ lines contains two integers $v_i$ and $u_i$ ($1 \le v_i, u_i \le n$)&nbsp;— meaning that there is an edge going from vertex $v_i$ to vertex $u_i$ in graph $G$. Note that edges are directed. Also note that the graph <span class="tex-font-style-bf">may have</span> self-loops and multiple edges.</p><p>It is guaranteed that neither the sum of $n$ nor the sum of $m$ over all test cases exceeds $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output two numbers&nbsp;— the length of the longest simple path in $H$ and the minimal possible value of such path.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^4$). The description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $m$ ($1 \le n,m \le 2 \cdot 10^5$)&nbsp;— the number of vertices and the number of edges.</p><p>The second line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($0 \le a_i \le 10^9$)&nbsp;— the numbers written on the vertices of graph $H$.</p><p>The $i$-th of the next $m$ lines contains two integers $v_i$ and $u_i$ ($1 \le v_i, u_i \le n$)&nbsp;— meaning that there is an edge going from vertex $v_i$ to vertex $u_i$ in graph $G$. Note that edges are directed. Also note that the graph <span class="tex-font-style-bf">may have</span> self-loops and multiple edges.</p><p>It is guaranteed that neither the sum of $n$ nor the sum of $m$ over all test cases exceeds $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output two numbers&nbsp;— the length of the longest simple path in $H$ and the minimal possible value of such path.</p>





```input1|2,3,4,5,6,7,8,9,19,20,21,22,23,24,25,26,27,28,29,30,31,32,33,34,35,36,37,38,39,40,41,42
3
5 6
2 2 4 1 3
1 2
1 3
2 4
3 4
4 5
5 2
7 7
999999999 999999999 999999999 999999999 1000000000 999999999 1000000000
1 2
2 3
3 4
4 1
4 5
4 6
6 7
14 22
2 3 5 7 3 4 1 4 3 4 2 2 5 1
1 2
2 3
2 4
3 1
4 4
4 5
5 6
5 6
5 12
6 7
6 8
7 5
7 7
7 9
8 4
9 11
10 9
11 10
11 10
12 13
13 14
14 12
```




```output1
5 12
6 5999999995
11 37
```



## Note

<p>In the first test case, the longest path in both graphs is $1 \to 3 \to 4 \to 5 \to 2$. As the path includes all vertices, the minimal possible value of the longest path is the sum of values on all vertices, which is $12$.</p><p>In the second test case, the longest possible path is $1 \to 2 \to 3 \to 4 \to 6 \to 7$. As there are no longest paths with vertex $5$ in them, this path has the minimal possible value of $5\,999\,999\,995$.</p><p>In the third test case, it can be proven that there is no path longer than $11$ and that the value of the longest path cannot be less than $37$. Also, notice that the given graph has both self-loops and multiple edges.</p>
