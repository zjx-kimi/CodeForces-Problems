## Description

<div><p>Cactus lady loves her cactuses very much. Especially she likes a small cactus named Cing. Cing can be seen as a connected undirected graph in which every vertex lies on at most one simple cycle. Intuitively, a cactus is a generalization of a tree where some cycles are allowed. Multiedges (multiple edges between a pair of vertices) and loops (edges that connect a vertex to itself) are not allowed.</p><p>She bought a special grid for her special little cactus Cing. This grid can be represented as a graph consisting of two paths of length $400\,000$, $u_{(0, -200\,000)} - u_{(0, -199\,999)} - \ldots - u_{(0, 200\,000)}$ and $u_{(1, -200\,000)} - u_{(1, -199\,999)} - \ldots - u_{(1, 200\,000)}$, connected together by $400\,001$ edges $(u_{(0, i)}, u_{(1, i)})$ for each $i$. In other words, a grid can be seen as a ladder.</p><center> <img class="tex-graphics" src="file://W8AYHmQI.png" style="max-width: 100.0%;max-height: 100.0%;" width="265px"> </center><p>Cactus lady wants to know whether she can embed Cing into this grid, i.e., map each vertex of the cactus onto a separate vertex of the grid while each edge of the cactus will be mapped onto some edge of the grid.</p></div><div class="input-specification"><p>The first line contains an integer $t$&nbsp;— the number of test cases.</p><p>Each test case begins with a line containing two integers $n$ and $m$&nbsp;— the number of vertices and the number of edges in a given cactus, respectively ($1 \le n \le 200\,000$; $0 \le m \le 250\,000$).</p><p>Each of the following $m$ lines contains two integers $v$ and $u$, describing the edges of the cactus ($1 \le v, u \le n, u \ne v$).</p><p>The total sum of all $n$ in the input doesn't exceed $200\,000$.</p></div><div class="output-specification"><p>Print an answer for each test case in the same order the cases appear in the input.</p><p>For each test case print "<span class="tex-font-style-tt">No</span>" in the first line, if no layout exists.</p><p>Otherwise print "<span class="tex-font-style-tt">Yes</span>" in the first line, and the following $n$ lines describing the layout. The $i$-th of these $n$ lines should contain two integers $x_i$ and $y_i$, the location of the $i$-th vertex ($0 \le x_i \le 1$; $-200\,000 \le y_i \le 200\,000$).</p></div>

## Input

<p>The first line contains an integer $t$&nbsp;— the number of test cases.</p><p>Each test case begins with a line containing two integers $n$ and $m$&nbsp;— the number of vertices and the number of edges in a given cactus, respectively ($1 \le n \le 200\,000$; $0 \le m \le 250\,000$).</p><p>Each of the following $m$ lines contains two integers $v$ and $u$, describing the edges of the cactus ($1 \le v, u \le n, u \ne v$).</p><p>The total sum of all $n$ in the input doesn't exceed $200\,000$.</p>

## Output

<p>Print an answer for each test case in the same order the cases appear in the input.</p><p>For each test case print "<span class="tex-font-style-tt">No</span>" in the first line, if no layout exists.</p><p>Otherwise print "<span class="tex-font-style-tt">Yes</span>" in the first line, and the following $n$ lines describing the layout. The $i$-th of these $n$ lines should contain two integers $x_i$ and $y_i$, the location of the $i$-th vertex ($0 \le x_i \le 1$; $-200\,000 \le y_i \le 200\,000$).</p>





```input1
5
4 3
1 2
2 3
3 4

8 7
1 2
3 2
2 4
4 5
4 6
6 7
6 8

5 4
1 2
1 3
1 4
1 5

8 9
1 2
2 3
3 4
1 4
4 5
5 6
6 7
7 8
5 8

10 10
1 2
2 3
3 4
4 5
5 6
6 1
3 7
4 8
1 9
6 10
```




```output1
Yes
0 0
0 1
1 1
1 2
Yes
0 3
1 3
1 4
1 2
0 2
1 1
0 1
1 0
No
Yes
0 0
1 0
1 1
0 1
0 2
0 3
1 3
1 2
Yes
1 1
1 2
1 3
0 3
0 2
0 1
1 4
0 4
1 0
0 0
```



## Note

<p>Empty lines between test cases are for clarity. In real test cases there are no empty lines.</p><p>In these notes, we consider the embeddings for tests 2 and 4.</p><p>We start with the embedding for test 2.</p><center> <img class="tex-graphics" src="file://NF7aAR7m.png" style="max-width: 100.0%;max-height: 100.0%;" width="189px"> </center><p>Here goes the embedding for test 4.</p><center> <img class="tex-graphics" src="file://oEQu9sp2.png" style="max-width: 100.0%;max-height: 100.0%;" width="189px"> </center>
