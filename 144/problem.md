## Description

<div><p>You are currently researching a graph traversal algorithm called the Breadth First Search (BFS). Suppose you have an input graph of $N$ nodes (numbered from $1$ to $N$). The graph is represented by an adjacency matrix $M$, for which node $u$ can traverse to node $v$ if $M_{u, v}$ is $1$, otherwise it is $0$. Your algorithm will output the order the nodes are visited in the BFS. The pseudocode of the algorithm is presented as follows.</p><pre class="verbatim"><br>    BFS(M[1..N][1..N]):<br>        let A be an empty array<br>        let Q be an empty queue<br><br>        append 1 to A<br>        push 1 to Q<br><br>        while Q is not empty:<br>            pop the front element of Q into u<br>            for v = 1 to N:<br>                if M[u][v] == 1 and v is not in A:<br>                    append v to A<br>                    push v to Q<br><br>        return A<br></pre><p>During your research, you are interested in the following problem. Given an array $A$ such that $A$ is a permutation of $1$ to $N$ and $A_1 = 1$. How many <span class="tex-font-style-bf">simple undirected graph</span> with $N$ nodes and adjacency matrix $M$ such that $\text{BFS}(M) = A$? Since the answer can be very large, calculate the answer modulo $998\,244\,353$.</p><p>A simple graph has no self-loop ($M_{i, i} = 0$ for $1 \leq i \leq N$) and there is at most one edge that connects a pair of nodes. In an undirected graph, if node $u$ is adjacent to node $v$, then node $v$ is also adjacent to node $u$; formally, $M_{u, v} = M_{v, u}$ for $1 \leq u &lt; v \leq N$.</p><p>Two graphs are considered different if there is an edge that exists in one graph but not the other. In other words, two graphs are considered different if their adjacency matrices are different.</p></div><div class="input-specification"><p>The first line consists of an integer $N$ ($2 \leq N \leq 5000$).</p><p>The second line consists of $N$ integers $A_i$. The array $A$ is a permutation of $1$ to $N$ and $A_1 = 1$.</p></div><div class="output-specification"><p>Output an integer representing the number of simple undirected graphs with $N$ nodes and adjacency matrix $M$ such that $\text{BFS}(M) = A$. Since the answer can be very large, output the answer modulo $998\,244\,353$.</p></div>

## Input

<p>The first line consists of an integer $N$ ($2 \leq N \leq 5000$).</p><p>The second line consists of $N$ integers $A_i$. The array $A$ is a permutation of $1$ to $N$ and $A_1 = 1$.</p>

## Output

<p>Output an integer representing the number of simple undirected graphs with $N$ nodes and adjacency matrix $M$ such that $\text{BFS}(M) = A$. Since the answer can be very large, output the answer modulo $998\,244\,353$.</p>





```input1
3
1 2 3
```




```input2
3
1 3 2
```




```input3
5
1 3 2 4 5
```




```input4
11
1 2 3 4 5 6 7 8 9 10 11
```




```output1
3
```




```output2
1
```




```output3
17
```




```output4
379394847
```



## Note

<p><span class="tex-font-style-it">Explanation for the sample input/output #1</span></p><p>The following illustration shows all graphs that satisfy the requirements.</p><center> <img class="tex-graphics" src="file://J3xFGEo4.png" style="max-width: 100.0%;max-height: 100.0%;" width="378px"> </center><p><span class="tex-font-style-it">Explanation for the sample input/output #2</span></p><p>The only graph that satisfies the requirements is a graph with two edges: one that connects nodes $1$ and $3$, and another one that connects nodes $3$ and $2$.</p>
