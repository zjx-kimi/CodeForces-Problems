## Description

<div><p>Tenzing has an undirected tree of $n$ vertices.</p><p>Define the <span class="tex-font-style-it">value</span> of a tree with black and white vertices in the following way. The <span class="tex-font-style-it">value</span> of an edge is the absolute difference between the number of black nodes in the two components of the tree after deleting the edge. The value of the tree is the sum of values over all edges.</p><p>For all $k$ such that $0 \leq k \leq n$, Tenzing wants to know the maximum value of the tree when $k$ vertices are painted black and $n-k$ vertices are painted white.</p></div><div class="input-specification"><p>The first line of the input contains a single integer $n$ ($1\leq n\leq 5000$)&nbsp;— the number of vertices.</p><p>The following $n-1$ lines of the input contains $2$ integers $u_i$ and $v_i$ ($1 \leq u_i, v_i \leq n, u_i \neq v_i$)&nbsp;— indicating an edge between vertices $u_i$ and $v_i$. It is guaranteed that the given edges form a tree.</p></div><div class="output-specification"><p>Output $n+1$ numbers. The $i$-th number is the answer of $k=i-1$.</p></div>

## Input

<p>The first line of the input contains a single integer $n$ ($1\leq n\leq 5000$)&nbsp;— the number of vertices.</p><p>The following $n-1$ lines of the input contains $2$ integers $u_i$ and $v_i$ ($1 \leq u_i, v_i \leq n, u_i \neq v_i$)&nbsp;— indicating an edge between vertices $u_i$ and $v_i$. It is guaranteed that the given edges form a tree.</p>

## Output

<p>Output $n+1$ numbers. The $i$-th number is the answer of $k=i-1$.</p>





```input1
4
1 2
3 2
2 4
```




```input2
1
```




```output1
0 3 4 5 6
```




```output2
0 0
```



## Note

<p>Consider the first example. When $k=2$, Tenzing can paint vertices $1$ and $2$ black then the value of edge $(1,2)$ is 0, and the values of other edges are all equal to $2$. So the value of that tree is $4$.</p>
