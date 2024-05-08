## Description

<div><p>There are $n$ cities along the road, which can be represented as a straight line. The $i$-th city is situated at the distance of $a_i$ kilometers from the origin. All cities are situated in the same direction from the origin. There are $m$ trucks travelling from one city to another. </p><p>Each truck can be described by $4$ integers: starting city $s_i$, finishing city $f_i$, fuel consumption $c_i$ and number of possible refuelings $r_i$. The $i$-th truck will spend $c_i$ litres of fuel per one kilometer. </p><p>When a truck arrives in some city, it can be refueled (but refueling is impossible in the middle of nowhere). The $i$-th truck can be refueled at most $r_i$ times. Each refueling makes truck's gas-tank full. All trucks start with full gas-tank.</p><p>All trucks will have gas-tanks of the same size $V$ litres. You should find minimum possible $V$ such that all trucks can reach their destinations without refueling more times than allowed.</p></div><div class="input-specification"><p>First line contains two integers $n$ and $m$ ($2 \le n \le 400$, $1 \le m \le 250000$) — the number of cities and trucks.</p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le 10^9$, $a_i &lt; a_{i+1}$) — positions of cities in the ascending order.</p><p>Next $m$ lines contains $4$ integers each. The $i$-th line contains integers $s_i$, $f_i$, $c_i$, $r_i$ ($1 \le s_i &lt; f_i \le n$, $1 \le c_i \le 10^9$, $0 \le r_i \le n$) — the description of the $i$-th truck.</p></div><div class="output-specification"><p>Print the only integer — minimum possible size of gas-tanks $V$ such that all trucks can reach their destinations.</p></div>

## Input

<p>First line contains two integers $n$ and $m$ ($2 \le n \le 400$, $1 \le m \le 250000$) — the number of cities and trucks.</p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le 10^9$, $a_i &lt; a_{i+1}$) — positions of cities in the ascending order.</p><p>Next $m$ lines contains $4$ integers each. The $i$-th line contains integers $s_i$, $f_i$, $c_i$, $r_i$ ($1 \le s_i &lt; f_i \le n$, $1 \le c_i \le 10^9$, $0 \le r_i \le n$) — the description of the $i$-th truck.</p>

## Output

<p>Print the only integer — minimum possible size of gas-tanks $V$ such that all trucks can reach their destinations.</p>





```input1
7 6
2 5 7 10 14 15 17
1 3 10 0
1 7 12 7
4 5 13 3
4 7 10 1
4 7 10 1
1 5 11 2
```




```output1
55
```



## Note

<p>Let's look at queries in details: </p><ol> <li> the $1$-st truck must arrive at position $7$ from $2$ without refuelling, so it needs gas-tank of volume at least $50$. </li><li> the $2$-nd truck must arrive at position $17$ from $2$ and can be refueled at any city (if it is on the path between starting point and ending point), so it needs gas-tank of volume at least $48$. </li><li> the $3$-rd truck must arrive at position $14$ from $10$, there is no city between, so it needs gas-tank of volume at least $52$. </li><li> the $4$-th truck must arrive at position $17$ from $10$ and can be refueled only one time: it's optimal to refuel at $5$-th city (position $14$) so it needs gas-tank of volume at least $40$. </li><li> the $5$-th truck has the same description, so it also needs gas-tank of volume at least $40$. </li><li> the $6$-th truck must arrive at position $14$ from $2$ and can be refueled two times: first time in city $2$ or $3$ and second time in city $4$ so it needs gas-tank of volume at least $55$. </li></ol>
