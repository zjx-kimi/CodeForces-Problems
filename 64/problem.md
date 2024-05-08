## Description

<div><p>A brick is a strip of size $1 \times k$, placed horizontally or vertically, where $k$ can be an arbitrary number that is at least $2$ ($k \ge 2$).</p><p>A brick wall of size $n \times m$ is such a way to place several bricks inside a rectangle $n \times m$, that all bricks lie either horizontally or vertically in the cells, do not cross the border of the rectangle, and that each cell of the $n \times m$ rectangle belongs to exactly one brick. Here $n$ is the height of the rectangle $n \times m$ and $m$ is the width. <span class="tex-font-style-bf">Note</span> that there can be bricks with different values of k in the same brick wall.</p><p>The wall stability is the difference between the number of horizontal bricks and the number of vertical bricks. <span class="tex-font-style-bf">Note</span> that if you used $0$ horizontal bricks and $2$ vertical ones, then the stability will be <span class="tex-font-style-bf">$-2$, not $2$</span>.</p><p>What is the maximal possible stability of a wall of size $n \times m$?</p><p>It is guaranteed that under restrictions in the statement at least one $n \times m$ wall exists.</p></div><div class="input-specification"><p>The first line of the input contains one integer $t$ ($1 \le t \le 10\,000$), the number of test cases. </p><p>The only line of each test case contains two integers $n$ and $m$ ($2 \le n,\,m \le 10^4$).</p></div><div class="output-specification"><p>For each test case, print one integer, the maximum stability of a wall of size $n \times m$.</p></div>

## Input

<p>The first line of the input contains one integer $t$ ($1 \le t \le 10\,000$), the number of test cases. </p><p>The only line of each test case contains two integers $n$ and $m$ ($2 \le n,\,m \le 10^4$).</p>

## Output

<p>For each test case, print one integer, the maximum stability of a wall of size $n \times m$.</p>





```input1|2,4,6
5
2 2
7 8
16 9
3 5
10000 10000
```




```output1
2
28
64
6
50000000
```



## Note

<p>In the 1st test case, the maximum stability of $2$ is obtained by placing two horizontal bricks $1 \times 2$ one on top of the other.</p><p>In the 2nd test case, one can get the maximum stability of $28$ by placing $4$ horizontal bricks $1 \times 2$ in each of the $7$ rows.</p>
