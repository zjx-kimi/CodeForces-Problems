## Description

<div><p>You are given an unweighted tree of $n$ vertices numbered from $1$ to $n$ and a list of $n-1$ integers $a_1, a_2, \ldots, a_{n-1}$. A tree is a connected undirected graph without cycles. You will use each element of the list to label one vertex. No vertex should be labeled twice. You can label the only remaining unlabeled vertex with any integer. </p><p>A vertex $x$ is called <span class="tex-font-style-it">good</span> if it is possible to do this labeling so that for each vertex $i$, its label is the distance between $x$ and $i$. The distance between two vertices $s$ and $t$ on a tree is the minimum number of edges on a path that starts at vertex $s$ and ends at vertex $t$. </p><p>Find all good vertices.</p></div><div class="input-specification"><p>The first line contains one integer $n$ ($2\le n\le 2\cdot 10^5$) — the number of vertices in the tree.</p><p>The second line contains $n - 1$ integers $a_1,a_2,\ldots,a_{n-1}$ ($0\le a_i &lt; n$)&nbsp;— the given list.</p><p>Then, $n−1$ lines follow. Each of them contains two integers $u$ and $v$ ($1\le u,v\le n$) denoting an edge between vertices $u$ and $v$. It is guaranteed that the edges form a tree.</p></div><div class="output-specification"><p>In the first line print the number of good vertices.</p><p>In the second line, print the indices of all good vertices <span class="tex-font-style-bf">in ascending order</span>.</p></div>

## Input

<p>The first line contains one integer $n$ ($2\le n\le 2\cdot 10^5$) — the number of vertices in the tree.</p><p>The second line contains $n - 1$ integers $a_1,a_2,\ldots,a_{n-1}$ ($0\le a_i &lt; n$)&nbsp;— the given list.</p><p>Then, $n−1$ lines follow. Each of them contains two integers $u$ and $v$ ($1\le u,v\le n$) denoting an edge between vertices $u$ and $v$. It is guaranteed that the edges form a tree.</p>

## Output

<p>In the first line print the number of good vertices.</p><p>In the second line, print the indices of all good vertices <span class="tex-font-style-bf">in ascending order</span>.</p>





```input1
6
2 1 0 1 2
1 2
2 3
2 4
4 5
4 6
```




```input2
5
1 2 1 2
1 2
3 2
3 4
5 4
```




```input3
3
2 2
1 2
2 3
```




```output1
2
2 4
```




```output2
1
3
```




```output3
0
```



## Note

<p>This is the tree for the first example: </p><center> <img class="tex-graphics" src="file://diRdSo0t.png" style="max-width: 100.0%;max-height: 100.0%;" width="454px"> </center><p>And these are two possible labelings with the elements on the list so that $2$ is a good vertex (left) and $4$ is a good vertex (right).</p><center> <img class="tex-graphics" src="file://ej4118bA.png" style="max-width: 100.0%;max-height: 100.0%;" width="907px"> </center><p>The square below each vertex represents its label. The black squares contain the numbers which were on the given list and the only white square contains the only number which was not on the given list.</p><p>In the second example, the only good vertex is vertex $3$.</p><p>In the third example, there are no good vertices.</p>
