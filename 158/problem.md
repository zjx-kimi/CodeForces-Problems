## Description

<div><p>You are given a tree$^{\dagger}$. In one <span class="tex-font-style-it">zelda-operation</span> you can do follows:</p><ul><li> Choose two vertices of the tree $u$ and $v$;</li><li> Compress all the vertices on the path from $u$ to $v$ into one vertex. In other words, all the vertices on path from $u$ to $v$ will be erased from the tree, a new vertex $w$ will be created. Then every vertex $s$ that had an edge to some vertex on the path from $u$ to $v$ will have an edge to the vertex $w$.</li></ul><center> <img class="tex-graphics" src="file://zZb3uOd0.png" style="max-width: 100.0%;max-height: 100.0%;">   <span class="tex-font-size-small">Illustration of a zelda-operation performed for vertices $1$ and $5$.</span> </center><p>Determine the minimum number of zelda-operations required for the tree to have only one vertex.</p><p>$^{\dagger}$A tree is a connected acyclic undirected graph.</p></div><div class="input-specification"><p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 10^4$) — the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2 \le n \le 10^5$) — the number of vertices.</p><p>$i$-th of the next $n − 1$ lines contains two integers $u_i$ and $v_i$ ($1 \le u_i, v_i \le n, u_i \ne v_i$) — the numbers of vertices connected by the $i$-th edge.</p><p>It is guaranteed that the given edges form a tree.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p></div><div class="output-specification"><p>For each test case, output a single integer — the minimum number of zelda-operations required for the tree to have only one vertex.</p></div>

## Input

<p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 10^4$) — the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2 \le n \le 10^5$) — the number of vertices.</p><p>$i$-th of the next $n − 1$ lines contains two integers $u_i$ and $v_i$ ($1 \le u_i, v_i \le n, u_i \ne v_i$) — the numbers of vertices connected by the $i$-th edge.</p><p>It is guaranteed that the given edges form a tree.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p>

## Output

<p>For each test case, output a single integer — the minimum number of zelda-operations required for the tree to have only one vertex.</p>





```input1|2,3,4,5,15,16,17,18,19,20,21
4
4
1 2
1 3
3 4
9
3 1
3 5
3 2
5 6
6 7
7 8
7 9
6 4
7
1 2
1 3
2 4
4 5
3 6
2 7
6
1 2
1 3
1 4
4 5
2 6
```




```output1
1
3
2
2
```



## Note

<p>In the first test case, it's enough to perform one zelda-operation for vertices $2$ and $4$.</p><p>In the second test case, we can perform the following zelda-operations:</p><ol> <li> $u = 2, v = 1$. Let the resulting added vertex be labeled as $w = 10$; </li><li> $u = 4, v = 9$. Let the resulting added vertex be labeled as $w = 11$; </li><li> $u = 8, v = 10$. After this operation, the tree consists of a single vertex. </li></ol>
