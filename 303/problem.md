## Description

<div><p><span class="tex-font-style-bf">This is an interactive problem. Remember to flush your output while communicating with the testing program.</span> You may use <span class="tex-font-style-tt">fflush(stdout)</span> in C++, <span class="tex-font-style-tt">system.out.flush()</span> in Java, <span class="tex-font-style-tt">stdout.flush()</span> in Python or <span class="tex-font-style-tt">flush(output)</span> in Pascal to flush the output. If you use some other programming language, consult its documentation. You may also refer to the guide on interactive problems: <a href="https://codeforces.com/blog/entry/45307">https://codeforces.com/blog/entry/45307</a>.</p><p>You are given a tree on $n$ vertices; vertex $1$ is the root of the tree. For every $i \in [2, n]$, the parent of the $i$-th vertex is $p_i$, and $p_i &lt; i$.</p><p>You have to color all edges of the tree using the <span class="tex-font-style-bf">minimum possible number of colors</span> such that you can win the game on that tree (every edge should be painted into exactly one color).</p><p>The game we're going to play will be conducted as follows. After you paint the edges and print their colors, the jury will place a chip into one of the vertices of the tree (except for the root). Your goal is to move this chip to the root in exactly $d$ moves, where $d$ is the distance from the root to that vertex (the distance is equal to the number of edges on the path). If the chip reaches the root in $d$ moves, you win. Otherwise, you lose.</p><p>The jury won't tell you where the chip is located. You won't even know the value of $d$ in advance. However, at the start of each move, you will be told how many edges of each color are incident to the current vertex (this includes both the edge leading up the tree and the edges leading away from the root). You have to choose one of these colors, and the chip will be moved along the edge of the chosen color (if there are multiple edges with that color incident to the current vertex, the jury gets to choose one of them). After the chip is moved, you will be told the same information about the current vertex again, and the game continues, until you either reach the root, or you make $d$ moves without reaching the root.</p><p><span class="tex-font-style-bf">The interactor for this problem is adaptive</span>. It means that both the starting vertex and the current vertex are <span class="tex-font-style-bf">not fixed</span> and may change "on the run" depending on the output of your program. However, the state of the game will always be consistent with the information you are given: <span class="tex-font-style-bf">there will always be at least one starting vertex and at least one path of your chip from that vertex consistent with both the information about the colors you receive and the colors you've chosen during the moves</span>.</p></div><div class="input-specification"><p>The first line contains one integer $n$ ($3 \le n \le 100$) — the number of vertices in the tree.</p><p>The second line contains $n-1$ integers $p_2, p_3, \dots, p_n$ ($1 \le p_i &lt; i$), where $p_i$ is the parent of the $i$-th vertex in the tree.</p></div><div><h2>Interaction</h2><p>First, you have to print the coloring of the edges you've chosen as follows:</p><ul> <li> in the first line, print one integer $k$ ($1 \le k \le n - 1$) — the number of colors you are using; </li><li> in the second line, print $n-1$ integers $c_2, c_3, \dots, c_n$ ($1 \le c_i \le k$), where $c_i$ should be the color of the edge connecting $p_i$ with $i$. </li></ul><p>Then, the game begins. At the start of each move, the jury program prints one of the following:</p><ul> <li> one integer $1$ on a separate line, indicating that the chip has reached the root and you won; </li><li> one integer $-1$ on a separate line, indicating that either you didn't reach the root in $d$ moves and lost, or you have done something incorrect (either the coloring you provided didn't meet the constraints, or your previous move is impossible); </li><li> or one integer $0$ on a separate line, followed by a line containing $k$ integers $e_1, e_2, \dots, e_k$, where $e_i$ is the number of edges with color $i$ incident to the current vertex. </li></ul><p>If you receive $1$ or $-1$, your program should terminate immediately, otherwise the verdict for your submission may be undefined. If you receive $0$ followed by $k$ integers $e_1, e_2, \dots, e_k$, you have to print one integer indicating the color you choose during the move (of course, $e_i$ for that color should not be equal to $0$).</p><p>Don't forget to flush the output every time you print something!</p></div>

## Input

<p>The first line contains one integer $n$ ($3 \le n \le 100$) — the number of vertices in the tree.</p><p>The second line contains $n-1$ integers $p_2, p_3, \dots, p_n$ ($1 \le p_i &lt; i$), where $p_i$ is the parent of the $i$-th vertex in the tree.</p>





```input1
5
1 1 1 1
0
1
1
```




```input2
4
1 2 3
0
0 1 0
0
1 1 0
0
1 0 1
1
```




```input3
3
1 2
0
1 1
1
```




```output1
1
1 1 1 1
1
```




```output2
3
3 1 2
2
1
3
```




```output3
2
1 2
1
```



## Note

<p>In the first example, every vertex from $2$ to $n$ is connected to the root. So, we can paint all edges into the same color $1$, and when the game starts, there will be only one edge incident to the current vertex (and it will lead to the root).</p><p>In the second example, the tree is a path of $4$ vertices. We have to paint its edges into different colors, because it can be shown that we don't have a winning strategy with just two colors.</p>
