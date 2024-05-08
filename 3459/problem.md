## Description

<div><p>Donghyun's new social network service (SNS) contains $n$ users numbered $1, 2, \ldots, n$. Internally, their network is a <span class="tex-font-style-it">tree graph</span>, so there are $n-1$ direct connections between each user. Each user can reach every other users by using some sequence of direct connections. From now on, we will denote this primary network as $T_1$.</p><p>To prevent a possible server breakdown, Donghyun created a backup network $T_2$, which also connects the same $n$ users via a tree graph. If a system breaks down, exactly one edge $e \in T_1$ becomes unusable. In this case, Donghyun will protect the edge $e$ by picking another edge $f \in T_2$, and add it to the existing network. This new edge should make the network be connected again. </p><p>Donghyun wants to assign a replacement edge $f \in T_2$ for as many edges $e \in T_1$ as possible. However, since the backup network $T_2$ is fragile, $f \in T_2$ can be assigned as the replacement edge for at most one edge in $T_1$. With this restriction, Donghyun wants to protect as many edges in $T_1$ as possible.</p><p>Formally, let $E(T)$ be an edge set of the tree $T$. We consider a bipartite graph with two parts $E(T_1)$ and $E(T_2)$. For $e \in E(T_1), f \in E(T_2)$, there is an edge connecting $\{e, f\}$ if and only if graph $T_1 - \{e\} + \{f\}$ is a tree. You should find a maximum matching in this bipartite graph.</p></div><div class="input-specification"><p>The first line contains an integer $n$ ($2 \le n \le 250\,000$), the number of users. </p><p>In the next $n-1$ lines, two integers $a_i$, $b_i$ ($1 \le a_i, b_i \le n$) are given. Those two numbers denote the indices of the vertices connected by the corresponding edge in $T_1$.</p><p>In the next $n-1$ lines, two integers $c_i$, $d_i$ ($1 \le c_i, d_i \le n$) are given. Those two numbers denote the indices of the vertices connected by the corresponding edge in $T_2$. </p><p>It is guaranteed that both edge sets form a tree of size $n$.</p></div><div class="output-specification"><p>In the first line, print the number $m$ ($0 \leq m &lt; n$), the maximum number of edges that can be protected.</p><p>In the next $m$ lines, print four integers $a_i, b_i, c_i, d_i$. Those four numbers denote that the edge $(a_i, b_i)$ in $T_1$ is will be replaced with an edge $(c_i, d_i)$ in $T_2$.</p><p>All printed edges should belong to their respective network, and they should link to distinct edges in their respective network. If one removes an edge $(a_i, b_i)$ from $T_1$ and adds edge $(c_i, d_i)$ from $T_2$, the network should remain connected. The order of printing the edges or the order of vertices in each edge does not matter.</p><p>If there are several solutions, you can print any.</p></div>

## Input

<p>The first line contains an integer $n$ ($2 \le n \le 250\,000$), the number of users. </p><p>In the next $n-1$ lines, two integers $a_i$, $b_i$ ($1 \le a_i, b_i \le n$) are given. Those two numbers denote the indices of the vertices connected by the corresponding edge in $T_1$.</p><p>In the next $n-1$ lines, two integers $c_i$, $d_i$ ($1 \le c_i, d_i \le n$) are given. Those two numbers denote the indices of the vertices connected by the corresponding edge in $T_2$. </p><p>It is guaranteed that both edge sets form a tree of size $n$.</p>

## Output

<p>In the first line, print the number $m$ ($0 \leq m &lt; n$), the maximum number of edges that can be protected.</p><p>In the next $m$ lines, print four integers $a_i, b_i, c_i, d_i$. Those four numbers denote that the edge $(a_i, b_i)$ in $T_1$ is will be replaced with an edge $(c_i, d_i)$ in $T_2$.</p><p>All printed edges should belong to their respective network, and they should link to distinct edges in their respective network. If one removes an edge $(a_i, b_i)$ from $T_1$ and adds edge $(c_i, d_i)$ from $T_2$, the network should remain connected. The order of printing the edges or the order of vertices in each edge does not matter.</p><p>If there are several solutions, you can print any.</p>





```input1
4
1 2
2 3
4 3
1 3
2 4
1 4
```




```input2
5
1 2
2 4
3 4
4 5
1 2
1 3
1 4
1 5
```




```input3
9
7 9
2 8
2 1
7 5
4 7
2 4
9 6
3 9
1 8
4 8
2 9
9 5
7 6
1 3
4 6
5 3
```




```output1
3
3 2 4 2
2 1 1 3
4 3 1 4
```




```output2
4
2 1 1 2
3 4 1 3
4 2 1 4
5 4 1 5
```




```output3
8
4 2 9 2
9 7 6 7
5 7 5 9
6 9 4 6
8 2 8 4
3 9 3 5
2 1 1 8
7 4 1 3
```


