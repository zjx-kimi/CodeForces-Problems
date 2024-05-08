## Description

<div><p><span class="tex-font-style-bf">This problem has an attachment. You can use it to simulate and visualize the movements of the amoeba.</span></p><p>Amoeba Amanda lives inside a rectangular grid of square pixels. Her body occupies some of these pixels. Other pixels may be either free or blocked. Amanda moves across the grid using the so-called amoeboid movement. In each step of such a movement, her body first shrinks by one pixel (one pixel of the body is removed and becomes free), and then grows at a different place (one previously-free pixel is added to the body).</p><p>To prevent structural damage, Amanda's body always occupies a connected region of pixels, which means that any pair of pixels forming the body can be connected by a sequence of adjacent pixels without ever leaving the body. Two pixels are considered adjacent if they share a common side (each pixel has at most 4 neighbours). The body remains connected even during the movement, including the moment after removing a pixel and before adding another one.</p><p>Your task is to help Amanda find her way around. Given her initial position and desired final position, suggest a sequence of valid moves leading from the former to the latter.</p><center> <img class="tex-graphics" src="file://hEluaDIU.png" style="max-width: 100.0%;max-height: 100.0%;">   <span class="tex-font-size-small">Illustration of sample $1$: The filled shape is the initial position, the dotted region is the final position.</span> </center></div><div class="input-specification"><p>The first line contains two integers $r$ and $c$ ($1\le r,c \le 50$)&nbsp;— the size of the rectangular grid in pixels.</p><p>The next $r$ lines contain $c$ characters each, describing the initial position of Amanda. Each of those characters is either a dot $\texttt{.}$ denoting a free pixel, an asterisk $\texttt{*}$ denoting Amanda's body, or an $\texttt{X}$ denoting a blocked pixel which may never be occupied.</p><p>The next line is empty.</p><p>The next $r$ lines describe the desired final position in the same format as the initial position.</p><p>It is guaranteed that: </p><ul> <li> The number of pixels forming Amanda's body is the same in both positions, and it is at least 2. </li><li> The body of Amanda is connected in the initial position. </li><li> The body of Amanda is connected in the final position. </li><li> The blocked pixels do not change between the descriptions of the initial and final position, their placement is exactly the same in both positions. </li></ul></div><div class="output-specification"><p>Print $\texttt{YES}$ if it is possible for Amanda to go from the initial position to the final one. Otherwise, print $\texttt{NO}$.</p><p>If it is possible, on the next line print one integer $m$ ($0\le m\le 10\,000$)&nbsp;— the number of moves to execute.</p><p>The following $m$ lines must contain four integer coordinates each: $i_1$, $j_1$, $i_2$, $j_2$ ($1\le i_1,i_2\le r$, $1\le j_1,j_2\le c$). These four coordinates specify one move, meaning that the pixel at $i_1$-th row and $j_1$-th column is first removed from the body. Then, $(i_2,j_2)$ must designate a <span class="tex-font-style-bf">different</span> location where one pixel is added.</p><p>The sequence should consist only of valid moves and after the last move, Amanda's body should occupy the desired final position.</p><p>If there are multiple solutions, print any of them.</p><p>Under the assumptions of this problem, it can be proven that if it is possible for Amanda to go from the initial position to the desired final one, then it is possible to do it with at most $10\,000$ moves.</p></div>

## Input

<p>The first line contains two integers $r$ and $c$ ($1\le r,c \le 50$)&nbsp;— the size of the rectangular grid in pixels.</p><p>The next $r$ lines contain $c$ characters each, describing the initial position of Amanda. Each of those characters is either a dot $\texttt{.}$ denoting a free pixel, an asterisk $\texttt{*}$ denoting Amanda's body, or an $\texttt{X}$ denoting a blocked pixel which may never be occupied.</p><p>The next line is empty.</p><p>The next $r$ lines describe the desired final position in the same format as the initial position.</p><p>It is guaranteed that: </p><ul> <li> The number of pixels forming Amanda's body is the same in both positions, and it is at least 2. </li><li> The body of Amanda is connected in the initial position. </li><li> The body of Amanda is connected in the final position. </li><li> The blocked pixels do not change between the descriptions of the initial and final position, their placement is exactly the same in both positions. </li></ul>

## Output

<p>Print $\texttt{YES}$ if it is possible for Amanda to go from the initial position to the final one. Otherwise, print $\texttt{NO}$.</p><p>If it is possible, on the next line print one integer $m$ ($0\le m\le 10\,000$)&nbsp;— the number of moves to execute.</p><p>The following $m$ lines must contain four integer coordinates each: $i_1$, $j_1$, $i_2$, $j_2$ ($1\le i_1,i_2\le r$, $1\le j_1,j_2\le c$). These four coordinates specify one move, meaning that the pixel at $i_1$-th row and $j_1$-th column is first removed from the body. Then, $(i_2,j_2)$ must designate a <span class="tex-font-style-bf">different</span> location where one pixel is added.</p><p>The sequence should consist only of valid moves and after the last move, Amanda's body should occupy the desired final position.</p><p>If there are multiple solutions, print any of them.</p><p>Under the assumptions of this problem, it can be proven that if it is possible for Amanda to go from the initial position to the desired final one, then it is possible to do it with at most $10\,000$ moves.</p>





```input1|
5 8
.******.
**.X**..
*******.
**.X**..
.******.
<br>
.******.
...X****
.*******
...X****
.******.
```




```input2|
2 5
*.X..
**X..
<br>
..X**
..X*.
```




```output1
YES
5
3 1 3 8
2 1 2 8
4 1 4 8
2 2 4 7
4 2 2 7
```




```output2
NO
```



## Note

<p>In the <span class="tex-font-style-bf">first sample</span>, Amanda executes 5 moves to reach the final position, as shown in the figure below. </p><center> <img class="tex-graphics" src="file://khW8d0Rm.png" style="max-width: 100.0%;max-height: 100.0%;"> </center>
