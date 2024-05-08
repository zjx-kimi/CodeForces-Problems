## Description

<div><p>You are given an undirected connected graph on $n$ vertices. Each edge of this graph has a weight; the weight of the edge connecting vertices $i$ and $j$ is $w_{i,j}$ (or $w_{i,j} = 0$ if there is no edge between $i$ and $j$). All weights are positive integers.</p><p>You are also given a positive integer $c$.</p><p>You have to build a spanning tree of this graph; i. e. choose exactly $(n-1)$ edges of this graph in such a way that every vertex can be reached from every other vertex by traversing some of the chosen edges. The cost of the spanning tree is the sum of two values:</p><ul> <li> the sum of weights of all chosen edges; </li><li> the maximum matching in the spanning tree (i. e. the maximum size of a set of edges such that they all belong to the chosen spanning tree, and no vertex has more than one incident edge in this set), multiplied by the given integer $c$. </li></ul><p>Find any spanning tree with the minimum cost. Since the graph is connected, there exists at least one spanning tree.</p></div><div class="input-specification"><p>The first line contains two integers $n$ and $c$ ($2 \le n \le 20$; $1 \le c \le 10^6$).</p><p>Then $n$ lines follow. The $i$-th of them contains $n$ integers $w_{i,1}, w_{i,2}, \dots, w_{i,n}$ ($0 \le w_{i,j} \le 10^6$), where $w_{i,j}$ denotes the weight of the edge between $i$ and $j$ (or $w_{i,j} = 0$ if there is no such edge).</p><p>Additional constraints on the input:</p><ul> <li> for every $i \in [1, n]$, $w_{i,i} = 0$; </li><li> for every pair of integers $(i, j)$ such that $i \in [1, n]$ and $j \in [1, n]$, $w_{i,j} = w_{j,i}$; </li><li> the given graph is connected. </li></ul></div><div class="output-specification"><p>Print one integer — the minimum cost of a spanning tree of the given graph.</p></div>

## Input

<p>The first line contains two integers $n$ and $c$ ($2 \le n \le 20$; $1 \le c \le 10^6$).</p><p>Then $n$ lines follow. The $i$-th of them contains $n$ integers $w_{i,1}, w_{i,2}, \dots, w_{i,n}$ ($0 \le w_{i,j} \le 10^6$), where $w_{i,j}$ denotes the weight of the edge between $i$ and $j$ (or $w_{i,j} = 0$ if there is no such edge).</p><p>Additional constraints on the input:</p><ul> <li> for every $i \in [1, n]$, $w_{i,i} = 0$; </li><li> for every pair of integers $(i, j)$ such that $i \in [1, n]$ and $j \in [1, n]$, $w_{i,j} = w_{j,i}$; </li><li> the given graph is connected. </li></ul>

## Output

<p>Print one integer — the minimum cost of a spanning tree of the given graph.</p>





```input1|
4 10
0 1 8 0
1 0 1 0
8 1 0 2
0 0 2 0
```




```input2|
4 5
0 1 8 0
1 0 1 0
8 1 0 2
0 0 2 0
```




```output1
21
```




```output2
14
```



## Note

<p>In the first example, the minimum cost spanning tree consists of edges $(1, 3)$, $(2, 3)$ and $(3, 4)$. The maximum matching for it is $1$.</p><p>In the second example, the minimum cost spanning tree consists of edges $(1, 2)$, $(2, 3)$ and $(3, 4)$. The maximum matching for it is $2$.</p>
