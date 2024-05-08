## Description

<div><p>You are given a tree consisting of $n$ vertices. There is an integer written on each vertex; the $i$-th vertex has integer $a_i$ written on it.</p><p>You have to process $q$ queries. The $i$-th query consists of three integers $x_i$, $y_i$ and $k_i$. For this query, you have to answer if it is possible to choose a set of vertices $v_1, v_2, \dots, v_m$ (possibly empty) such that:</p><ul> <li> every vertex $v_j$ is on the simple path between $x_i$ and $y_i$ (endpoints can be used as well); </li><li> $a_{v_1} \oplus a_{v_2} \oplus \dots \oplus a_{v_m} = k_i$, where $\oplus$ denotes the bitwise XOR operator. </li></ul></div><div class="input-specification"><p>The first line contains one integer $n$ ($2 \le n \le 2 \cdot 10^5$).</p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($0 \le a_i \le 2^{20} - 1$).</p><p>Then $n-1$ lines follow. Each of them contains two integers $u$ and $v$ ($1 \le u, v \le n$; $u \ne v$) denoting an edge of the tree.</p><p>The next line contains one integer $q$ ($1 \le q \le 2 \cdot 10^5$) — the number of queries.</p><p>Then $q$ lines follow. The $i$-th of them contains three integers $x_i$, $y_i$ and $k_i$ ($1 \le x_i, y_i \le n$; $0 \le k_i \le 2^{20} - 1$).</p></div><div class="output-specification"><p>For each query, print <span class="tex-font-style-tt">YES</span> if it is possible to form a set of vertices meeting the constraints. Otherwise, print <span class="tex-font-style-tt">NO</span>.</p><p>You can print each letter in any case.</p></div>

## Input

<p>The first line contains one integer $n$ ($2 \le n \le 2 \cdot 10^5$).</p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($0 \le a_i \le 2^{20} - 1$).</p><p>Then $n-1$ lines follow. Each of them contains two integers $u$ and $v$ ($1 \le u, v \le n$; $u \ne v$) denoting an edge of the tree.</p><p>The next line contains one integer $q$ ($1 \le q \le 2 \cdot 10^5$) — the number of queries.</p><p>Then $q$ lines follow. The $i$-th of them contains three integers $x_i$, $y_i$ and $k_i$ ($1 \le x_i, y_i \le n$; $0 \le k_i \le 2^{20} - 1$).</p>

## Output

<p>For each query, print <span class="tex-font-style-tt">YES</span> if it is possible to form a set of vertices meeting the constraints. Otherwise, print <span class="tex-font-style-tt">NO</span>.</p><p>You can print each letter in any case.</p>





```input1|
4
0 1 2 10
2 1
3 2
4 2
8
3 3 0
3 4 1
3 4 7
1 3 1
1 3 2
1 3 10
1 4 10
1 4 11
```




```output1
YES
YES
NO
YES
YES
NO
YES
YES
```


