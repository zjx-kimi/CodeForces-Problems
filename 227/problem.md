## Description

<div><p>You are given a rooted tree with the root at vertex $1$, initially consisting of a single vertex. Each vertex has a numerical value, initially set to $0$. There are also $q$ queries of two types: </p><ul> <li> The first type: add a child vertex with the number $sz + 1$ to vertex $v$, where $sz$ is the current size of the tree. The numerical value of the new vertex will be $0$. </li><li> The second type: add $x$ to the numerical values of all vertices in the subtree of vertex $v$. </li></ul><p>After all queries, output the numerical value of all of the vertices in the final tree.</p></div><div class="input-specification"><p>The first line contains a single integer $T$ ($1 \leq T \leq 10^4$) — the number of test cases. The descriptions of the test cases follow.</p><p>The first line of each test case contains a single integer $q$ ($1 \leq q \leq 5 \cdot 10^5$) — the number of queries.</p><p>The following $q$ lines can fall into two cases: </p><ul> <li> The first type of query: The $i$-th line contains two integers $t_i$ ($t_i = 1$), $v_i$. You need to add a child with the number $sz + 1$ to vertex $v_i$, where $sz$ is the current size of the tree. It is guaranteed that $1 \leq v_i \leq sz$. </li><li> The second type of query: The $i$-th line contains three integers $t_i$ ($t_i = 2$), $v_i$, $x_i$ ($-10^9 \leq x_i \leq 10^9$). You need to add $x_i$ to all numerical values of vertices in the subtree of $v_i$. It is guaranteed that $1 \leq v_i \leq sz$, where $sz$ is the current size of the tree. </li></ul><p>It is guaranteed that the sum of $q$ across all test cases does not exceed $5 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output the numerical value of each vertex of the final tree after all queries have been performed.</p></div>

## Input

<p>The first line contains a single integer $T$ ($1 \leq T \leq 10^4$) — the number of test cases. The descriptions of the test cases follow.</p><p>The first line of each test case contains a single integer $q$ ($1 \leq q \leq 5 \cdot 10^5$) — the number of queries.</p><p>The following $q$ lines can fall into two cases: </p><ul> <li> The first type of query: The $i$-th line contains two integers $t_i$ ($t_i = 1$), $v_i$. You need to add a child with the number $sz + 1$ to vertex $v_i$, where $sz$ is the current size of the tree. It is guaranteed that $1 \leq v_i \leq sz$. </li><li> The second type of query: The $i$-th line contains three integers $t_i$ ($t_i = 2$), $v_i$, $x_i$ ($-10^9 \leq x_i \leq 10^9$). You need to add $x_i$ to all numerical values of vertices in the subtree of $v_i$. It is guaranteed that $1 \leq v_i \leq sz$, where $sz$ is the current size of the tree. </li></ul><p>It is guaranteed that the sum of $q$ across all test cases does not exceed $5 \cdot 10^5$.</p>

## Output

<p>For each test case, output the numerical value of each vertex of the final tree after all queries have been performed.</p>





```input1|2,3,4,5,6,7,8,9,10,11,18,19,20,21,22,23
3
9
2 1 3
1 1
2 2 1
1 1
2 3 2
1 3
2 1 4
1 3
2 3 2
5
2 1 1
1 1
2 1 -1
1 1
2 1 1
5
1 1
1 1
2 1 1
2 1 3
2 2 10
```




```output1
7 5 8 6 2 
1 0 1 
4 14 4
```



## Note

<p>In the first case, the final tree with the assigned numerical values will look like this: </p><center> <img class="tex-graphics" src="file://37avgwo8.png" style="max-width: 100.0%;max-height: 100.0%;">   <span class="tex-font-size-small">The final tree with the assigned numerical values</span> </center>
