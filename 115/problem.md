## Description

<div><p>You are given a tree consisting of $n$ vertices. Some vertices of the tree are red, all other vertices are blue.</p><p>Each edge of the tree has a positive weight. Let's define $d(x, y)$ as the distance between the vertices $x$ and $y$, i. e. the sum of weights of edges belonging to the simple path between $x$ and $y$.</p><p>For each vertex, you have to choose an integer $v_i$. These integers should meet the following constraint: for every blue vertex $b$ and every red vertex $r$, $d(b, r) \ge v_b + v_r$. </p><p>You have to maximize the value of $\sum \limits_{i=1}^{n} v_i$.</p><p><span class="tex-font-style-bf">Note that the values of $v_i$ are not necessarily positive</span>.</p></div><div class="input-specification"><p>The first line contains one integer $n$ ($2 \le n \le 3 \cdot 10^5$).</p><p>The second line contains $n$ integers $c_1, c_2, \dots, c_n$ ($0 \le c_i \le 1$). If the $i$-th vertex is red, $c_i = 1$, otherwise $c_i = 0$.</p><p>Then $n-1$ lines follow. Each line contains three integers $x_i$, $y_i$ and $w_i$ ($1 \le x_i, y_i \le n$; $1 \le w_i \le 10^6$; $x_i \ne y_i$) denoting an edge between the vertices $x_i$ and $y_i$ which has weight $w_i$. These edges form a tree.</p></div><div class="output-specification"><p>If the value of $\sum \limits_{i=1}^{n} v_i$ can be as big as possible, print <span class="tex-font-style-tt">Infinity</span>. Otherwise, print one integer — the maximum possible value of $\sum \limits_{i=1}^{n} v_i$ you can get.</p></div>

## Input

<p>The first line contains one integer $n$ ($2 \le n \le 3 \cdot 10^5$).</p><p>The second line contains $n$ integers $c_1, c_2, \dots, c_n$ ($0 \le c_i \le 1$). If the $i$-th vertex is red, $c_i = 1$, otherwise $c_i = 0$.</p><p>Then $n-1$ lines follow. Each line contains three integers $x_i$, $y_i$ and $w_i$ ($1 \le x_i, y_i \le n$; $1 \le w_i \le 10^6$; $x_i \ne y_i$) denoting an edge between the vertices $x_i$ and $y_i$ which has weight $w_i$. These edges form a tree.</p>

## Output

<p>If the value of $\sum \limits_{i=1}^{n} v_i$ can be as big as possible, print <span class="tex-font-style-tt">Infinity</span>. Otherwise, print one integer — the maximum possible value of $\sum \limits_{i=1}^{n} v_i$ you can get.</p>





```input1
4
1 1 0 0
3 4 50
3 2 100
2 1 100
```




```input2
6
0 1 0 1 0 1
1 2 1
1 4 1
1 6 1
6 5 100
6 3 100
```




```input3
3
1 1 1
1 2 100
2 3 100
```




```output1
350
```




```output2
203
```




```output3
Infinity
```



## Note

<p>In the first example, you can assign $v_1 = 120, v_2 = 20, v_3 = 80, v_4 = 130$.</p>
