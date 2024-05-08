## Description

<div><p>Let's call an ordered pair of nodes $(u, v)$ in a directed graph <span class="tex-font-style-it">unidirectional</span> if $u \neq v$, there exists a path from $u$ to $v$, and there are no paths from $v$ to $u$.</p><p>A directed graph is called <span class="tex-font-style-it">$p$-reachable</span> if it contains exactly $p$ ordered pairs of nodes $(u, v)$ such that $u &lt; v$ and $u$ and $v$ are reachable from each other. Find the minimum number of nodes required to create a $p$-reachable directed graph.</p><p>Also, among all such $p$-reachable directed graphs with the minimum number of nodes, let $G$ denote a graph which maximizes the number of unidirectional pairs of nodes. Find this number.</p></div><div class="input-specification"><p>The first and only line contains a single integer $p$ ($0 \le p \le 2 \cdot 10^5$)&nbsp;— the number of ordered pairs of nodes.</p></div><div class="output-specification"><p>Print a single line containing two integers&nbsp;— the minimum number of nodes required to create a $p$-reachable directed graph, and the maximum number of unidirectional pairs of nodes among all such $p$-reachable directed graphs with the minimum number of nodes.</p></div>

## Input

<p>The first and only line contains a single integer $p$ ($0 \le p \le 2 \cdot 10^5$)&nbsp;— the number of ordered pairs of nodes.</p>

## Output

<p>Print a single line containing two integers&nbsp;— the minimum number of nodes required to create a $p$-reachable directed graph, and the maximum number of unidirectional pairs of nodes among all such $p$-reachable directed graphs with the minimum number of nodes.</p>





```input1
3
```




```input2
4
```




```input3
0
```




```output1
3 0
```




```output2
5 6
```




```output3
0 0
```



## Note

<p>In the first test case, the minimum number of nodes required to create a $3$-reachable directed graph is $3$. Among all $3$-reachable directed graphs with $3$ nodes, the following graph $G$ is one of the graphs with the maximum number of unidirectional pairs of nodes, which is $0$. </p><center> <img class="tex-graphics" src="file://umGlp3E2.png" style="max-width: 100.0%;max-height: 100.0%;"> </center>
