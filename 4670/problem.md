## Description

<div><p>Elena has a grid formed by $n$ horizontal lines and $m$ vertical lines. The horizontal lines are numbered by integers from $1$ to $n$ from top to bottom. The vertical lines are numbered by integers from $1$ to $m$ from left to right. For each $x$ and $y$ ($1 \leq x \leq n$, $1 \leq y \leq m$), the notation $(x, y)$ denotes the point at the intersection of the $x$-th horizontal line and $y$-th vertical line.</p><p>Two points $(x_1,y_1)$ and $(x_2,y_2)$ are adjacent if and only if $|x_1-x_2| + |y_1-y_2| = 1$.</p><center> <img class="tex-graphics" src="file://lF8ia6xh.png" style="max-width: 100.0%;max-height: 100.0%;">   <span class="tex-font-size-small">The grid formed by $n=4$ horizontal lines and $m=5$ vertical lines.</span> </center><p>Elena calls a sequence of points $p_1, p_2, \ldots, p_g$ of length $g$ a <span class="tex-font-style-it">walk</span> if and only if all the following conditions hold: </p><ul> <li> The first point $p_1$ in this sequence is $(1, 1)$. </li><li> The last point $p_g$ in this sequence is $(n, m)$. </li><li> For each $1 \le i &lt; g$, the points $p_i$ and $p_{i+1}$ are adjacent. </li></ul><p>Note that the walk may contain the same point more than once. In particular, it may contain point $(1, 1)$ or $(n, m)$ multiple times.</p><p>There are $n(m-1)+(n-1)m$ segments connecting the adjacent points in Elena's grid. Elena wants to color each of these segments in blue or red color so that there exists a walk $p_1, p_2, \ldots, p_{k+1}$ of length $k+1$ such that </p><ul> <li> out of $k$ segments connecting two consecutive points in this walk, no two consecutive segments have the same color (in other words, for each $1 \le i &lt; k$, the color of the segment between points $p_i$ and $p_{i+1}$ differs from the color of the segment between points $p_{i+1}$ and $p_{i+2}$). </li></ul><p>Please find any such coloring or report that there is no such coloring.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \leq t \leq 32$). The description of test cases follows.</p><p>The only line of each test case contains three integers $n$, $m$, and $k$ ($3 \leq n,m \leq 16$, $1 \leq k \leq 10^9$)&nbsp;— the dimensions of the grid and the number of segments in the walk Elena is looking for.</p></div><div class="output-specification"><p>For each test case, output "<span class="tex-font-style-tt">NO</span>" if it is not possible to color each of the $n(m-1)+(n-1)m$ segments in blue or red color, so that there exists a walk of length $k+1$ satisfying the condition from the statement.</p><p>Otherwise, output in the first line "<span class="tex-font-style-tt">YES</span>", and then provide the required coloring.</p><p>In each of the first $n$ lines of coloring description, output $m-1$ space-separated characters. The $j$-th character in the $i$-th of these $n$ lines should denote the color of the segment between points $(i,j)$ and $(i,j+1)$. Here, use '<span class="tex-font-style-tt">B</span>' to denote the blue color and '<span class="tex-font-style-tt">R</span>' to denote the red color.</p><p>In each of the next $n-1$ lines of coloring description, output $m$ space-separated characters. The $j$-th character in the $i$-th of these $n-1$ lines should denote the color of the segment between points $(i,j)$ and $(i+1,j)$. Similarly, use '<span class="tex-font-style-tt">B</span>' to denote the blue color and '<span class="tex-font-style-tt">R</span>' to denote the red color.</p><p>You can output each letter in the answer in any case (upper or lower). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as positive responses, and both '<span class="tex-font-style-tt">R</span>' and '<span class="tex-font-style-tt">r</span>' are valid notation of red.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \leq t \leq 32$). The description of test cases follows.</p><p>The only line of each test case contains three integers $n$, $m$, and $k$ ($3 \leq n,m \leq 16$, $1 \leq k \leq 10^9$)&nbsp;— the dimensions of the grid and the number of segments in the walk Elena is looking for.</p>

## Output

<p>For each test case, output "<span class="tex-font-style-tt">NO</span>" if it is not possible to color each of the $n(m-1)+(n-1)m$ segments in blue or red color, so that there exists a walk of length $k+1$ satisfying the condition from the statement.</p><p>Otherwise, output in the first line "<span class="tex-font-style-tt">YES</span>", and then provide the required coloring.</p><p>In each of the first $n$ lines of coloring description, output $m-1$ space-separated characters. The $j$-th character in the $i$-th of these $n$ lines should denote the color of the segment between points $(i,j)$ and $(i,j+1)$. Here, use '<span class="tex-font-style-tt">B</span>' to denote the blue color and '<span class="tex-font-style-tt">R</span>' to denote the red color.</p><p>In each of the next $n-1$ lines of coloring description, output $m$ space-separated characters. The $j$-th character in the $i$-th of these $n-1$ lines should denote the color of the segment between points $(i,j)$ and $(i+1,j)$. Similarly, use '<span class="tex-font-style-tt">B</span>' to denote the blue color and '<span class="tex-font-style-tt">R</span>' to denote the red color.</p><p>You can output each letter in the answer in any case (upper or lower). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as positive responses, and both '<span class="tex-font-style-tt">R</span>' and '<span class="tex-font-style-tt">r</span>' are valid notation of red.</p>





```input1|2,4,6
5
4 5 11
3 3 2
3 4 1000000000
3 3 12588
4 4 8
```




```output1
YES
R R B B
R R R R
B B B R
R R B B
R B B R B
R B B B B
B B R R R
NO
NO
YES
R B
B B
B R
B B R
R B B
YES
B B R
R B R
B R R
R R B
B R R B
B B B B
B R R R
```



## Note

<p>In the first test case, one of the correct answers is shown in the picture below. The color-alternating walk of length $12$ is highlighted.</p><center> <img class="tex-graphics" src="file://yDxLMJ9n.png" style="max-width: 100.0%;max-height: 100.0%;">   </center><p>In the second and the third test cases, it can be shown that there is no coloring satisfying the condition from the statement.</p>
