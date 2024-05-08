## Description

<div><p>The world is a grid with $n$ rows and $m$ columns. The rows are numbered $0, 1, \ldots, n-1$, while the columns are numbered $0, 1, \ldots, m-1$. In this world, the columns are <span class="tex-font-style-bf">cyclic</span> (i.e. the top and the bottom cells in each column are adjacent). The cell on the $i$-th row and the $j$-th column ($0 \le i &lt; n, 0 \le j &lt; m$) is denoted as $(i,j)$. </p><p><span class="tex-font-style-bf">At time $0$</span>, the cell $(i,j)$ (where $0 \le i &lt; n, 0 \le j &lt; m$) contains either a <span class="tex-font-style-bf">rock</span> or <span class="tex-font-style-bf">nothing</span>. The state of cell $(i,j)$ can be described using the integer $a_{i,j}$: </p><ul> <li> If $a_{i,j} = 1$, there is a rock at $(i,j)$. </li><li> If $a_{i,j} = 0$, there is nothing at $(i,j)$. </li></ul><p>As a result of aftershocks from the earthquake, the columns follow tectonic plate movements: each column moves cyclically <span class="tex-font-style-bf">upwards</span> at a velocity of $1$ cell per unit of time. Formally, for some $0 \le i &lt; n, 0 \le j &lt; m$, if $(i,j)$ contains a rock at the moment, it will move from $(i, j)$ to $(i - 1, j)$ (or to $(n - 1, j)$ if $i=0$). </p><p>The robot called RT is initially positioned at $(0,0)$. It has to go to $(n-1,m-1)$ to carry out an earthquake rescue operation (to the bottom rightmost cell). The earthquake doesn't change the position of the robot, they only change the position of rocks in the world.</p><p>Let RT's current position be $(x,y)$ ($0 \le x &lt; n, 0 \le y &lt; m$), it can perform the following operations: </p><ul> <li> Go one cell cyclically upwards, i.e. from $(x,y)$ to $((x+n-1) \bmod n, y)$ using $1$ unit of time. </li><li> Go one cell cyclically downwards, i.e. $(x,y)$ to $((x+1) \bmod n, y)$ using $1$ unit of time. </li><li> Go one cell to the right, i.e. $(x,y)$ to $(x, y+1)$ using $1$ unit of time. (RT may perform this operation only if $y &lt; m-1$.) </li></ul><p><span class="tex-font-style-bf">Note that RT cannot go left using the operations nor can he stay at a position.</span></p><p>Unfortunately, RT will explode upon colliding with a rock. As such, when RT is at $(x,y)$ and there is a rock at $((x+1) \bmod n, y)$ or $((x+2) \bmod n, y)$, RT cannot move down or it will be hit by the rock. </p><center> <img class="tex-graphics" src="file://RqcCRfui.png" style="max-width: 100.0%;max-height: 100.0%;"> </center><p>Similarly, if $y+1 &lt; m$ and there is a rock at $((x+1) \bmod n, y+1)$, RT cannot move right or it will be hit by the rock.</p><center> <img class="tex-graphics" src="file://A69LaRTE.png" style="max-width: 100.0%;max-height: 100.0%;"> </center><p>However, it is worth noting that if there is a rock at $(x \bmod n, y+1)$ and $((x+1) \bmod n, y)$, RT can still move right safely.</p><center> <img class="tex-graphics" src="file://kNQc68I5.png" style="max-width: 100.0%;max-height: 100.0%;"> </center><p>Find the minimum amount of time RT needs to reach $(n-1,m-1)$ without colliding with any rocks. If it is impossible to do so, output $-1$.</p></div><div class="input-specification"><p>The first line of the input contains one integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>In each test case, the first line contains two integers $n$, $m$ ($3 \le n, m \le 10^3$)&nbsp;— the size of the planet's boundaries. </p><p>Each of the next $n$ lines contains $m$ integers. The $(j+1)$-th integer on the $(i+1)$-th line ($0 \le i &lt; n, 0 \le j &lt; m$) is $a_{i,j}$ ($0 \le a_{i,j} \le 1$), which denotes whether or not there is a rock at $(i,j)$ at time $0$.</p><p><span class="tex-font-style-bf">Additionally, it is guaranteed that $a_{0,0} = 0$, and $a_{i, m-1} = 0$ for $0 \le i &lt; n$.</span> In other words, there is no rock at RT's initial position as well as column $m-1$.</p><p>The sum of $n \cdot m$ over all test cases does not exceed $10^6$.</p></div><div class="output-specification"><p>For each test case: </p><ul> <li> If the destination can be reached without colliding with any rocks, output a single integer&nbsp;— the minimum amount of time RT needs to reach $(n-1,m-1)$. </li><li> Otherwise, output $-1$. </li></ul></div>

## Input

<p>The first line of the input contains one integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>In each test case, the first line contains two integers $n$, $m$ ($3 \le n, m \le 10^3$)&nbsp;— the size of the planet's boundaries. </p><p>Each of the next $n$ lines contains $m$ integers. The $(j+1)$-th integer on the $(i+1)$-th line ($0 \le i &lt; n, 0 \le j &lt; m$) is $a_{i,j}$ ($0 \le a_{i,j} \le 1$), which denotes whether or not there is a rock at $(i,j)$ at time $0$.</p><p><span class="tex-font-style-bf">Additionally, it is guaranteed that $a_{0,0} = 0$, and $a_{i, m-1} = 0$ for $0 \le i &lt; n$.</span> In other words, there is no rock at RT's initial position as well as column $m-1$.</p><p>The sum of $n \cdot m$ over all test cases does not exceed $10^6$.</p>

## Output

<p>For each test case: </p><ul> <li> If the destination can be reached without colliding with any rocks, output a single integer&nbsp;— the minimum amount of time RT needs to reach $(n-1,m-1)$. </li><li> Otherwise, output $-1$. </li></ul>





```input1|2,3,4,5,6,11,12,13,14,15,16,21,22,23,24
6
4 5
0 1 0 0 0
0 0 1 0 0
1 0 1 1 0
0 0 0 0 0
3 3
0 0 0
1 0 0
0 0 0
5 3
0 0 0
0 0 0
1 0 0
0 0 0
1 0 0
3 7
0 0 1 0 0 1 0
1 0 1 0 1 0 0
0 1 0 0 0 0 0
3 4
0 1 0 0
1 0 0 0
0 1 1 0
5 5
0 0 0 0 0
0 1 0 1 0
0 1 0 1 0
0 1 0 1 0
0 0 0 1 0
```




```input2|2,3,4,5,11,12,13,14,15,20,21,22,23
6
3 3
0 0 0
0 0 0
0 0 0
4 3
0 1 0
1 0 0
0 1 0
1 0 0
4 3
0 1 0
0 1 0
0 1 0
0 1 0
3 3
0 0 0
1 1 0
0 0 0
3 3
0 1 0
0 0 0
0 1 0
5 5
0 0 0 0 0
0 1 1 0 0
0 1 1 0 0
0 0 0 0 0
0 0 1 0 0
```




```output1
7
3
3
8
-1
12
```




```output2
3
3
-1
-1
3
8
```



## Note

<p>Visual explanation of the first test case in the example: </p><center> <img class="tex-graphics" src="file://R9QDUTD3.png" style="max-width: 100.0%;max-height: 100.0%;"> </center>
