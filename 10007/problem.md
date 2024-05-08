## Description

<div><p>Vladislav has a binary square grid of $n \times n$ cells. A triangle or a square is drawn on the grid with symbols $\texttt{1}$. As he is too busy being cool, he asks you to tell him which shape is drawn on the grid.</p><ul><li> A <span class="tex-font-style-it">triangle</span> is a shape consisting of $k$ ($k&gt;1$) consecutive rows, where the $i$-th row has $2 \cdot i-1$ consecutive characters $\texttt{1}$, and the central <span class="tex-font-style-tt">1</span>s are located in one column. An upside down triangle is also considered a valid triangle (but not rotated by 90 degrees).</li></ul><center> <img class="tex-graphics" src="file://Op4p8AvO.png" style="max-width: 100.0%;max-height: 100.0%;">   <span class="tex-font-size-small">Two left pictures contain examples of triangles: $k=4$, $k=3$. The two right pictures don't contain triangles.</span> </center><ul><li> A <span class="tex-font-style-it">square</span> is a shape consisting of $k$ ($k&gt;1$) consecutive rows, where the $i$-th row has $k$ consecutive characters $\texttt{1}$, which are positioned at an equal distance from the left edge of the grid.</li></ul><center> <img class="tex-graphics" src="file://ZwW3oJmn.png" style="max-width: 100.0%;max-height: 100.0%;">   <span class="tex-font-size-small">Examples of two squares: $k=2$, $k=4$.</span> </center><p>For the given grid, determine the type of shape that is drawn on it.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \leq t \leq 100$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains a single integer $n$ ($2 \leq n \leq 10$)&nbsp;— the size of the grid.</p><p>The next $n$ lines each contain $n$ characters $\texttt{0}$ or $\texttt{1}$.</p><p>The grid contains exactly one triangle or exactly one square that contains all the $\texttt{1}$s in the grid. It is guaranteed that the size of the triangle or square is greater than $1$ (i.e., the shape cannot consist of exactly one <span class="tex-font-style-tt">1</span>).</p></div><div class="output-specification"><p>For each test case, output "<span class="tex-font-style-tt">SQUARE</span>" if all the $\texttt{1}$s in the grid form a square, and "<span class="tex-font-style-tt">TRIANGLE</span>" otherwise (without quotes).</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \leq t \leq 100$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains a single integer $n$ ($2 \leq n \leq 10$)&nbsp;— the size of the grid.</p><p>The next $n$ lines each contain $n$ characters $\texttt{0}$ or $\texttt{1}$.</p><p>The grid contains exactly one triangle or exactly one square that contains all the $\texttt{1}$s in the grid. It is guaranteed that the size of the triangle or square is greater than $1$ (i.e., the shape cannot consist of exactly one <span class="tex-font-style-tt">1</span>).</p>

## Output

<p>For each test case, output "<span class="tex-font-style-tt">SQUARE</span>" if all the $\texttt{1}$s in the grid form a square, and "<span class="tex-font-style-tt">TRIANGLE</span>" otherwise (without quotes).</p>





```input1|2,3,4,5,11,12,13,20,21,22,23,24,25,26,27,28,29,30
6
3
000
011
011
4
0000
0000
0100
1110
2
11
11
5
00111
00010
00000
00000
00000
10
0000000000
0000000000
0000000000
0000000000
0000000000
1111111110
0111111100
0011111000
0001110000
0000100000
3
111
111
111
```




```output1
SQUARE
TRIANGLE
SQUARE
TRIANGLE
TRIANGLE
SQUARE
```


