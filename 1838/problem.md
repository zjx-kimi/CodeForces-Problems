## Description

<div><p>You are given a rooted tree consisting of $n$ vertices numbered from $1$ to $n$. The root of the tree is the vertex $1$.</p><p>You have to color all vertices of the tree into $n$ colors (also numbered from $1$ to $n$) so that there is exactly one vertex for each color. Let $c_i$ be the color of vertex $i$, and $p_i$ be the parent of vertex $i$ in the rooted tree. The coloring is considered beautiful if there is no vertex $k$ ($k &gt; 1$) such that $c_k = c_{p_k} - 1$, i. e. no vertex such that its color is less than the color of its parent by <span class="tex-font-style-bf">exactly $1$</span>.</p><p>Calculate the number of beautiful colorings, and print it modulo $998244353$.</p></div><div class="input-specification"><p>The first line contains one integer $n$ ($2 \le n \le 250000$) — the number of vertices in the tree.</p><p>Then $n-1$ lines follow, the $i$-th line contains two integers $x_i$ and $y_i$ ($1 \le x_i, y_i \le n$; $x_i \ne y_i$) denoting an edge between the vertex $x_i$ and the vertex $y_i$. These edges form a tree.</p></div><div class="output-specification"><p>Print one integer — the number of beautiful colorings, taken modulo $998244353$.</p></div>

## Input

<p>The first line contains one integer $n$ ($2 \le n \le 250000$) — the number of vertices in the tree.</p><p>Then $n-1$ lines follow, the $i$-th line contains two integers $x_i$ and $y_i$ ($1 \le x_i, y_i \le n$; $x_i \ne y_i$) denoting an edge between the vertex $x_i$ and the vertex $y_i$. These edges form a tree.</p>

## Output

<p>Print one integer — the number of beautiful colorings, taken modulo $998244353$.</p>





```input1
5
1 2
3 2
4 2
2 5
```




```input2
5
1 2
2 3
3 4
4 5
```




```input3
20
20 19
20 4
12 4
5 8
1 2
20 7
3 10
7 18
11 8
9 10
17 10
1 15
11 16
14 11
18 10
10 1
14 2
13 17
20 6
```




```output1
42
```




```output2
53
```




```output3
955085064
```


