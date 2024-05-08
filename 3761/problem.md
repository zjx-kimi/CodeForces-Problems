## Description

<div><p>In the galaxy far far away is the ancient interplanetary republic of Bubbleland, consisting of $N$ planets. Between them, there are $M$ bidirectional wormholes, each connecting a pair of planets. Bubbleland is a very centralized republic, having a capital planet Whiteplanet, from which any another planet can be reached using these wormholes. It is also guaranteed that no wormhole connects planet to itself and that no two different wormholes connect same pair of planets. </p><p>We call a path that begins at one planet, visits other planets and each of them at most once and returns to starting point a <span class="tex-font-style-it">tour</span>. Interplanetary Safety Regulations guarantee that each planet belongs to at most one <span class="tex-font-style-it">tour</span> and that there are at most $42$ <span class="tex-font-style-it">tours</span>.</p><p>After many eons of usage, wormholes need to be repaired and each wormhole has the cost $W_{i}$ which needs to be payed for reparation. Unfortunately, the Senate of Bubbleland is short on budget. Therefore, they have decided only to fix as many wormholes as they need in order to have all planets reachable from capital and to pay as little money as they have to for this repair. However the way in which the Senate calculates the cost is different. Cost of the set of reparations is binary xor of costs of each individual reparation, that is if reparations to be made have costs $A_{1},A_{2},...,A_{k}$, the cost of entire set is $A_{1} \oplus A_{2} \oplus ... \oplus A_{k}$.</p><p>Now the Senate would like to know how much money do they have to pay and also the number of different ways to achieve that cost <span class="tex-font-style-bf">modulo $1000000007$</span>.</p></div><div class="input-specification"><p>First line of input contains two numbers $N (1 \leq N \leq 100.000)$, the number of planets and $M (1 \leq M \leq 100.041)$, the number of wormholes. Following $M$ lines contain three numbers $U, V (1 \leq U \neq V \leq N)$ and $W (1 \leq W \leq 100.000)$, meaning that there exists a wormhole connecting planets $U$ and $V$, with repair cost of $W$.</p></div><div class="output-specification"><p>Output two numbers, the smallest possible cost of entire reparation and the number of different valid reparations with that cost <span class="tex-font-style-bf">modulo $1000000007$</span>.</p></div>

## Input

<p>First line of input contains two numbers $N (1 \leq N \leq 100.000)$, the number of planets and $M (1 \leq M \leq 100.041)$, the number of wormholes. Following $M$ lines contain three numbers $U, V (1 \leq U \neq V \leq N)$ and $W (1 \leq W \leq 100.000)$, meaning that there exists a wormhole connecting planets $U$ and $V$, with repair cost of $W$.</p>

## Output

<p>Output two numbers, the smallest possible cost of entire reparation and the number of different valid reparations with that cost <span class="tex-font-style-bf">modulo $1000000007$</span>.</p>





```input1
6 6
4 1 5
5 2 1
6 3 2
1 2 6
1 3 3
2 3 4
```




```output1
1 1
```



## Note

<p>We can repair wormholes $1$,$2$,$3$,$5$ and $6$, paying $5 \oplus 1\oplus 2 \oplus 3 \oplus 4=1$, one can check that this is the cheapest repair in which all of the planets are connected and the only valid repair with that cost.</p>
