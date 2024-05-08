## Description

<div><p>You are given an undirected graph with $n$ vertices and $3m$ edges. The graph may contain multi-edges, but does not contain self-loops. </p><p>The graph satisfies the following property: the given edges can be divided into $m$ groups of $3$, such that each group is a triangle.</p><p>A triangle is defined as three edges $(a,b)$, $(b,c)$ and $(c,a)$ for some three distinct vertices $a,b,c$ ($1 \leq a,b,c \leq n$).</p><p>Initially, each vertex $v$ has a non-negative integer weight $a_v$. For every edge $(u,v)$ in the graph, you <span class="tex-font-style-bf">should</span> perform the following operation <span class="tex-font-style-bf">exactly once</span>: </p><ul> <li> Choose an integer $x$ between $1$ and $4$. Then increase both $a_u$ and $a_v$ by $x$. </li></ul><p>After performing all operations, the following requirement should be satisfied: if $u$ and $v$ are connected by an edge, then $a_u \ne a_v$.</p><p>It can be proven this is always possible under the constraints of the task. Output a way to do so, by outputting the choice of $x$ for each edge. It is easy to see that the order of operations does not matter. If there are multiple valid answers, output any. </p><p> </p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \leq t \leq 10^5$) — the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains two integers $n$ and $m$ ($3 \le n \le 10^6$, $1 \le m \le 4 \cdot 10^5$) — denoting the graph have $n$ vertices and $3m$ edges.</p><p>The second line of each test case contains $n$ integers $a_1,a_2,\ldots,a_n$ ($0 \leq a_i \leq 10^6$) — the initial weights of each vertex. </p><p>Then $m$ lines follow. The $i$-th line contains three integers $a_i$, $b_i$, $c_i$ ($1 \leq a_i &lt; b_i &lt; c_i \leq n$) — denotes that three edges $(a_i,b_i)$, $(b_i,c_i)$ and $(c_i,a_i)$. </p><p>Note that the graph may contain multi-edges: a pair $(x,y)$ may appear in multiple triangles.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^6$ and the sum of $m$ over all test cases does not exceed $4 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output $m$ lines of $3$ integers each.</p><p>The $i$-th line should contains three integers $e_{ab},e_{bc},e_{ca}$ ($1 \leq e_{ab}, e_{bc} , e_{ca} \leq 4$), denoting the choice of value $x$ for edges $(a_i, b_i)$, $(b_i,c_i)$ and $(c_i, a_i)$ respectively.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \leq t \leq 10^5$) — the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains two integers $n$ and $m$ ($3 \le n \le 10^6$, $1 \le m \le 4 \cdot 10^5$) — denoting the graph have $n$ vertices and $3m$ edges.</p><p>The second line of each test case contains $n$ integers $a_1,a_2,\ldots,a_n$ ($0 \leq a_i \leq 10^6$) — the initial weights of each vertex. </p><p>Then $m$ lines follow. The $i$-th line contains three integers $a_i$, $b_i$, $c_i$ ($1 \leq a_i &lt; b_i &lt; c_i \leq n$) — denotes that three edges $(a_i,b_i)$, $(b_i,c_i)$ and $(c_i,a_i)$. </p><p>Note that the graph may contain multi-edges: a pair $(x,y)$ may appear in multiple triangles.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^6$ and the sum of $m$ over all test cases does not exceed $4 \cdot 10^5$.</p>

## Output

<p>For each test case, output $m$ lines of $3$ integers each.</p><p>The $i$-th line should contains three integers $e_{ab},e_{bc},e_{ca}$ ($1 \leq e_{ab}, e_{bc} , e_{ca} \leq 4$), denoting the choice of value $x$ for edges $(a_i, b_i)$, $(b_i,c_i)$ and $(c_i, a_i)$ respectively.</p>





```input1|2,3,4,9,10,11,12,13,14
4
4 1
0 0 0 0
1 2 3
5 2
0 0 0 0 0
1 2 3
1 4 5
4 4
3 4 5 6
1 2 3
1 2 4
1 3 4
2 3 4
5 4
0 1000000 412 412 412
1 2 3
1 4 5
2 4 5
3 4 5
```




```output1
2 1 3
2 3 3
4 3 3
3 1 2
2 2 3
2 3 4
3 1 1
2 3 4
1 2 4
4 4 3
4 1 1
```



## Note

<p>In the first test case, the initial weights are $[0,0,0,0]$. We have added values as follows: </p><ul> <li> Added $2$ to vertices $1$ and $2$ </li><li> Added $1$ to vertices $2$ and $3$ </li><li> Added $3$ to vertices $3$ and $1$ </li></ul><p>The final weights are $[5,3,4,0]$. The output is valid because $a_1 \neq a_2$, $a_1 \neq a_3$, $a_2 \neq a_3$, and that all chosen values are between $1$ and $4$.</p><p>In the second test case, the initial weights are $[0,0,0,0,0]$. The weights after the operations are $[12,5,6,7,6]$. The output is valid because $a_1 \neq a_2$, $a_1 \neq a_3$, $a_2 \neq a_3$, and that $a_1 \neq a_4$, $a_1 \neq a_5$, $a_4 \neq a_5$, and that all chosen values are between $1$ and $4$.</p><p>In the third test case, the initial weights are $[3,4,5,6]$. The weights after the operations are $[19,16,17,20]$, and all final weights are distinct, which means no two adjacent vertices have the same weight.</p>
