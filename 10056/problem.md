## Description

<div><p><span class="tex-font-style-bf">This is an interactive problem.</span></p><p>You are given a grid with $n$ rows and $m$ columns. The coordinates $(x, y)$ represent the cell on the grid, where $x$ ($1 \leq x \leq n$) is the row number counting from the top and $y$ ($1 \leq y \leq m$) is the column number counting from the left. It is guaranteed that there are exactly $2$ mines in the grid at <span class="tex-font-style-bf">distinct</span> cells, denoted as $(x_1, y_1)$ and $(x_2, y_2)$. You are allowed to make no more than $4$ queries to the interactor, and after these queries, you need to provide the location of <span class="tex-font-style-bf">one of the mines</span>.</p><p>In each query, you can choose any grid cell $(x, y)$, and in return, you will receive the minimum Manhattan distance from both the mines to the chosen cell, i.e., you will receive the value $\min(|x-x_1|+|y-y_1|, |x-x_2|+|y-y_2|)$.</p><p>Your task is to determine the location of one of the mines after making the queries.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line of input contains a single integer $t$ ($1 \leq t \leq 3 \cdot 10^{3}$)&nbsp;— the number of test cases.</p><p>The only line of each test case contains two integers $n$ and $m$ ($2 \leq n \leq 10^{8}$, $2 \leq m \leq 10^{8}$)&nbsp;— the number of rows and columns.</p></div><div><h2>Interaction</h2><p>For each test case, the interaction starts with reading $n$ and $m$.</p><p>Then you are allowed to make at most $4$ queries in the following way:</p><p>"<span class="tex-font-style-tt">? x y</span>" ($1 \leq x \leq n$ and $1 \leq y \leq m$)</p><p>After each one, you should read an integer $d$ which is equal to $\min(|x-x_1|+|y-y_1|, |x-x_2|+|y-y_2|)$.</p><p>When you have found the location of any one of the mines, print a single line "<span class="tex-font-style-tt">! x y</span>" (without quotes), representing the row and the column of one of the mines. Outputting the answer does not count as a query.</p><p>After printing the answer, your program must then continue to solve the remaining test cases, or exit if all test cases have been solved.</p><p><span class="tex-font-style-bf">The interactor for this problem is not adaptive</span>: cells of mines are fixed before any queries are made.</p><p>After printing a query, do not forget to output the end of line and flush the output. Otherwise, you will get <span class="tex-font-style-tt">Idleness limit exceeded</span>. To do this, use: </p><ul> <li> <span class="tex-font-style-tt">fflush(stdout)</span> or <span class="tex-font-style-tt">cout.flush()</span> in C++; </li><li> <span class="tex-font-style-tt">System.out.flush()</span> in Java; </li><li> <span class="tex-font-style-tt">flush(output)</span> in Pascal; </li><li> <span class="tex-font-style-tt">stdout.flush()</span> in Python; </li><li> see the documentation for other languages. </li></ul><p><span class="tex-font-style-bf">Hacks:</span></p><p>To make a hack, use the following format:</p><p>The first line contains a single integer $t$ ($1 \leq t \leq 3 \cdot 10^{3}$)&nbsp;— the number of test cases.</p><p>The description of each test case should consist of three lines. </p><p>The first line contains two integers $n$ and $m$ ($2 \leq n \leq 10^{8}$, $2 \leq m \leq 10^{8}$)&nbsp;— the number of rows and columns. </p><p>The second line contains the coordinates of the first mine $x_1$ and $y_1$($1 \leq x_1 \leq n$, $1 \leq y_1 \leq m$).</p><p>The third line contains the coordinates of the second mine $x_2$ and $y_2$($1 \leq x_2 \leq n$, $1 \leq y_2 \leq m$).</p><p>The mines should be located at different positions.</p></div>

## Input

<p>Each test contains multiple test cases. The first line of input contains a single integer $t$ ($1 \leq t \leq 3 \cdot 10^{3}$)&nbsp;— the number of test cases.</p><p>The only line of each test case contains two integers $n$ and $m$ ($2 \leq n \leq 10^{8}$, $2 \leq m \leq 10^{8}$)&nbsp;— the number of rows and columns.</p>





```input1
2
4 4

3

2

2

0

5 5

1

2

3
```




```output1
? 1 1

? 1 4

? 4 1

? 2 3

! 2 3

? 5 5

? 2 2

? 3 3

! 1 1
```



## Note

<p>In the first test case, we start by querying the upper-left corner $(1, 1)$ and get the result $3$, which means that there is a mine on the counter diagonal, and there is no mine above it. </p><p>In the image below, each cell contains a number indicating the distance to the blue cell. The green cells are candidates to contain the nearest mine.</p><center> <img class="tex-graphics" src="file://G92r3QVm.png" style="max-width: 100.0%;max-height: 100.0%;" width="227px"> </center><p>Then we ask three cells on that diagonal, and at the last query, we get the result $0$, which means that a mine is found at the position $(2, 3)$.</p><p>The second mine was located at the position $(3, 2)$.</p><p>In the second test case, we start by asking the lower-right corner $(5, 5)$, and get the result $1$, which means that one of the two neighbours contains a mine, let's call it mine $1$.</p><center> <img class="tex-graphics" src="file://EfJTgH4D.png" style="max-width: 100.0%;max-height: 100.0%;" width="227px"> </center><p>Then we ask cell $(2, 2)$. We can see that these green cells don't intersect with the green cells from the first query, so they contain the other mine, let's call it mine $2$.</p><center> <img class="tex-graphics" src="file://w73czvhr.png" style="max-width: 100.0%;max-height: 100.0%;" width="227px"> </center><p>Query $3$ is cell $(3, 3)$. These cells contain mine $1$, but we still don't know where exactly. Nevertheless, we can determine that the only possible cell for mine $2$ is $(1, 1)$, because all other candidates are at a distance closer than $3$ for this query.</p><center> <img class="tex-graphics" src="file://cZhritqO.png" style="max-width: 100.0%;max-height: 100.0%;" width="227px"> </center>
