## Description

<div><p>Given a tree consisting of $n$ vertices. A tree is a connected undirected graph without cycles. Each edge of the tree has its weight, $w_i$.</p><p>Your task is to count the number of different graphs that satisfy all four conditions:</p><ol> <li> The graph does not have self-loops and multiple edges. </li><li> The weights on the edges of the graph are integers and do not exceed $S$. </li><li> The graph has <span class="tex-font-style-bf">exactly one</span> <a href="http://tiny.cc/30g9vz">minimum spanning tree</a>. </li><li> The minimum spanning tree of the graph is the given tree. </li></ol><p>Two graphs are considered different if their sets of edges are different, taking into account the weights of the edges.</p><p>The answer can be large, output it modulo $998244353$.</p></div><div class="input-specification"><p>The first line contains an integer $t$ ($1\le t\le 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains two integers $n$ and $S$ ($2 \le n \le 2 \cdot 10^5, 1\le S\le 10^9$)&nbsp;— the number of vertices and the upper bound of the weights.</p><p>Then follow $n-1$ lines describing the tree, the $i$-th line contains three integers $u_i$, $v_i$, and $w_i$ ($1\le u_i,v_i\le n, u_i \ne v_i, 1\le w_i\le S$)&nbsp;— an edge in the tree with weight $w_i$.</p><p>It is guaranteed that the sum of $n$ for all tests does not exceed $2\cdot 10^5$.</p></div><div class="output-specification"><p>For each test, output the number of different graphs that satisfy the conditions, modulo $998244353$.</p></div>

## Input

<p>The first line contains an integer $t$ ($1\le t\le 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains two integers $n$ and $S$ ($2 \le n \le 2 \cdot 10^5, 1\le S\le 10^9$)&nbsp;— the number of vertices and the upper bound of the weights.</p><p>Then follow $n-1$ lines describing the tree, the $i$-th line contains three integers $u_i$, $v_i$, and $w_i$ ($1\le u_i,v_i\le n, u_i \ne v_i, 1\le w_i\le S$)&nbsp;— an edge in the tree with weight $w_i$.</p><p>It is guaranteed that the sum of $n$ for all tests does not exceed $2\cdot 10^5$.</p>

## Output

<p>For each test, output the number of different graphs that satisfy the conditions, modulo $998244353$.</p>





```input1|2,3,8,9,10,11,12
4
2 5
1 2 4
4 5
1 2 2
2 3 4
3 4 3
5 6
1 2 3
1 3 2
3 4 6
3 5 1
10 200
1 2 3
2 3 33
3 4 200
1 5 132
5 6 1
5 7 29
7 8 187
7 9 20
7 10 4
```




```output1
1
8
80
650867886
```



## Note

<p>In the first sample, there is only one graph, which is the given tree.</p><p>In the second samle, the given tree looks like this: </p><center> <img class="tex-graphics" src="file://FUBYPKk7.png" style="max-width: 100.0%;max-height: 100.0%;">   </center> All possible graphs for the second sample are shown below, the minimum spanning tree is highlighted in red:<center> <img class="tex-graphics" src="file://XfeEI7Kf.png" style="max-width: 100.0%;max-height: 100.0%;">   </center>
