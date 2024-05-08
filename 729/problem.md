## Description

<div><p>You are given a checkerboard of size $201 \times 201$, i.&nbsp;e. it has $201$ rows and $201$ columns. The rows of this checkerboard are numbered from $-100$ to $100$ from bottom to top. The columns of this checkerboard are numbered from $-100$ to $100$ from left to right. The notation $(r, c)$ denotes the cell located in the $r$-th row and the $c$-th column.</p><p>There is a king piece at position $(0, 0)$ and it wants to get to position $(a, b)$ as soon as possible. In this problem our king is lame. Each second, the king makes exactly one of the following five moves. </p><ul> <li> Skip move. King's position remains unchanged. </li><li> Go up. If the current position of the king is $(r, c)$ he goes to position $(r + 1, c)$. </li><li> Go down. Position changes from $(r, c)$ to $(r - 1, c)$. </li><li> Go right. Position changes from $(r, c)$ to $(r, c + 1)$. </li><li> Go left. Position changes from $(r, c)$ to $(r, c - 1)$. </li></ul> King is <span class="tex-font-style-bf">not allowed</span> to make moves that put him outside of the board. The important consequence of the king being lame is that he is <span class="tex-font-style-bf">not allowed</span> to make the same move during two consecutive seconds. For example, if the king goes right, the next second he can only skip, go up, down, or left.<p>What is the minimum number of seconds the lame king needs to reach position $(a, b)$?</p></div><div class="input-specification"><p>The first line of the input contains a single integer $t$ ($1 \leq t \leq 10^4$)&nbsp;— the number of test cases. Then follow $t$ lines containing one test case description each.</p><p>Each test case consists of two integers $a$ and $b$ ($-100 \leq a, b \leq 100$)&nbsp;— the position of the cell that the king wants to reach. It is guaranteed that either $a \ne 0$ or $b \ne 0$.</p></div><div class="output-specification"><p>Print $t$ integers. The $i$-th of these integers should be equal to the minimum number of seconds the lame king needs to get to the position he wants to reach in the $i$-th test case. The king always starts at position $(0, 0)$.</p></div>

## Input

<p>The first line of the input contains a single integer $t$ ($1 \leq t \leq 10^4$)&nbsp;— the number of test cases. Then follow $t$ lines containing one test case description each.</p><p>Each test case consists of two integers $a$ and $b$ ($-100 \leq a, b \leq 100$)&nbsp;— the position of the cell that the king wants to reach. It is guaranteed that either $a \ne 0$ or $b \ne 0$.</p>

## Output

<p>Print $t$ integers. The $i$-th of these integers should be equal to the minimum number of seconds the lame king needs to get to the position he wants to reach in the $i$-th test case. The king always starts at position $(0, 0)$.</p>





```input1|2,4,6
5
-4 1
4 4
0 -6
-5 -4
7 -8
```




```output1
7
8
11
9
15
```



## Note

<p>One of the possible solutions for the first example is: go down, go right, go down, go right, go down, go left, go down.</p><p>One of the possible solutions for the second example is to alternate "go right" and "go up" moves $4$ times each.</p><p>One of the possible solutions for the third example is to alternate "go left" and "skip" moves starting with "go left". Thus, "go left" will be used $6$ times, and "skip" will be used $5$ times.</p>
