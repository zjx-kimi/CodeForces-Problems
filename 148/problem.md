## Description

<div><p>You are given a one-based array consisting of $N$ integers: $A_1, A_2, \cdots, A_N$. Initially, the value of each element is set to $0$.</p><p>There are $M$ operations (numbered from $1$ to $M$). Operation $i$ is represented by $\langle L_i, R_i, X_i \rangle$. If operation $i$ is executed, all elements $A_j$ for $L_i \leq j \leq R_i$ will be increased by $X_i$.</p><p>You have to answer $Q$ <span class="tex-font-style-bf">independent</span> queries. Each query is represented by $\langle K, S, T \rangle$ which represents the following task. Choose a range $[l, r]$ satisfying $S \leq l \leq r \leq T$, and execute operations $l, l + 1, \dots, r$. The answer to the query is the maximum value of $A_K$ after the operations are executed among all possible choices of $l$ and $r$.</p></div><div class="input-specification"><p>The first line consists of two integers $N$ $M$ ($1 \leq N, M \leq 100\,000$).</p><p>Each of the next $M$ lines consists of three integers $L_i$ $R_i$ $X_i$ ($1 \leq L_i \leq R_i \leq N; -100\,000 \leq X_i \leq 100\,000$).</p><p>The following line consists of an integer $Q$ ($1 \leq Q \leq 100\,000$).</p><p>Each of the next $Q$ lines consists of three integers $K$ $S$ $T$ ($1 \leq K \leq N; 1 \leq S \leq T \leq M$).</p></div><div class="output-specification"><p>For each query, output in a single line, an integer which represent the answer of the query.</p></div>

## Input

<p>The first line consists of two integers $N$ $M$ ($1 \leq N, M \leq 100\,000$).</p><p>Each of the next $M$ lines consists of three integers $L_i$ $R_i$ $X_i$ ($1 \leq L_i \leq R_i \leq N; -100\,000 \leq X_i \leq 100\,000$).</p><p>The following line consists of an integer $Q$ ($1 \leq Q \leq 100\,000$).</p><p>Each of the next $Q$ lines consists of three integers $K$ $S$ $T$ ($1 \leq K \leq N; 1 \leq S \leq T \leq M$).</p>

## Output

<p>For each query, output in a single line, an integer which represent the answer of the query.</p>





```input1
2 6
1 1 -50
1 2 -20
2 2 -30
1 1 60
1 2 40
2 2 10
5
1 1 6
2 1 6
1 1 3
2 1 3
1 1 2
```




```input2
5 3
1 3 3
2 4 -2
3 5 3
6
1 1 3
2 1 3
3 1 3
3 2 3
2 2 3
2 2 2
```




```output1
100
50
0
0
-20
```




```output2
3
3
4
3
0
-2
```



## Note

<p><span class="tex-font-style-it">Explanation for the sample input/output #1</span></p><p>For query $1$, one of the solutions is to execute operation $4$ and $5$.</p><p>For query $2$, one of the solutions is to execute operation $4$, $5$, and $6$.</p><p>For query $3$, the only solution is to execute operation $3$.</p><p>For query $4$, the only solution is to execute operation $1$.</p><p>For query $6$, the only solution is to execute operation $2$.</p>
