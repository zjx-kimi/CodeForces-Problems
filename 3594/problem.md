## Description

<div><p>There are $N$ cities in the country of Numbata, numbered from $1$ to $N$. Currently, there is no road connecting them. Therefore, each of these $N$ cities proposes a road candidate to be constructed.</p><p>City $i$ likes to connect with city $A_i$, so city $i$ proposes to add a direct bidirectional road connecting city $i$ and city $A_i$. It is guaranteed that no two cities like to connect with each other. In other words, there is no pair of integers $i$ and $j$ where $A_i = j$ and $A_j = i$. It is also guaranteed that any pair of cities are connected by a sequence of road proposals. In other words, if all proposed roads are constructed, then any pair of cities are connected by a sequence of constructed road.</p><p>City $i$ also prefers the road to be constructed using a specific material. Each material can be represented by an integer (for example, $0$ for asphalt, $1$ for wood, etc.). The material that can be used for the road connecting city $i$ and city $A_i$ is represented by an array $B_i$ containing $M_i$ integers: $[(B_i)_1, (B_i)_2, \dots, (B_i)_{M_i}]$. This means that the road connecting city $i$ and city $A_i$ can be constructed with either of the material in $B_i$.</p><p>There are $K$ workers to construct the roads. Each worker is only familiar with one material, thus can only construct a road with a specific material. In particular, the $i^{th}$ worker can only construct a road with material $C_i$. Each worker can only construct at most one road. You want to assign each worker to construct a road such that any pair of cities are connected by a sequence of constructed road.</p></div><div class="input-specification"><p>Input begins with a line containing two integers: $N$ $K$ ($3 \le N \le 2000$; $1 \le K \le 2000$) representing the number of cities and the number of workers, respectively. The next $N$ lines each contains several integers: $A_i$ $M_i$ $(B_i)_1$, $(B_i)_2$, $\cdots$, $(B_i)_{M_i}$ ($1 \le A_i \le N$; $A_i \ne i$; $1 \le M_i \le 10\,000$; $0 \le (B_i)_1 &lt; (B_i)_2 &lt; \dots &lt; (B_i)_{M_i} \le 10^9$) representing the bidirectional road that city $i$ likes to construct. It is guaranteed that the sum of $M_i$ does not exceed $10\,000$. It is also guaranteed that no two cities like to connect with each other and any pair of cities are connected by a sequence of road proposals. The next line contains $K$ integers: $C_i$ ($0 \le C_i \le 10^9$) representing the material that is familiarized by the workers.</p></div><div class="output-specification"><p>If it is not possible to assign each worker to construct a road such that any pair of cities are connected by a sequence of constructed road, simply output <span class="tex-font-style-tt">-1</span> in a line. Otherwise, for each worker in the same order as input, output in a line two integers (separated by a single space): $u$ and $v$ in any order. This means that the worker constructs a direct bidirectional road connecting city $u$ and $v$. If the worker does not construct any road, output "<span class="tex-font-style-tt">0 0</span>" (without quotes) instead. Each pair of cities can only be assigned to at most one worker. You may output any assignment as long as any pair of cities are connected by a sequence of constructed road.</p></div>

## Input

<p>Input begins with a line containing two integers: $N$ $K$ ($3 \le N \le 2000$; $1 \le K \le 2000$) representing the number of cities and the number of workers, respectively. The next $N$ lines each contains several integers: $A_i$ $M_i$ $(B_i)_1$, $(B_i)_2$, $\cdots$, $(B_i)_{M_i}$ ($1 \le A_i \le N$; $A_i \ne i$; $1 \le M_i \le 10\,000$; $0 \le (B_i)_1 &lt; (B_i)_2 &lt; \dots &lt; (B_i)_{M_i} \le 10^9$) representing the bidirectional road that city $i$ likes to construct. It is guaranteed that the sum of $M_i$ does not exceed $10\,000$. It is also guaranteed that no two cities like to connect with each other and any pair of cities are connected by a sequence of road proposals. The next line contains $K$ integers: $C_i$ ($0 \le C_i \le 10^9$) representing the material that is familiarized by the workers.</p>

## Output

<p>If it is not possible to assign each worker to construct a road such that any pair of cities are connected by a sequence of constructed road, simply output <span class="tex-font-style-tt">-1</span> in a line. Otherwise, for each worker in the same order as input, output in a line two integers (separated by a single space): $u$ and $v$ in any order. This means that the worker constructs a direct bidirectional road connecting city $u$ and $v$. If the worker does not construct any road, output "<span class="tex-font-style-tt">0 0</span>" (without quotes) instead. Each pair of cities can only be assigned to at most one worker. You may output any assignment as long as any pair of cities are connected by a sequence of constructed road.</p>





```input1
4 5
2 2 1 2
3 2 2 3
4 2 3 4
2 2 4 5
1 2 3 4 5
```




```input2
4 5
2 2 10 20
3 2 2 3
4 2 3 4
2 2 4 5
1 2 3 4 5
```




```output1
1 2
2 3
3 4
0 0
4 2
```




```output2
-1
```



## Note

<p><span class="tex-font-style-it">Explanation for the sample input/output #1</span></p><p>We can assign the workers to construct the following roads: </p><ul> <li> The first worker constructs a road connecting city $1$ and city $2$. </li><li> The second worker constructs a road connecting city $2$ and city $3$. </li><li> The third worker constructs a road connecting city $3$ and city $4$. </li><li> The fourth worker does not construct any road. </li><li> The fifth worker constructs a road connecting city $4$ and city $2$. </li></ul> Therefore, any pair of cities are now connected by a sequence of constructed road.<p><span class="tex-font-style-it">Explanation for the sample input/output #2</span></p><p>There is no worker that can construct a road connecting city $1$, thus city $1$ is certainly isolated.</p>
