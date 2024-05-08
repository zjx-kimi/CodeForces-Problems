## Description

<div><p>There is a city park represented as a tree with $n$ attractions as its vertices and $n - 1$ rails as its edges. The $i$-th attraction has happiness value $a_i$.</p><p>Each rail has a color. It is either black if $t_i = 0$, or white if $t_i = 1$. Black trains only operate on a black rail track, and white trains only operate on a white rail track. If you are previously on a black train and want to ride a white train, or you are previously on a white train and want to ride a black train, you need to use $1$ ticket.</p><p>The path of a tour must be a simple path — it must not visit an attraction more than once. You do not need a ticket the first time you board a train. You only have $k$ tickets, meaning <span class="tex-font-style-bf">you can only switch train types at most $k$ times</span>. In particular, you do not need a ticket to go through a path consisting of one rail color.</p><p>Define $f(u, v)$ as the sum of happiness values of the attractions in the tour $(u, v)$, which is a simple path that starts at the $u$-th attraction and ends at the $v$-th attraction. Find the sum of $f(u,v)$ for all valid tours $(u, v)$ ($1 \leq u \leq v \leq n$) that does not need more than $k$ tickets, modulo $10^9 + 7$.</p></div><div class="input-specification"><p>The first line contains two integers $n$ and $k$ ($2 \leq n \leq 2 \cdot 10^5$, $0 \leq k \leq n-1$) — the number of attractions in the city park and the number of tickets you have.</p><p>The second line contains $n$ integers $a_1, a_2,\ldots, a_n$ ($0 \leq a_i \leq 10^9$) — the happiness value of each attraction.</p><p>The $i$-th of the next $n - 1$ lines contains three integers $u_i$, $v_i$, and $t_i$ ($1 \leq u_i, v_i \leq n$, $0 \leq t_i \leq 1$) — an edge between vertices $u_i$ and $v_i$ with color $t_i$. The given edges form a tree.</p></div><div class="output-specification"><p>Output an integer denoting the total happiness value for all valid tours $(u, v)$ ($1 \leq u \leq v \leq n$), modulo $10^9 + 7$.</p></div>

## Input

<p>The first line contains two integers $n$ and $k$ ($2 \leq n \leq 2 \cdot 10^5$, $0 \leq k \leq n-1$) — the number of attractions in the city park and the number of tickets you have.</p><p>The second line contains $n$ integers $a_1, a_2,\ldots, a_n$ ($0 \leq a_i \leq 10^9$) — the happiness value of each attraction.</p><p>The $i$-th of the next $n - 1$ lines contains three integers $u_i$, $v_i$, and $t_i$ ($1 \leq u_i, v_i \leq n$, $0 \leq t_i \leq 1$) — an edge between vertices $u_i$ and $v_i$ with color $t_i$. The given edges form a tree.</p>

## Output

<p>Output an integer denoting the total happiness value for all valid tours $(u, v)$ ($1 \leq u \leq v \leq n$), modulo $10^9 + 7$.</p>





```input1
5 0
1 3 2 6 4
1 2 1
1 4 0
3 2 1
2 5 0
```




```input2
3 1
1 1 1
1 2 1
3 2 0
```




```output1
45
```




```output2
10
```


