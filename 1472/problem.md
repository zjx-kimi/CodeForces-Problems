## Description

<div><p>You are given a rooted tree consisting of $n$ vertices. Vertices are numbered from $1$ to $n$. Any vertex can be the root of a tree.</p><p>A <span class="tex-font-style-it">tree</span> is a connected undirected graph without cycles. A <span class="tex-font-style-it">rooted tree</span> is a tree with a selected vertex, which is called the <span class="tex-font-style-it">root</span>.</p><p>The tree is specified by an array of parents $p$ containing $n$ numbers: $p_i$ is a parent of the vertex with the index $i$. The <span class="tex-font-style-it">parent</span> of a vertex $u$ is a vertex that is the next vertex on the shortest path from $u$ to the root. For example, on the simple path from $5$ to $3$ (the root), the next vertex would be $1$, so the parent of $5$ is $1$.</p><p>The root has no parent, so for it, the value of $p_i$ is $i$ (the root is the only vertex for which $p_i=i$).</p><p>Find such a set of paths that:</p><ul> <li> each vertex belongs to exactly one path, each path can contain one or more vertices; </li><li> in each path each next vertex&nbsp;— is a son of the current vertex (that is, paths always lead down&nbsp;— from parent to son); </li><li> number of paths is <span class="tex-font-style-bf">minimal</span>. </li></ul><p>For example, if $n=5$ and $p=[3, 1, 3, 3, 1]$, then the tree can be divided into three paths: </p><ol> <li> $3 \rightarrow 1 \rightarrow 5$ (path of $3$ vertices), </li><li> $4$ (path of $1$ vertices). </li><li> $2$ (path of $1$ vertices). </li></ol><center> <img class="tex-graphics" src="file://SxG0wYbM.png" style="max-width: 100.0%;max-height: 100.0%;">   <span class="tex-font-size-small">Example of splitting a root tree into three paths for $n=5$, the root of the tree&nbsp;— node $3$.</span> </center></div><div class="input-specification"><p>The first line of input data contains an integer $t$ ($1 \le t \le 10^4$) — the number of test cases in the test.</p><p>Each test case consists of two lines.</p><p>The first of them contains an integer $n$ ($1 \le n \le 2 \cdot 10^5$). It is the number of vertices in the tree.</p><p>The second line contains $n$ integers $p_1, p_2, \dots, p_n$ ($1 \le p_i \le n$). It is guaranteed that the $p$ array encodes some rooted tree.</p><p>It is guaranteed that the sum of the values $n$ over all test cases in the test does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case on the first line, output an integer $m$ — the minimum number of non-intersecting leading down paths that can cover all vertices of the tree.</p><p>Then print $m$ pairs of lines containing path descriptions. In the first of them print the length of the path, in the second — the sequence of vertices specifying that path in the order from top to bottom. You can output the paths in any order.</p><p>If there are several answers, output any of them.</p></div>

## Input

<p>The first line of input data contains an integer $t$ ($1 \le t \le 10^4$) — the number of test cases in the test.</p><p>Each test case consists of two lines.</p><p>The first of them contains an integer $n$ ($1 \le n \le 2 \cdot 10^5$). It is the number of vertices in the tree.</p><p>The second line contains $n$ integers $p_1, p_2, \dots, p_n$ ($1 \le p_i \le n$). It is guaranteed that the $p$ array encodes some rooted tree.</p><p>It is guaranteed that the sum of the values $n$ over all test cases in the test does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case on the first line, output an integer $m$ — the minimum number of non-intersecting leading down paths that can cover all vertices of the tree.</p><p>Then print $m$ pairs of lines containing path descriptions. In the first of them print the length of the path, in the second — the sequence of vertices specifying that path in the order from top to bottom. You can output the paths in any order.</p><p>If there are several answers, output any of them.</p>





```input1|2,3,6,7,10,11
6
5
3 1 3 3 1
4
1 1 4 1
7
1 1 2 3 4 5 6
1
1
6
4 4 4 4 1 2
4
2 2 2 2
```




```output1
3
3
3 1 5
1
2
1
4

2
2
1 2
2
4 3

1
7
1 2 3 4 5 6 7

1
1
1

3
3
4 1 5
2
2 6
1
3

3
2
2 1
1
3
1
4
```


