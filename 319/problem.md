## Description

<div><p>With a problem title like that, there is no way this is going to be a graph problem.</p><p>Chaneka has a graph with $n$ vertices and $n-1$ edges. Some of the edges are directed and some of the edges are undirected. Edge $i$ connects vertex $u_i$ to vertex $v_i$. If $t_i=0$, edge $i$ is undirected. If $t_i=1$, edge $i$ is directed in the direction from $u_i$ to $v_i$. It is known that if you make all edges undirected, the graph becomes a tree$^\dagger$.</p><p>Chaneka wants to direct all undirected edges and colour each edge (different edges can have the same colour).</p><p>After doing that, suppose Chaneka starts a walk from an arbitrary vertex $x$ to an arbitrary vertex $y$ (it is possible that $x=y$) going through one or more edges. She is allowed to go through each edge either following the direction or opposite to the direction of the edge. She is also allowed to visit a vertex or an edge more than once. During the walk, Chaneka maintains a stack of balls that is initially empty before the walk. Each time Chaneka goes through an edge, she does the following: </p><ul> <li> If Chaneka goes through it in the right direction, she puts a new ball with a colour that is the same as the edge's colour to the top of the stack. </li><li> If Chaneka goes through it in the opposite direction, she removes the ball that is on the top of the stack. </li></ul><p>A walk is <span class="tex-font-style-bf">stackable</span> if and only if the stack is not empty before each time Chaneka goes through an edge in the opposite direction.</p><p>A walk is <span class="tex-font-style-bf">ball-stackable</span> if and only if it is stackable and each time Chaneka goes through an edge in the opposite direction, the colour of the ball removed from the stack is the same as the colour of the edge traversed.</p><p>Is it possible to direct all undirected edges and colour each edge such that all stackable walks are also ball-stackable? If it is possible, find a construction example that uses the <span class="tex-font-style-bf">maximum number of different colours</span> among all valid ways of directing and colouring. If there are multiple such solutions, output any of them.</p><p>$^\dagger$ A tree is a connected graph with no cycles.</p></div><div class="input-specification"><p>The first line contains a single integer $n$ ($2\leq n\leq10^5$) — the number of vertices in the graph.</p><p>The $i$-th of the next $n-1$ lines contains three integers $u_i$, $v_i$, and $t_i$ ($1 \leq u_i,v_i \leq n$; $0\leq t_i\leq1$) — an undirected edge connecting vectices $u_i$ and $v_i$ if $t_i=0$, or a directed edge from vertex $u_i$ to vertex $v_i$ if $t_i=1$. If you make all edges undirected, the graph becomes a tree.</p></div><div class="output-specification"><p>A single line containing $-1$ if it is impossible.</p><p>Otherwise, the output consists of $n$ lines describing your construction. The first line contains an integer $z$ representing the number of different colours used. The $i$-th of the next $n-1$ lines contains three integers $p$, $q$, and $c$ ($1\leq p,q\leq n$; $1\leq c\leq z$) — the edge connecting vertices $p$ and $q$ in the graph is directed from vertex $p$ to vertex $q$ and is coloured with colour $c$. If there are multiple such solutions, output any of them.</p><p>Note that since there should be $z$ different colours in your construction, that means each colour from $1$ to $z$ must appear at least once in the graph.</p></div>

## Input

<p>The first line contains a single integer $n$ ($2\leq n\leq10^5$) — the number of vertices in the graph.</p><p>The $i$-th of the next $n-1$ lines contains three integers $u_i$, $v_i$, and $t_i$ ($1 \leq u_i,v_i \leq n$; $0\leq t_i\leq1$) — an undirected edge connecting vectices $u_i$ and $v_i$ if $t_i=0$, or a directed edge from vertex $u_i$ to vertex $v_i$ if $t_i=1$. If you make all edges undirected, the graph becomes a tree.</p>

## Output

<p>A single line containing $-1$ if it is impossible.</p><p>Otherwise, the output consists of $n$ lines describing your construction. The first line contains an integer $z$ representing the number of different colours used. The $i$-th of the next $n-1$ lines contains three integers $p$, $q$, and $c$ ($1\leq p,q\leq n$; $1\leq c\leq z$) — the edge connecting vertices $p$ and $q$ in the graph is directed from vertex $p$ to vertex $q$ and is coloured with colour $c$. If there are multiple such solutions, output any of them.</p><p>Note that since there should be $z$ different colours in your construction, that means each colour from $1$ to $z$ must appear at least once in the graph.</p>





```input1
5
2 5 1
1 3 0
5 4 0
1 5 1
```




```output1
3
1 5 2
5 4 1
2 5 2
3 1 3
```



## Note

<p>The following is the given graph.</p><p> <img class="tex-graphics" src="file://9xDNR5Yt.png" style="max-width: 100.0%;max-height: 100.0%;" width="350px"></p><p>Chaneka can direct all undirected edges and colour each edge as follows.</p><p> <img class="tex-graphics" src="file://WB1R9FlV.png" style="max-width: 100.0%;max-height: 100.0%;" width="350px"></p><p>As an example, consider a stackable walk $3→1→5→2→5→4→5$. Let's show that that walk is ball-stackable. </p><ol> <li> Chaneka starts in vertex $3$. The stack is $[]$. </li><li> Chaneka moves to vertex $1$. She puts a ball of colour $3$. The stack is $[3]$. </li><li> Chaneka moves to vertex $5$. She puts a ball of colour $2$. The stack is $[3,2]$. </li><li> Chaneka moves to vertex $2$. She removes a ball of colour $2$ (same colour as the edge). The stack is $[3]$. </li><li> Chaneka moves to vertex $5$. She puts a ball of colour $2$. The stack is $[3,2]$. </li><li> Chaneka moves to vertex $4$. She puts a ball of colour $1$. The stack is $[3,2,1]$. </li><li> Chaneka moves to vertex $5$. She removes a ball of colour $1$ (same colour as the edge). The stack is $[3,2]$. </li></ol><p>Since every time Chaneka removes a ball from the stack, it has the same colour as the edge traversed, then the walk above is ball-stackable. It can be shown that if we direct and colour the edges as shown above, any possible stackable walk is also ball-stackable.</p>
