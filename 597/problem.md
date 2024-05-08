## Description

<div><p>You are given a tree (an undirected connected acyclic graph) which initially only contains vertex $1$. There will be several queries to the given tree. In the $i$-th query, vertex $i + 1$ will appear and be connected to vertex $p_i$ ($1 \le p_i \le i$). </p><p>After each query, please find out the least number of operations required to make the current tree has <span class="tex-font-style-bf">two</span> centroids. In one operation, you can add <span class="tex-font-style-bf">one</span> vertex and <span class="tex-font-style-bf">one</span> edge to the tree such that it remains a tree.</p><p>A vertex is called a centroid if its removal splits the tree into subtrees with at most $\lfloor \frac{n}{2} \rfloor$ vertices each, with $n$ as the number of vertices of the tree. For example, the centroid of the following tree is $3$ because the biggest subtree after removing the centroid has $2$ vertices.</p><center> <img class="tex-graphics" src="file://2JoGds8T.png" style="max-width: 100.0%;max-height: 100.0%;"> </center><p>In the next tree, vertex $1$ and $2$ are both centroids.</p><center> <img class="tex-graphics" src="file://Uo3KqWNR.png" style="max-width: 100.0%;max-height: 100.0%;"> </center></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^4$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2 \le n \le 5 \cdot 10^{5}$)&nbsp;— the number of nodes of the final tree.</p><p>The second line of each test case contains $n - 1$ integers $p_1, p_2, \ldots, p_{n - 1}$ ($1 \le p_i \le i$)&nbsp;— the index of the vertex that is connected to vertex $i + 1$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $5 \cdot 10^{5}$.</p></div><div class="output-specification"><p>For each test case, output $n - 1$ integers. The $i$-th integer is the answer to the $i$-th query&nbsp;— the least number of operations required to make the current tree have two centroids.</p><p>We can show that an answer always exists.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^4$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2 \le n \le 5 \cdot 10^{5}$)&nbsp;— the number of nodes of the final tree.</p><p>The second line of each test case contains $n - 1$ integers $p_1, p_2, \ldots, p_{n - 1}$ ($1 \le p_i \le i$)&nbsp;— the index of the vertex that is connected to vertex $i + 1$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $5 \cdot 10^{5}$.</p>

## Output

<p>For each test case, output $n - 1$ integers. The $i$-th integer is the answer to the $i$-th query&nbsp;— the least number of operations required to make the current tree have two centroids.</p><p>We can show that an answer always exists.</p>





```input1|2,3,6,7,10,11
5
2
1
3
1 1
4
1 2 3
7
1 2 3 2 5 2
10
1 2 2 4 5 5 7 8 9
```




```output1
0
0 1
0 1 0
0 1 0 1 2 3
0 1 2 1 0 1 0 1 2
```



## Note

<p>The illustrations below are of the fourth example test case.</p><p>After the third query: </p><center> <img class="tex-graphics" src="file://l48gA29F.png" style="max-width: 100.0%;max-height: 100.0%;"> </center> The tree already has vertices $2$ and $3$ as centroids, so no operations are needed.<p>After the fourth query: </p><center> <img class="tex-graphics" src="file://euVyB2fV.png" style="max-width: 100.0%;max-height: 100.0%;"> </center> Adding vertex $x$ to the tree makes vertices $2$ and $3$ centroids. Only one operation is needed.<p>After the fifth query: </p><center> <img class="tex-graphics" src="file://KChDQsir.png" style="max-width: 100.0%;max-height: 100.0%;"> </center> Adding vertex $x$ and $y$ to the tree makes vertices $5$ and $2$ centroids. Two operations are needed.<p>After the sixth query: </p><center> <img class="tex-graphics" src="file://1rkGi1d9.png" style="max-width: 100.0%;max-height: 100.0%;"> </center> Adding vertex $x$, $y$, and $z$ to the tree makes vertices $5$ and $2$ centroids. Three operations are needed.
