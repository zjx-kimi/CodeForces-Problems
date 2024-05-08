## Description

<div><p>There is an $n\times m$ board divided into cells. There are also some dominoes on this board. Each domino covers two adjacent cells (that is, two cells that share a side), and no two dominoes overlap.</p><p>Piet thinks that this board is too boring and it needs to be painted. He will paint the cells of the dominoes black and white. He calls the painting <span class="tex-font-style-it">beautiful</span> if all of the following conditions hold:</p><ul> <li> for each domino, one of its cells is painted white and the other is painted black; </li><li> for each row, the number of black cells in this row equals the number of white cells in this row; </li><li> for each column, the number of black cells in this column equals the number of white cells in this column. </li></ul><p>Note that the cells that are not covered by dominoes are not painted at all, they are counted as neither black nor white.</p><p>Help Piet produce a beautiful painting or tell that it is impossible.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10\,000$). The description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $m$ ($2\le n, m\le 500$).</p><p>The next $n$ lines describe the tiling of the board, row by row from top to bottom. Each of these lines contains $m$ characters, describing the cells in the corresponding row from left to right. Each character is one of <span class="tex-font-style-tt">U</span>, <span class="tex-font-style-tt">D</span>, <span class="tex-font-style-tt">L</span>, <span class="tex-font-style-tt">R</span>, or <span class="tex-font-style-tt">.</span>, meaning that the cell is covered with a top, bottom, left, right half of a domino or nothing, respectively. The tiling is guaranteed to be valid.</p><p>It is guaranteed that the sum of $n \cdot m$ over all test cases does not exceed $250\,000$.</p></div><div class="output-specification"><p>For each test case, output a single integer $-1$ if a beautiful painting does not exist. Otherwise, print $n$ lines, each containing $m$ characters, describing the colors in the corresponding row of a beautiful painting. Every character corresponding to a cell not covered by a domino must be <span class="tex-font-style-tt">.</span> (a dot), and all other characters must be <span class="tex-font-style-tt">B</span> if the corresponding cell is black or <span class="tex-font-style-tt">W</span> if it is white.</p><p>If there are multiple solutions, print any of them.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10\,000$). The description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $m$ ($2\le n, m\le 500$).</p><p>The next $n$ lines describe the tiling of the board, row by row from top to bottom. Each of these lines contains $m$ characters, describing the cells in the corresponding row from left to right. Each character is one of <span class="tex-font-style-tt">U</span>, <span class="tex-font-style-tt">D</span>, <span class="tex-font-style-tt">L</span>, <span class="tex-font-style-tt">R</span>, or <span class="tex-font-style-tt">.</span>, meaning that the cell is covered with a top, bottom, left, right half of a domino or nothing, respectively. The tiling is guaranteed to be valid.</p><p>It is guaranteed that the sum of $n \cdot m$ over all test cases does not exceed $250\,000$.</p>

## Output

<p>For each test case, output a single integer $-1$ if a beautiful painting does not exist. Otherwise, print $n$ lines, each containing $m$ characters, describing the colors in the corresponding row of a beautiful painting. Every character corresponding to a cell not covered by a domino must be <span class="tex-font-style-tt">.</span> (a dot), and all other characters must be <span class="tex-font-style-tt">B</span> if the corresponding cell is black or <span class="tex-font-style-tt">W</span> if it is white.</p><p>If there are multiple solutions, print any of them.</p>





```input1|2,3,4,5,6,13,14,15
3
4 6
..LR..
ULRU..
DLRDUU
..LRDD
5 4
.LR.
.UU.
UDDU
D..D
LR..
2 2
..
..
```




```output1
..WB..
WWBB..
BBWWWB
..BWBW
-1
..
..
```



## Note

<p>In the first test case, the answer is illustrated below: </p><center> <img class="tex-graphics" src="file://ChJhlAC1.png" style="max-width: 100.0%;max-height: 100.0%;"> </center><p>In the second test case, it is impossible to paint all cells the right way.</p>
