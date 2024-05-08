## Description

<div><p>Pak Chanek observes that the carriages of a train is always full on morning departure hours and afternoon departure hours. Therefore, the balance between carriages is needed so that it is not too crowded in only a few carriages.</p><p>A train contains $N$ carriages that are numbered from $1$ to $N$ from left to right. Carriage $i$ initially contains $A_i$ passengers. All carriages are connected by carriage doors, namely for each $i$ ($1\leq i\leq N-1$), carriage $i$ and carriage $i+1$ are connected by a two-way door.</p><p>Each passenger can move between carriages, but train regulation regulates that for each $i$, a passenger that <span class="tex-font-style-bf">starts from carriage $i$</span> cannot go through more than $D_i$ doors.</p><p>Define $Z$ as the most number of passengers in one same carriage after moving. Pak Chanek asks, what is the minimum possible value of $Z$?</p></div><div class="input-specification"><p>The first line contains a single integer $N$ ($1 \leq N \leq 2\cdot10^5$) — the number of carriages.</p><p>The second line contains $N$ integers $A_1, A_2, A_3, \ldots, A_N$ ($0 \leq A_i \leq 10^9$) — the initial number of passengers in each carriage.</p><p>The third line contains $N$ integers $D_1, D_2, D_3, \ldots, D_N$ ($0 \leq D_i \leq N-1$) — the maximum limit of the number of doors for each starting carriage.</p></div><div class="output-specification"><p>An integer representing the minimum possible value of $Z$.</p></div>

## Input

<p>The first line contains a single integer $N$ ($1 \leq N \leq 2\cdot10^5$) — the number of carriages.</p><p>The second line contains $N$ integers $A_1, A_2, A_3, \ldots, A_N$ ($0 \leq A_i \leq 10^9$) — the initial number of passengers in each carriage.</p><p>The third line contains $N$ integers $D_1, D_2, D_3, \ldots, D_N$ ($0 \leq D_i \leq N-1$) — the maximum limit of the number of doors for each starting carriage.</p>

## Output

<p>An integer representing the minimum possible value of $Z$.</p>





```input1
7
7 4 2 0 5 8 3
4 0 0 1 3 1 3
```




```output1
5
```



## Note

<p>One strategy that is optimal is as follows: </p><ul> <li> $5$ people in carriage $1$ move to carriage $4$ (going through $3$ doors). </li><li> $3$ people in carriage $5$ move to carriage $3$ (going through $2$ doors). </li><li> $2$ people in carriage $6$ move to carriage $5$ (going through $1$ door). </li><li> $1$ person in carriage $6$ moves to carriage $7$ (going through $1$ door). </li></ul><p>The number of passengers in each carriage becomes $[2,4,5,5,4,5,4]$.</p>
