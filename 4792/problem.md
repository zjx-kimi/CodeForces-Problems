## Description

<div><p>Vasya has got a tree consisting of $n$ vertices. He wants to delete some (possibly zero) edges in this tree such that the maximum matching in the resulting graph is unique. He asks you to calculate the number of ways to choose a set of edges to remove.</p><p>A matching in the graph is a subset of its edges such that there is no vertex incident to two (or more) edges from the subset. A maximum matching is a matching such that the number of edges in the subset is maximum possible among all matchings in this graph.</p><p>Since the answer may be large, output it modulo $998244353$.</p></div><div class="input-specification"><p>The first line contains one integer $n$ ($1 \le n \le 3 \cdot 10^5$) — the number of vertices in the tree.</p><p>Each of the next $n − 1$ lines contains two integers $u$ and $v$ ($1 \le u, v \le n, u \neq v$) denoting an edge between vertex $u$ and vertex $v$. It is guaranteed that these edges form a tree.</p></div><div class="output-specification"><p>Print one integer — the number of ways to delete some (possibly empty) subset of edges so that the maximum matching in the resulting graph is unique. Print the answer modulo $998244353$.</p></div>

## Input

<p>The first line contains one integer $n$ ($1 \le n \le 3 \cdot 10^5$) — the number of vertices in the tree.</p><p>Each of the next $n − 1$ lines contains two integers $u$ and $v$ ($1 \le u, v \le n, u \neq v$) denoting an edge between vertex $u$ and vertex $v$. It is guaranteed that these edges form a tree.</p>

## Output

<p>Print one integer — the number of ways to delete some (possibly empty) subset of edges so that the maximum matching in the resulting graph is unique. Print the answer modulo $998244353$.</p>





```input1
4
1 2
1 3
1 4

```




```input2
4
1 2
2 3
3 4

```




```input3
1

```




```output1
4

```




```output2
6

```




```output3
1

```



## Note

<p>Possible ways to delete edges in the first example: </p><ul> <li> delete $(1, 2)$ and $(1, 3)$. </li><li> delete $(1, 2)$ and $(1, 4)$. </li><li> delete $(1, 3)$ and $(1, 4)$. </li><li> delete all edges. </li></ul><p>Possible ways to delete edges in the second example: </p><ul> <li> delete no edges. </li><li> delete $(1, 2)$ and $(2, 3)$. </li><li> delete $(1, 2)$ and $(3, 4)$. </li><li> delete $(2, 3)$ and $(3, 4)$. </li><li> delete $(2, 3)$. </li><li> delete all edges. </li></ul>
