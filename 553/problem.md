## Description

<div><p>You are given a bipartite graph $G$ with the vertex set in the left part $L$, in the right part $R$, and $m$ edges connecting these two sets. We know that $|L| = |R| = n$.</p><p>For any subset $S \subseteq L$, let $N(S)$ denote the set of all neighbors of vertices in $S$. We say that a subset $S \subseteq L$ in graph $G$ is <span class="tex-font-style-it">tight</span> if $|S| = |N(S)|$. We say that graph $G$ is <span class="tex-font-style-it">good</span> if $\forall_{S \subseteq L}, |S| \leq |N(S)|$.</p><p>Your task is to verify whether the graph is good and, if so, to optimize it. If the graph is not good, find a subset $S \subseteq L$ such that $|S| &gt; |N(S)|$. However, if the graph is good, your task is to find a good bipartite graph $G'$ with the same set of vertices $L \cup R$, in which $\forall_{S \subseteq L}$, $S$ is tight in $G$ if and only if $S$ is tight in $G'$. If there are multiple such graphs, choose one with the smallest possible number of edges. If there are still multiple such graphs, print any.</p></div><div class="input-specification"><p>The first line of the input contains two integers $n$ and $m$ ($1 \leq n \leq 10^3$, $0 \leq m \leq n^2$), separated by a single space. The number $n$ denotes the number of vertices in each of the sets $L$ and $R$, and the number $m$ denotes the number of edges between them.</p><p>The following $m$ lines describe the edges. Each of them contains two integers $l$ and $r$ ($1 \leq l \leq n$, $n+1 \leq r \leq 2 \cdot n$), separated by a single space, indicating that there is an edge from vertex $l \in L$ to vertex $r \in R$.</p></div><div class="output-specification"><p>If the graph $G$ given in the input is not good, output one word "<span class="tex-font-style-tt">NO</span>" in the first line of the output. In the second line of the output, output the number $k$, and in the third line, output $k$ numbers $l_1, l_2, \dots, l_k$, separated by single spaces. These numbers should indicate that for the set $S = \{l_1, l_2, \dots, l_k\}$, $|S| &gt; |N(S)|$.</p><p>However, if the graph $G$ given in the input is good, output one word "<span class="tex-font-style-tt">YES</span>" in the first line of the output. In the second line of the output, output the number $m'$, indicating the number of edges in the new, also good graph $G'$. Then, in the following $m'$ lines, output the edges of the graph $G'$ in the same format as given in the input.</p></div>

## Input

<p>The first line of the input contains two integers $n$ and $m$ ($1 \leq n \leq 10^3$, $0 \leq m \leq n^2$), separated by a single space. The number $n$ denotes the number of vertices in each of the sets $L$ and $R$, and the number $m$ denotes the number of edges between them.</p><p>The following $m$ lines describe the edges. Each of them contains two integers $l$ and $r$ ($1 \leq l \leq n$, $n+1 \leq r \leq 2 \cdot n$), separated by a single space, indicating that there is an edge from vertex $l \in L$ to vertex $r \in R$.</p>

## Output

<p>If the graph $G$ given in the input is not good, output one word "<span class="tex-font-style-tt">NO</span>" in the first line of the output. In the second line of the output, output the number $k$, and in the third line, output $k$ numbers $l_1, l_2, \dots, l_k$, separated by single spaces. These numbers should indicate that for the set $S = \{l_1, l_2, \dots, l_k\}$, $|S| &gt; |N(S)|$.</p><p>However, if the graph $G$ given in the input is good, output one word "<span class="tex-font-style-tt">YES</span>" in the first line of the output. In the second line of the output, output the number $m'$, indicating the number of edges in the new, also good graph $G'$. Then, in the following $m'$ lines, output the edges of the graph $G'$ in the same format as given in the input.</p>





```input1
3 8
1 4
1 5
1 6
2 4
2 5
2 6
3 5
3 6
```




```input2
3 4
1 4
1 5
2 6
3 6
```




```output1
YES
6
1 4
1 5
2 5
2 6
3 6
3 4
```




```output2
NO
2
2 3
```



## Note

<p>In the first sample test, the graph $G$ is good; thus, we are looking for an equivalent graph with the same tight sets. The only tight set is $\{ 1, 2, 3 \}$, which remains tight in the resulting graph. Moreover, no other set is tight in the resulting graph. One can prove that no graph with less than $6$ edges and the same tight sets exists.</p><p>In the second sample test, the graph $G$ is not good. Set $\{ 2, 3 \}$ has only one neighbour — vertex $6$. Thus, $|\{ 2, 3 \}| &gt; |\{ 6 \}|$, which is a prove that the input graph is not good.</p>
