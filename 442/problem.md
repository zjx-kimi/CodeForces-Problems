## Description

<div><p>Mark loves to move fast. So he made a spaceship that works in $4$-dimensional space. </p><p>He wants to use the spaceship to complete missions as fast as possible. In each mission, the spaceship starts at $(0, 0, 0, 0)$ and needs to end up at $(a, b, c, d)$. To do this, he instructs the spaceship's computer to execute a series of moves, where each move is a unit step in one of the eight cardinal directions: $(\pm 1, 0, 0, 0)$, $(0, \pm 1, 0, 0)$, $(0, 0, \pm 1, 0)$, $(0, 0, 0, \pm 1)$.</p><p>Unfortunately, he also moved fast when building the spaceship, so there is a bug in the spaceship's code. The first move will be executed once, the second move will be executed twice, the third move will be executed thrice, and so on. In general, the $i$-th move will be executed $i$ times.</p><p>For any four integers $a, b, c, d$, let $f(a, b, c, d)$ be the minimum number of moves of a mission that ends up at $(a, b, c, d)$. Compute the sum of $f(a, b, c, d)$ over all points (with integer coordinates) such that $-A\le a\le A$, $-B\le b\le B$, $-C\le c\le C$, $-D\le d\le D$.</p></div><div class="input-specification"><p>The only line of the input contains the four integers $A, B, C, D$ ($0\le A,B,C,D\le 1000$).</p></div><div class="output-specification"><p>Print the sum of $f(a, b, c, d)$ over the set of points described in the statement.</p></div>

## Input

<p>The only line of the input contains the four integers $A, B, C, D$ ($0\le A,B,C,D\le 1000$).</p>

## Output

<p>Print the sum of $f(a, b, c, d)$ over the set of points described in the statement.</p>





```input1
1 0 0 0
```




```input2
1 1 0 1
```




```input3
3 2 4 1
```




```output1
2
```




```output2
82
```




```output3
4616
```



## Note

<p>In the first sample, one has to compute $f(-1, 0, 0, 0)+f(0, 0, 0, 0) + f(1, 0, 0, 0) = 1 + 0 + 1 = 2$.</p><p>In the second sample, one has to compute the sum of $f(a, b, c, d)$ over $27$ different points $(a, b, c, d)$. Let us describe the value of $f(a, b, c, d)$ for some of them:</p><ul> <li> It holds $f(-1, 0, 0, -1)=3$ and it may be achieved with the following sequence of moves (an arrow $\xrightarrow{\pm i}$ denotes that the move is performed on the $i$-th coordinate): $$(0, 0, 0, 0) \xrightarrow{-1} (-1, 0, 0, 0) \xrightarrow{+4} (-1, 0, 0, 2) \xrightarrow{-4} (-1, 0, 0, -1).$$ </li><li> It holds $f(1, 1, 0, 1) = 5$ and it may be achieved with the following sequence of moves: $$(0, 0, 0, 0) \xrightarrow{+1} (1, 0, 0, 0) \xrightarrow{-2} (1, -2, 0, 0) \xrightarrow{+2} (1, 1, 0, 0) \xrightarrow{-4} (1, 1, 0, -4) \xrightarrow{+4} (1, 1, 0, 1).$$ </li></ul><p>In the third sample, one has to compute the sum of $f(a, b, c, d)$ over $7\cdot5\cdot 9\cdot 3$ points. One of them is $(3, 2, 4, 1)$. It holds $f(3, 2, 4, 1) = 4$ and it may be achieved with the following sequence of moves: $$(0, 0, 0, 0) \xrightarrow{+4} (0, 0, 0, 1) \xrightarrow{+2} (0, 2, 0, 1) \xrightarrow{+1} (3, 2, 0, 1) \xrightarrow{+3} (3, 2, 4, 1).$$</p>
