## Description

<div><p>Argus was charged with guarding Io, which is not an ordinary cow. Io is quite an explorer, and she wanders off rather frequently, making Argus' life stressful. So the cowherd decided to construct an enclosed pasture for Io.</p><p>There are $n$ trees growing along the river, where Argus tends Io. For this problem, the river can be viewed as the $OX$ axis of the Cartesian coordinate system, and the $n$ trees as points with the $y$-coordinate equal $0$. There is also another tree growing in the point $(0, 1)$. </p><p>Argus will tie a rope around three of the trees, creating a triangular pasture. Its exact shape doesn't matter to Io, but its area is crucial to her. There may be many ways for Argus to arrange the fence, but only the ones which result in different areas of the pasture are interesting for Io. Calculate the number of <span class="tex-font-style-bf">different</span> areas that her pasture may have. Note that the pasture must have <span class="tex-font-style-bf">nonzero</span> area.</p></div><div class="input-specification"><p>The input consists of multiple test cases. The first line contains an integer $t$ ($1 \leq t \leq 100$)&nbsp;— the number of test cases. Then $t$ test cases follow, each one is described in two lines.</p><p>In the first line of each test case there is a single integer $n$ ($1 \leq n \leq 50$) denoting the number of trees growing along the river. Next line contains $n$ distinct integers $x_1 &lt; x_2 &lt; \ldots &lt; x_{n - 1} &lt; x_n$ ($1 \leq x_i \leq 50$), the $x$-coordinates of trees growing along the river.</p></div><div class="output-specification"><p>In a single line output an integer, the number of <span class="tex-font-style-bf">different</span> <span class="tex-font-style-bf">nonzero</span> areas that triangles with trees as vertices may have.</p></div>

## Input

<p>The input consists of multiple test cases. The first line contains an integer $t$ ($1 \leq t \leq 100$)&nbsp;— the number of test cases. Then $t$ test cases follow, each one is described in two lines.</p><p>In the first line of each test case there is a single integer $n$ ($1 \leq n \leq 50$) denoting the number of trees growing along the river. Next line contains $n$ distinct integers $x_1 &lt; x_2 &lt; \ldots &lt; x_{n - 1} &lt; x_n$ ($1 \leq x_i \leq 50$), the $x$-coordinates of trees growing along the river.</p>

## Output

<p>In a single line output an integer, the number of <span class="tex-font-style-bf">different</span> <span class="tex-font-style-bf">nonzero</span> areas that triangles with trees as vertices may have.</p>





```input1
8
4
1 2 4 5
3
1 3 5
3
2 6 8
2
1 2
1
50
5
3 4 5 6 8
3
1 25 26
6
1 2 4 8 16 32
```




```output1
4
2
3
1
0
5
3
15
```



## Note

<p>In the first test case, we have $6$ non-degenerate triangles with the following areas: $0.5$, $0.5$, $1$, $1.5$, $1.5$ and $2$. The pasture can have $4$ different areas, and thus $4$ is the answer.</p><p>In the second test case, we have $3$ non-degenerate triangles with the following areas: $1$, $1$ and $2$. The pasture can have $2$ different areas, so $2$ is the answer.</p><p>The following two drawings present the situation in the second test case. The blue triangles in the first drawing have area $1$. The red triangle in the second drawing has area $2$.</p><center> <img class="tex-graphics" src="file://7BwjNuX5.png" style="max-width: 100.0%;max-height: 100.0%;"> </center>
