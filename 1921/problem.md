## Description

<div><p>You are given an undirected graph of $N$ nodes and $M$ edges, $E_1, E_2, \dots E_M$.</p><p>A connected graph is a cactus if each of it's edges belogs to at most one simple cycle. A graph is a desert if each of it's connected components is a cactus. </p><p>Find the number of pairs $(L, R)$, ($1 \leq L \leq R \leq M$) such that, if we delete all the edges except for $E_L, E_{L+1}, \dots E_R$, the graph is a desert. </p></div><div class="input-specification"><p>The first line contains two integers $N$ and $M$ ($2 \leq N \leq 2.5 \times 10^5$, $1 \leq M \leq 5 \times 10^5$). Each of the next $M$ lines contains two integers. The $i$-th line describes the $i$-th edge. It contains integers $U_i$ and $V_i$, the nodes connected by the $i$-th edge ($E_i=(U_i, V_i)$). It is guaranteed that $1 \leq U_i, V_i \leq N$ and $U_i \neq V_i$. </p></div><div class="output-specification"><p>The output contains one integer number – the answer.</p></div>

## Input

<p>The first line contains two integers $N$ and $M$ ($2 \leq N \leq 2.5 \times 10^5$, $1 \leq M \leq 5 \times 10^5$). Each of the next $M$ lines contains two integers. The $i$-th line describes the $i$-th edge. It contains integers $U_i$ and $V_i$, the nodes connected by the $i$-th edge ($E_i=(U_i, V_i)$). It is guaranteed that $1 \leq U_i, V_i \leq N$ and $U_i \neq V_i$. </p>

## Output

<p>The output contains one integer number – the answer.</p>





```input1
5 6
1 2
2 3
3 4
4 5
5 1
2 4
```




```input2
2 3
1 2
1 2
1 2
```




```output1
20
```




```output2
5
```



## Note

<p>In the second example: Graphs for pairs $(1, 1)$, $(2, 2)$ and $(3, 3)$ are deserts because they don't have any cycles. Graphs for pairs $(1, 2)$ and $(2, 3)$ have one cycle of length 2 so they are deserts.</p>
