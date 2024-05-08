## Description

<div><p>Doremy has an edge-weighted tree with $n$ vertices whose weights are <span class="tex-font-style-bf">integers</span> between $1$ and $10^9$. She does $\frac{n(n+1)}{2}$ experiments on it.</p><p>In each experiment, Doremy chooses vertices $i$ and $j$ such that $j \leq i$ and connects them directly with an edge with weight $1$. Then, there is exactly one cycle (or self-loop when $i=j$) in the graph. Doremy defines $f(i,j)$ as the sum of lengths of shortest paths from every vertex to the cycle.</p><p>Formally, let $\mathrm{dis}_{i,j}(x,y)$ be the length of the shortest path between vertex $x$ and $y$ when the edge $(i,j)$ of weight $1$ is added, and $S_{i,j}$ be the set of vertices that are on the cycle when edge $(i,j)$ is added. Then,</p><p>$$ f(i,j)=\sum_{x=1}^{n}\left(\min_{y\in S_{i,j}}\mathrm{dis}_{i,j}(x,y)\right). $$</p><p>Doremy writes down all values of $f(i,j)$ such that $1 \leq j \leq i \leq n$, then goes to sleep. However, after waking up, she finds that the tree has gone missing. Fortunately, the values of $f(i,j)$ are still in her notebook, and she knows which $i$ and $j$ they belong to. Given the values of $f(i,j)$, can you help her restore the tree?</p><p>It is guaranteed that at least one suitable tree exists.</p></div><div class="input-specification"><p>The first line of input contains a single integer $n$ ($2 \le n \le 2000$)&nbsp;— the number of vertices in the tree.</p><p>The following $n$ lines contain a lower-triangular matrix with $i$ integers on the $i$-th line; the $j$-th integer on the $i$-th line is $f(i,j)$ ($0 \le f(i,j) \le 2\cdot 10^{15}$).</p><p>It is guaranteed that there exists a tree whose weights are integers between $1$ and $10^9$ such that the values of $f(i,j)$ of the tree match those given in the input.</p></div><div class="output-specification"><p>Print $n-1$ lines describing the tree. In the $i$-th line of the output, output three integers $u_i$, $v_i$, $w_i$ ($1 \le u_i,v_i \le n$, $1 \le w_i \le 10^9$), representing an edge $(u_i,v_i)$ whose weight is $w_i$.</p><p>If there are multiple answers, you may output any.</p><p>All edges must form a tree and all values of $f(i,j)$ must match those given in the input.</p></div>

## Input

<p>The first line of input contains a single integer $n$ ($2 \le n \le 2000$)&nbsp;— the number of vertices in the tree.</p><p>The following $n$ lines contain a lower-triangular matrix with $i$ integers on the $i$-th line; the $j$-th integer on the $i$-th line is $f(i,j)$ ($0 \le f(i,j) \le 2\cdot 10^{15}$).</p><p>It is guaranteed that there exists a tree whose weights are integers between $1$ and $10^9$ such that the values of $f(i,j)$ of the tree match those given in the input.</p>

## Output

<p>Print $n-1$ lines describing the tree. In the $i$-th line of the output, output three integers $u_i$, $v_i$, $w_i$ ($1 \le u_i,v_i \le n$, $1 \le w_i \le 10^9$), representing an edge $(u_i,v_i)$ whose weight is $w_i$.</p><p>If there are multiple answers, you may output any.</p><p>All edges must form a tree and all values of $f(i,j)$ must match those given in the input.</p>





```input1
3
7
3 5
0 2 8
```




```input2
9
8081910646
8081902766 8081903751
8081902555 8081903540 8081905228
3090681001 3090681986 3090681775 7083659398
7083657913 7083658898 7083658687 2092437133 15069617722
1748216295 1748217280 1748217069 5741194692 749972427 10439821163
2377558289 2377559274 2377559063 6370536686 1379314421 5028071980 8866466178
1746983932 1746984917 1746984706 5739962329 748740064 10438588800 5026839617 10448447704
2341942133 2341943118 2341942907 6334920530 1343698265 4992455824 8830850022 4991223461 9115779270
```




```output1
2 3 3
1 2 2
```




```output2
1 2 985
2 3 211
2 4 998244353
2 5 998244853
4 6 671232353
6 8 1232363
4 7 356561356
7 9 35616156
```



## Note

<p>In the first test case, the picture below, from left to right, from top to bottom, shows the graph when pairs $(1,1)$, $(1,2)$, $(1,3)$, $(2,2)$, $(2,3)$, $(3,3)$ are connected with an edge, respectively. The nodes colored yellow are on the cycle.</p><p><img class="tex-graphics" src="file://gQa9QwNF.png" style="max-width: 100.0%;max-height: 100.0%;"></p>
