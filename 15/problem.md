## Description

<div><p>There are $n$ points numbered $1$ to $n$ on a straight line. Initially, there are $m$ harbours. The $i$-th harbour is at point $X_i$ and has a value $V_i$. <span class="tex-font-style-bf">It is guaranteed that there are harbours at the points $1$ and $n$.</span> There is exactly one ship on each of the $n$ points. The cost of moving a ship from its current location to the next harbour is the product of the value of the nearest harbour to its left and the distance from the nearest harbour to its right. Specifically, if a ship is already at a harbour, the cost of moving it to the next harbour is $0$. </p><p>Additionally, there are $q$ queries, each of which is either of the following $2$ types:</p><ul> <li> $1$ $x$ $v$ — Add a harbour at point $x$ with value $v$. It is guaranteed that before adding the harbour, there is no harbour at point $x$. </li><li> $2$ $l$ $r$ — Print the sum of the cost of moving all ships at points from $l$ to $r$ to their next harbours. <span class="tex-font-style-bf">Note that you just need to calculate the cost of moving the ships but not actually move them.</span> </li></ul></div><div class="input-specification"><p>The first line contains three integers $n$, $m$, and $q$ ($2 \le m \le n \le 3 \cdot 10^5$, $1 \le q \le 3 \cdot 10^5$) — the number of points, harbours, and queries, respectively.</p><p>The second line contains $m$ distinct integers $X_1, X_2, \ldots, X_m(1 \le X_i \le n)$ — the position at which the $i$-th harbour is located.</p><p>The third line contains $m$ integers $V_1, V_2, \ldots, V_m(1 \le V_i \le 10^7)$ — the value of the $i$-th harbour.</p><p>Each of the next $q$ lines contains three integers. The first integer is $t$ ($1\le t \le 2$) — type of query. If $t=1$, then the next two integers are $x$ and $v$ ($2 \le x \le n - 1$, $1 \le v \le 10^7$) — first-type query. If $t=2$, then the next two integers are $l$ and $r$ ($1 \le l \le r \le n$) — second-type query.</p><p>It is guaranteed that there is at least one second-type query.</p></div><div class="output-specification"><p>For every second-type query, print one integer in a new line — answer to this query.</p></div>

## Input

<p>The first line contains three integers $n$, $m$, and $q$ ($2 \le m \le n \le 3 \cdot 10^5$, $1 \le q \le 3 \cdot 10^5$) — the number of points, harbours, and queries, respectively.</p><p>The second line contains $m$ distinct integers $X_1, X_2, \ldots, X_m(1 \le X_i \le n)$ — the position at which the $i$-th harbour is located.</p><p>The third line contains $m$ integers $V_1, V_2, \ldots, V_m(1 \le V_i \le 10^7)$ — the value of the $i$-th harbour.</p><p>Each of the next $q$ lines contains three integers. The first integer is $t$ ($1\le t \le 2$) — type of query. If $t=1$, then the next two integers are $x$ and $v$ ($2 \le x \le n - 1$, $1 \le v \le 10^7$) — first-type query. If $t=2$, then the next two integers are $l$ and $r$ ($1 \le l \le r \le n$) — second-type query.</p><p>It is guaranteed that there is at least one second-type query.</p>

## Output

<p>For every second-type query, print one integer in a new line — answer to this query.</p>





```input1|
8 3 4
1 3 8
3 24 10
2 2 5
1 5 15
2 5 5
2 7 8
```




```output1
171
0
15
```



## Note

<p>For the first type $2$ query, the cost for ships at positions $2$, $3$, $4$ and $5$ are $3(3 \times 1)$, $0$, $96(24 \times 4)$ and $72(24 \times 3)$ respectively.</p><p>For the second type $2$ query, since the ship at position $5$ is already at a harbour, so the cost is $0$.</p><p>For the third type $2$ query, the cost for ships at position $7$ and $8$ are $15(15 \times 1)$ and $0$ respectively.</p>
