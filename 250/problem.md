## Description

<div><p>Consider two undirected graphs $G_1$ and $G_2$. Every node in $G_1$ and in $G_2$ has a label. Doremy calls $G_1$ and $G_2$ similar if and only if:</p><ul> <li> The labels in $G_1$ are distinct, and the labels in $G_2$ are distinct. </li><li> The set $S$ of labels in $G_1$ coincides with the set of labels in $G_2$. </li><li> For every pair of two distinct labels $u$ and $v$ in $S$, the corresponding nodes are in the same connected component in $G_1$ if and only if they are in the same connected component in $G_2$. </li></ul><p>Now Doremy gives you two trees $T_1$ and $T_2$ with $n$ nodes, labeled from $1$ to $n$. You can do the following operation any number of times:</p><ul> <li> Choose an edge set $E_1$ from $T_1$ and an edge set $E_2$ from $T_2$, such that $\overline{E_1}$ and $\overline{E_2}$ are similar. Here $\overline{E}$ represents the graph which is given by only reserving the edge set $E$ from $T$ (i.e., the edge-induced subgraph). In other words, $\overline{E}$ is obtained from $T$ by removing all edges not included in $E$ and further removing all isolated vertices. </li><li> Swap the edge set $E_1$ in $T_1$ with the edge set $E_2$ in $T_2$. </li></ul><p>Now Doremy is wondering how many distinct $T_1$ you can get after any number of operations. Can you help her find the answer? Output the answer modulo $10^9+7$.</p></div><div class="input-specification"><p>The input consists of multiple test cases. The first line contains a single integer $t$ ($1\le t\le 2\cdot 10^4$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line contains an integer $n$ ($2\le n\le 10^5$)&nbsp;— the number of nodes in the trees $T_1$ and $T_2$.</p><p>Each of the following $n-1$ lines contain two integers $u,v$ ($1\le u,v\le n$), representing an undirected edge in $T_1$. It is guaranteed these edges form a tree.</p><p>Each of the following $n-1$ lines contain two integers $u,v$ ($1\le u,v\le n$), representing an undirected edge in $T_2$. It is guaranteed these edges form a tree.</p><p>It is guaranteed that the sum of $n$ does not exceed $2\cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, you should output a single line with an integer, representing the number of distinct $T_1$ after any number of operations, modulo $10^9+7$.</p></div>

## Input

<p>The input consists of multiple test cases. The first line contains a single integer $t$ ($1\le t\le 2\cdot 10^4$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line contains an integer $n$ ($2\le n\le 10^5$)&nbsp;— the number of nodes in the trees $T_1$ and $T_2$.</p><p>Each of the following $n-1$ lines contain two integers $u,v$ ($1\le u,v\le n$), representing an undirected edge in $T_1$. It is guaranteed these edges form a tree.</p><p>Each of the following $n-1$ lines contain two integers $u,v$ ($1\le u,v\le n$), representing an undirected edge in $T_2$. It is guaranteed these edges form a tree.</p><p>It is guaranteed that the sum of $n$ does not exceed $2\cdot 10^5$.</p>

## Output

<p>For each test case, you should output a single line with an integer, representing the number of distinct $T_1$ after any number of operations, modulo $10^9+7$.</p>





```input1|2,3,4,10,11,12,13,14,15,16
3
2
1 2
2 1
3
1 3
2 3
2 3
2 1
4
1 2
2 3
3 4
4 2
2 1
1 3
```




```output1
1
2
4
```



## Note

<p>In the first test case, there is at most one distinct $T_1$ having the only edge $(1,2)$.</p><p>In the second test case, you can choose the edge set $\{(1,3),(2,3)\}$ in $T_1$, the edge set $\{(1,2),(2,3)\}$ in $T_2$ and swap them. So $T_1$ can be $1-3-2$ or $1-2-3$.</p><p>In the third test case, there are $4$ distinct $T_1$, as the following pictures.</p><p><img class="tex-graphics" src="file://HI45EegG.png" style="max-width: 100.0%;max-height: 100.0%;"></p>
