## Description

<div><p><span class="tex-font-style-bf">This is the hard version of the problem. The difference between the versions is the constraints on $a_i$. You can make hacks only if all versions of the problem are solved.</span></p><p>Little Dormi has recently received a puzzle from his friend and needs your help to solve it. </p><p>The puzzle consists of an upright board with $n$ rows and $m$ columns of cells, some empty and some filled with blocks of sand, and $m$ non-negative integers $a_1,a_2,\ldots,a_m$ ($0 \leq a_i \leq n$). In this version of the problem, $a_i$ will always be <span class="tex-font-style-bf">not greater than</span> the number of blocks of sand in column $i$.</p><p>When a cell filled with a block of sand is disturbed, the block of sand will fall from its cell to the sand counter at the bottom of the column (each column has a sand counter). While a block of sand is falling, other blocks of sand that are adjacent at any point to the falling block of sand will also be disturbed and start to fall. Specifically, a block of sand disturbed at a cell $(i,j)$ will pass through all cells below and including the cell $(i,j)$ within the column, disturbing all adjacent cells along the way. Here, the cells adjacent to a cell $(i,j)$ are defined as $(i-1,j)$, $(i,j-1)$, $(i+1,j)$, and $(i,j+1)$ (if they are within the grid). Note that the newly falling blocks can disturb other blocks.</p><p>In one operation you are able to disturb any piece of sand. The puzzle is solved when there are <span class="tex-font-style-bf">at least</span> $a_i$ blocks of sand counted in the $i$-th sand counter for each column from $1$ to $m$.</p><p>You are now tasked with finding the minimum amount of operations in order to solve the puzzle. Note that Little Dormi will never give you a puzzle that is impossible to solve.</p></div><div class="input-specification"><p>The first line consists of two space-separated positive integers $n$ and $m$ ($1 \leq n \cdot m \leq 400\,000$).</p><p>Each of the next $n$ lines contains $m$ characters, describing each row of the board. If a character on a line is '<span class="tex-font-style-tt">.</span>', the corresponding cell is empty. If it is '<span class="tex-font-style-tt">#</span>', the cell contains a block of sand.</p><p>The final line contains $m$ non-negative integers $a_1,a_2,\ldots,a_m$ ($0 \leq a_i \leq n$) — the minimum amount of blocks of sand that needs to fall below the board in each column. In this version of the problem, $a_i$ will always be <span class="tex-font-style-bf">not greater than</span> the number of blocks of sand in column $i$.</p></div><div class="output-specification"><p>Print one non-negative integer, the minimum amount of operations needed to solve the puzzle.</p></div>

## Input

<p>The first line consists of two space-separated positive integers $n$ and $m$ ($1 \leq n \cdot m \leq 400\,000$).</p><p>Each of the next $n$ lines contains $m$ characters, describing each row of the board. If a character on a line is '<span class="tex-font-style-tt">.</span>', the corresponding cell is empty. If it is '<span class="tex-font-style-tt">#</span>', the cell contains a block of sand.</p><p>The final line contains $m$ non-negative integers $a_1,a_2,\ldots,a_m$ ($0 \leq a_i \leq n$) — the minimum amount of blocks of sand that needs to fall below the board in each column. In this version of the problem, $a_i$ will always be <span class="tex-font-style-bf">not greater than</span> the number of blocks of sand in column $i$.</p>

## Output

<p>Print one non-negative integer, the minimum amount of operations needed to solve the puzzle.</p>





```input1
5 7
#....#.
.#.#...
#....#.
#....##
#.#....
4 1 1 1 0 3 1
```




```input2
3 3
#.#
#..
##.
3 1 1
```




```input3
7 5
.#..#
#....
..##.
..##.
..###
..#..
#.##.
0 0 2 4 2
```




```output1
3
```




```output2
1
```




```output3
1
```



## Note

<p>For example $1$, by disturbing both blocks of sand on the first row from the top at the first and sixth columns from the left, and the block of sand on the second row from the top and the fourth column from the left, it is possible to have all the required amounts of sand fall in each column. It can be proved that this is not possible with fewer than $3$ operations, and as such the answer is $3$. Here is the puzzle from the first example.</p><center> <img class="tex-graphics" src="file://StmEJsrl.png" style="max-width: 100.0%;max-height: 100.0%;"> </center> <p>For example $2$, by disturbing the cell on the top row and rightmost column, one can cause all of the blocks of sand in the board to fall into the counters at the bottom. Thus, the answer is $1$. Here is the puzzle from the second example.</p><center> <img class="tex-graphics" src="file://EIT0WLcR.png" style="max-width: 100.0%;max-height: 100.0%;"> </center> <p>For example $3$, by disturbing the cell on the top row and rightmost column, it is possible to have all the required amounts of sand fall in each column. It can be proved that this is not possible with fewer than $1$ operation, and as such the answer is $1$. Here is the puzzle from the third example.</p><center> <img class="tex-graphics" src="file://eJruQqLI.png" style="max-width: 100.0%;max-height: 100.0%;"> </center>
