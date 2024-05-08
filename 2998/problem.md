## Description

<div><p>You have a set of $n$ discs, the $i$-th disc has radius $i$. Initially, these discs are split among $m$ towers: each tower contains at least one disc, and the discs in each tower are sorted in descending order of their radii from bottom to top.</p><p>You would like to assemble one tower containing all of those discs. To do so, you may choose two different towers $i$ and $j$ (each containing at least one disc), take several (possibly all) top discs from the tower $i$ and put them on top of the tower $j$ in the same order, as long as the top disc of tower $j$ is bigger than each of the discs you move. You may perform this operation any number of times.</p><p>For example, if you have two towers containing discs $[6, 4, 2, 1]$ and $[8, 7, 5, 3]$ (in order from bottom to top), there are only two possible operations:</p><ul> <li> move disc $1$ from the first tower to the second tower, so the towers are $[6, 4, 2]$ and $[8, 7, 5, 3, 1]$; </li><li> move discs $[2, 1]$ from the first tower to the second tower, so the towers are $[6, 4]$ and $[8, 7, 5, 3, 2, 1]$. </li></ul><p>Let the <span class="tex-font-style-it">difficulty</span> of some set of towers be the minimum number of operations required to assemble one tower containing all of the discs. For example, the <span class="tex-font-style-it">difficulty</span> of the set of towers $[[3, 1], [2]]$ is $2$: you may move the disc $1$ to the second tower, and then move both discs from the second tower to the first tower.</p><p>You are given $m - 1$ queries. Each query is denoted by two numbers $a_i$ and $b_i$, and means "merge the towers $a_i$ and $b_i$" (that is, take all discs from these two towers and assemble a new tower containing all of them in descending order of their radii from top to bottom). The resulting tower gets index $a_i$.</p><p>For each $k \in [0, m - 1]$, calculate the <span class="tex-font-style-it">difficulty</span> of the set of towers after the first $k$ queries are performed.</p></div><div class="input-specification"><p>The first line of the input contains two integers $n$ and $m$ ($2 \le m \le n \le 2 \cdot 10^5$) — the number of discs and the number of towers, respectively.</p><p>The second line contains $n$ integers $t_1$, $t_2$, ..., $t_n$ ($1 \le t_i \le m$), where $t_i$ is the index of the tower disc $i$ belongs to. Each value from $1$ to $m$ appears in this sequence at least once.</p><p>Then $m - 1$ lines follow, denoting the queries. Each query is represented by two integers $a_i$ and $b_i$ ($1 \le a_i, b_i \le m$, $a_i \ne b_i$), meaning that, during the $i$-th query, the towers with indices $a_i$ and $b_i$ are merged ($a_i$ and $b_i$ are chosen in such a way that these towers exist before the $i$-th query).</p></div><div class="output-specification"><p>Print $m$ integers. The $k$-th integer ($0$-indexed) should be equal to the difficulty of the set of towers after the first $k$ queries are performed.</p></div>

## Input

<p>The first line of the input contains two integers $n$ and $m$ ($2 \le m \le n \le 2 \cdot 10^5$) — the number of discs and the number of towers, respectively.</p><p>The second line contains $n$ integers $t_1$, $t_2$, ..., $t_n$ ($1 \le t_i \le m$), where $t_i$ is the index of the tower disc $i$ belongs to. Each value from $1$ to $m$ appears in this sequence at least once.</p><p>Then $m - 1$ lines follow, denoting the queries. Each query is represented by two integers $a_i$ and $b_i$ ($1 \le a_i, b_i \le m$, $a_i \ne b_i$), meaning that, during the $i$-th query, the towers with indices $a_i$ and $b_i$ are merged ($a_i$ and $b_i$ are chosen in such a way that these towers exist before the $i$-th query).</p>

## Output

<p>Print $m$ integers. The $k$-th integer ($0$-indexed) should be equal to the difficulty of the set of towers after the first $k$ queries are performed.</p>





```input1
7 4
1 2 3 3 1 4 3
3 1
2 3
2 4
```




```output1
5
4
2
0
```



## Note

<p>The towers in the example are:</p><ul> <li> before the queries: $[[5, 1], [2], [7, 4, 3], [6]]$; </li><li> after the first query: $[[2], [7, 5, 4, 3, 1], [6]]$; </li><li> after the second query: $[[7, 5, 4, 3, 2, 1], [6]]$; </li><li> after the third query, there is only one tower: $[7, 6, 5, 4, 3, 2, 1]$. </li></ul>
