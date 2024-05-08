## Description

<div><p>Rishi is developing games in the 2D metaverse and wants to offer game bundles to his customers. Each game has an associated enjoyment value. A game bundle consists of a subset of games whose total enjoyment value adds up to $60$.</p><p>Your task is to choose $k$ games, where $1 \leq k \leq 60$, along with their respective enjoyment values $a_1, a_2, \dots, a_k$, in such a way that exactly $m$ distinct game bundles can be formed.</p></div><div class="input-specification"><p>The input is a single integer $m$ ($1 \le m \le 10^{10}$) — the desired number of game bundles.</p></div><div class="output-specification"><p>The first line should contain an integer $k$ ($1 \le k \le 60$) — the number of games.</p><p>The second line should contain $k$ integers, $a_1, a_2, \dots, a_k$ ($1 \le a_1, a_2, \dots, a_k \le 60$) — the enjoyment values of the $k$ games.</p></div>

## Input

<p>The input is a single integer $m$ ($1 \le m \le 10^{10}$) — the desired number of game bundles.</p>

## Output

<p>The first line should contain an integer $k$ ($1 \le k \le 60$) — the number of games.</p><p>The second line should contain $k$ integers, $a_1, a_2, \dots, a_k$ ($1 \le a_1, a_2, \dots, a_k \le 60$) — the enjoyment values of the $k$ games.</p>





```input1
4
```




```input2
722
```




```input3
1
```




```output1
4
20 20 20 20
```




```output2
15
15 14 13 12 11 10 9 8 7 6 5 4 3 2 1
```




```output3
1
60
```



## Note

<p>In the first sample, any subset of size $3$ is a game bundle. There are $4$ such subsets.</p>
