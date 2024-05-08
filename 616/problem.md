## Description

<div><p>Alice and Bob are playing a game on a graph. They have an undirected graph without self-loops and multiple edges. All vertices of the graph have <span class="tex-font-style-bf">degree equal to $2$</span>. The graph may consist of several components. Note that if such graph has $n$ vertices, it will have exactly $n$ edges.</p><p>Alice and Bob take turn. Alice goes first. In each turn, the player can choose $k$ ($l \le k \le r$; $l &lt; r$) vertices that form <span class="tex-font-style-bf">a connected subgraph</span> and erase these vertices from the graph, including all incident edges.</p><p>The player who can't make a step loses.</p><p>For example, suppose they are playing on the given graph with given $l = 2$ and $r = 3$:</p><center> <img class="tex-graphics" src="file://YrMjem6A.png" style="max-width: 100.0%;max-height: 100.0%;"> </center><p>A valid vertex set for Alice to choose at the first move is one of the following: </p><ul> <li> $\{1, 2\}$ </li><li> $\{1, 3\}$ </li><li> $\{2, 3\}$ </li><li> $\{4, 5\}$ </li><li> $\{4, 6\}$ </li><li> $\{5, 6\}$ </li><li> $\{1, 2, 3\}$ </li><li> $\{4, 5, 6\}$ </li></ul> Suppose, Alice chooses subgraph $\{4, 6\}$.<p>Then a valid vertex set for Bob to choose at the first move is one of the following: </p><ul> <li> $\{1, 2\}$ </li><li> $\{1, 3\}$ </li><li> $\{2, 3\}$ </li><li> $\{1, 2, 3\}$ </li></ul> Suppose, Bob chooses subgraph $\{1, 2, 3\}$.<p>Alice can't make a move, so she loses.</p><p>You are given a graph of size $n$ and integers $l$ and $r$. Who will win if both Alice and Bob play optimally.</p></div><div class="input-specification"><p>The first line contains three integers $n$, $l$ and $r$ ($3 \le n \le 2 \cdot 10^5$; $1 \le l &lt; r \le n$)&nbsp;— the number of vertices in the graph, and the constraints on the number of vertices Alice or Bob can choose in one move.</p><p>Next $n$ lines contains edges of the graph: one edge per line. The $i$-th line contains two integers $u_i$ and $v_i$ ($1 \le u_i, v_i \le n$; $u_i \neq v_i$)&nbsp;— description of the $i$-th edge.</p><p>It's guaranteed that the degree of each vertex of the given graph is equal to $2$.</p></div><div class="output-specification"><p>Print <span class="tex-font-style-tt">Alice</span> (case-insensitive) if Alice wins, or <span class="tex-font-style-tt">Bob</span> otherwise.</p></div>

## Input

<p>The first line contains three integers $n$, $l$ and $r$ ($3 \le n \le 2 \cdot 10^5$; $1 \le l &lt; r \le n$)&nbsp;— the number of vertices in the graph, and the constraints on the number of vertices Alice or Bob can choose in one move.</p><p>Next $n$ lines contains edges of the graph: one edge per line. The $i$-th line contains two integers $u_i$ and $v_i$ ($1 \le u_i, v_i \le n$; $u_i \neq v_i$)&nbsp;— description of the $i$-th edge.</p><p>It's guaranteed that the degree of each vertex of the given graph is equal to $2$.</p>

## Output

<p>Print <span class="tex-font-style-tt">Alice</span> (case-insensitive) if Alice wins, or <span class="tex-font-style-tt">Bob</span> otherwise.</p>





```input1
6 2 3
1 2
2 3
3 1
4 5
5 6
6 4
```




```input2
6 1 2
1 2
2 3
3 1
4 5
5 6
6 4
```




```input3
12 1 3
1 2
2 3
3 1
4 5
5 6
6 7
7 4
8 9
9 10
10 11
11 12
12 8
```




```output1
Bob
```




```output2
Bob
```




```output3
Alice
```



## Note

<p>In the first test the same input as in legend is shown.</p><p>In the second test the same graph as in legend is shown, but with $l = 1$ and $r = 2$.</p>
