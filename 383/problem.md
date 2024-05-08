## Description

<div><p>Pak Chanek has a directed acyclic graph (a directed graph that does not have any cycles) containing $N$ vertices. Vertex $i$ has $S_i$ edges directed away from that vertex. The $j$-th edge of vertex $i$ that is directed away from it, is directed towards vertex $L_{i,j}$ and has an integer $W_{i,j}$ ($0\leq W_{i,j}\leq1$). Another information about the graph is that the graph is shaped in such a way such that each vertex can be reached from vertex $1$ via zero or more directed edges.</p><p>Pak Chanek has an array $Z$ that is initially empty.</p><p>Pak Chanek defines the function <span class="tex-font-style-tt">dfs</span> as follows:</p><pre class="lstlisting"><code class="prettyprint">// dfs from vertex i<br>void dfs(int i) {<br>    // iterate each edge of vertex i that is directed away from it<br>    for(int j = 1; j &lt;= S[i]; j++) {<br>        Z.push_back(W[i][j]); // add the integer in the edge to the end of Z<br>        dfs(L[i][j]); // recurse to the next vertex<br>    }<br>}<br></code></pre><p>Note that the function does not keep track of which vertices have been visited, so each vertex can be processed more than once.</p><p>Let's say Pak Chanek does <span class="tex-font-style-tt">dfs(1)</span> once. After that, Pak Chanek will get an array $Z$ containing some elements $0$ or $1$. Define an inversion in array $Z$ as a pair of indices $(x, y)$ ($x &lt; y$) such that $Z_x &gt; Z_y$. How many different inversions in $Z$ are there if Pak Chanek does <span class="tex-font-style-tt">dfs(1)</span> once? Since the answer can be very big, output the answer modulo $998\,244\,353$.</p></div><div class="input-specification"><p>The first line contains a single integer $N$ ($2 \leq N \leq 10^5$) — the number of vertices in the graph. The following lines contain the description of each vertex from vertex $1$ to vertex $N$.</p><p>The first line of each vertex $i$ contains a single integer $S_i$ ($0 \leq S_i \leq N-1$) — the number of edges directed away from vertex $i$.</p><p>The $j$-th of the next $S_i$ lines of each vertex $i$ contains two integers $L_{i,j}$ and $W_{i,j}$ ($1 \leq L_{i,j} \leq N$; $0 \leq W_{i,j} \leq 1$) — an edge directed away from vertex $i$ that is directed towards vertex $L_{i,j}$ and has an integer $W_{i,j}$. For each $i$, the values of $L_{i,1}$, $L_{i,2}$, ..., $L_{i,S_i}$ are pairwise distinct. </p><p>It is guaranteed that the sum of $S_i$ over all vertices does not exceed $2 \cdot 10^5$. There are no cycles in the graph. Each vertex can be reached from vertex $1$ via zero or more directed edges.</p></div><div class="output-specification"><p>An integer representing the number of inversions in $Z$ if Pak Chanek does <span class="tex-font-style-tt">dfs(1)</span> once. Since the answer can be very big, output the answer modulo $998\,244\,353$.</p></div>

## Input

<p>The first line contains a single integer $N$ ($2 \leq N \leq 10^5$) — the number of vertices in the graph. The following lines contain the description of each vertex from vertex $1$ to vertex $N$.</p><p>The first line of each vertex $i$ contains a single integer $S_i$ ($0 \leq S_i \leq N-1$) — the number of edges directed away from vertex $i$.</p><p>The $j$-th of the next $S_i$ lines of each vertex $i$ contains two integers $L_{i,j}$ and $W_{i,j}$ ($1 \leq L_{i,j} \leq N$; $0 \leq W_{i,j} \leq 1$) — an edge directed away from vertex $i$ that is directed towards vertex $L_{i,j}$ and has an integer $W_{i,j}$. For each $i$, the values of $L_{i,1}$, $L_{i,2}$, ..., $L_{i,S_i}$ are pairwise distinct. </p><p>It is guaranteed that the sum of $S_i$ over all vertices does not exceed $2 \cdot 10^5$. There are no cycles in the graph. Each vertex can be reached from vertex $1$ via zero or more directed edges.</p>

## Output

<p>An integer representing the number of inversions in $Z$ if Pak Chanek does <span class="tex-font-style-tt">dfs(1)</span> once. Since the answer can be very big, output the answer modulo $998\,244\,353$.</p>





```input1
5
2
4 0
3 1
0
1
2 0
2
3 1
5 1
0
```




```output1
4
```



## Note

<p>The following is the <span class="tex-font-style-tt">dfs(1)</span> process on the graph.</p><p> <img class="tex-graphics" src="file://lgEZUjiy.png" style="max-width: 100.0%;max-height: 100.0%;" width="350px"></p><p>In the end, $Z=[0,1,0,1,1,0]$. All of its inversions are $(2,3)$, $(2,6)$, $(4,6)$, and $(5,6)$.</p>
