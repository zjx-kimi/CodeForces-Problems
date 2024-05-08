## Description

<div><p>Recently biologists came to a fascinating conclusion about how to find a chameleon mood. Consider chameleon body to be a rectangular table $n \times m$, each cell of which may be green or blue and may change between these two colors. We will denote as $(x, y)$ ($1 \leq x \leq n$, $1 \leq y \leq m$) the cell in row $x$ and column $y$.</p><p>Let us define a chameleon <span class="tex-font-style-it">good mood certificate</span> to be four cells which are corners of some subrectangle of the table, such that colors in opposite cells among these four are similar, and at the same time not all of the four cell colors are similar. Formally, it is a group of four cells $(x_1, y_1)$, $(x_1, y_2)$, $(x_2, y_1)$, $(x_2, y_2)$ for some $1 \leq x_1 &lt; x_2 \leq n$, $1 \leq y_1 &lt; y_2 \leq m$, that colors of $(x_1, y_1)$ and $(x_2, y_2)$ coincide and colors of $(x_1, y_2)$ and $(x_2, y_1)$ coincide, but not all of the four cells share the same color. It was found that whenever such four cells are present, chameleon is in good mood, and vice versa: if there are no such four cells, chameleon is in bad mood.</p><p>You are asked to help scientists write a program determining the mood of chameleon. Let us consider that initially all cells of chameleon are green. After that chameleon coloring may change several times. On one change, colors of contiguous segment of some table row are replaced with the opposite. Formally, each color change is defined by three integers $a$, $l$, $r$ ($1 \leq a \leq n$, $1 \leq l \leq r \leq m$). On such change colors of all cells $(a, b)$ such that $l \leq b \leq r$ are replaced with the opposite.</p><p>Write a program that reports mood of the chameleon after each change. Additionally, if the chameleon mood is good, program should find out any four numbers $x_1$, $y_1$, $x_2$, $y_2$ such that four cells $(x_1, y_1)$, $(x_1, y_2)$, $(x_2, y_1)$, $(x_2, y_2)$ are the good mood certificate.</p></div><div class="input-specification"><p>The first line of input contains three integers $n$, $m$, $q$ ($1 \leq n, m \leq 2000$, $1 \leq q \leq 500\,000$), the sizes of the table and the number of changes respectively. </p><p>Each of the following $q$ lines contains 3 integers $a_i$, $l_i$, $r_i$ ($1 \leq a_i \leq n$, $1 \leq l_i \leq r_i \leq m$), describing $i$-th coloring change.</p></div><div class="output-specification"><p>Print $q$ lines. In the $i$-th line report the chameleon mood after first $i$ color changes for all $1 \leq i \leq q$.</p><p>If chameleon is in bad mood, print the only integer $-1$.</p><p>Otherwise, print four integers $x_1$, $y_1$, $x_2$, $y_2$ ($1 \leq x_1 &lt; x_2 \leq n$, $1 \leq y_1 &lt; y_2 \leq m$) such that four cells $(x_1, y_1)$, $(x_1, y_2)$, $(x_2, y_1)$, $(x_2, y_2)$ are the good mood certificate. If there are several ways to choose such four integers, print any valid one.</p></div>

## Input

<p>The first line of input contains three integers $n$, $m$, $q$ ($1 \leq n, m \leq 2000$, $1 \leq q \leq 500\,000$), the sizes of the table and the number of changes respectively. </p><p>Each of the following $q$ lines contains 3 integers $a_i$, $l_i$, $r_i$ ($1 \leq a_i \leq n$, $1 \leq l_i \leq r_i \leq m$), describing $i$-th coloring change.</p>

## Output

<p>Print $q$ lines. In the $i$-th line report the chameleon mood after first $i$ color changes for all $1 \leq i \leq q$.</p><p>If chameleon is in bad mood, print the only integer $-1$.</p><p>Otherwise, print four integers $x_1$, $y_1$, $x_2$, $y_2$ ($1 \leq x_1 &lt; x_2 \leq n$, $1 \leq y_1 &lt; y_2 \leq m$) such that four cells $(x_1, y_1)$, $(x_1, y_2)$, $(x_2, y_1)$, $(x_2, y_2)$ are the good mood certificate. If there are several ways to choose such four integers, print any valid one.</p>





```input1
2 2 6
1 1 1
2 2 2
2 1 1
1 2 2
2 2 2
1 1 1
```




```input2
4 3 9
2 2 3
4 1 2
2 1 3
3 2 2
3 1 3
1 2 2
4 2 3
1 1 3
3 1 3
```




```output1
-1
1 1 2 2
-1
-1
-1
1 1 2 2
```




```output2
-1
2 1 4 3
-1
2 1 3 2
3 2 4 3
1 1 2 2
1 1 2 2
-1
2 1 3 2
```


