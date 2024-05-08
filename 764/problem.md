## Description

<div><p>There is a rectangular maze of size $n\times m$. Denote $(r,c)$ as the cell on the $r$-th row from the top and the $c$-th column from the left. Two cells are <span class="tex-font-style-it">adjacent</span> if they share an edge. A <span class="tex-font-style-it">path</span> is a sequence of <span class="tex-font-style-it">adjacent</span> empty cells.</p><p>Each cell is initially empty. Li Hua can choose some cells (except $(x_1, y_1)$ and $(x_2, y_2)$) and place an obstacle in each of them. He wants to know the minimum number of obstacles needed to be placed so that there isn't a <span class="tex-font-style-it">path</span> from $(x_1, y_1)$ to $(x_2, y_2)$.</p><p>Suppose you were Li Hua, please solve this problem.</p></div><div class="input-specification"><p>The first line contains the single integer $t$ ($1 \le t \le 500$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains two integers $n,m$ ($4\le n,m\le 10^9$)&nbsp;— the size of the maze.</p><p>The second line of each test case contains four integers $x_1,y_1,x_2,y_2$ ($1\le x_1,x_2\le n, 1\le y_1,y_2\le m$)&nbsp;— the coordinates of the start and the end.</p><p>It is guaranteed that $|x_1-x_2|+|y_1-y_2|\ge 2$.</p></div><div class="output-specification"><p>For each test case print the minimum number of obstacles you need to put on the field so that there is no <span class="tex-font-style-it">path</span> from $(x_1, y_1)$ to $(x_2, y_2)$.</p></div>

## Input

<p>The first line contains the single integer $t$ ($1 \le t \le 500$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains two integers $n,m$ ($4\le n,m\le 10^9$)&nbsp;— the size of the maze.</p><p>The second line of each test case contains four integers $x_1,y_1,x_2,y_2$ ($1\le x_1,x_2\le n, 1\le y_1,y_2\le m$)&nbsp;— the coordinates of the start and the end.</p><p>It is guaranteed that $|x_1-x_2|+|y_1-y_2|\ge 2$.</p>

## Output

<p>For each test case print the minimum number of obstacles you need to put on the field so that there is no <span class="tex-font-style-it">path</span> from $(x_1, y_1)$ to $(x_2, y_2)$.</p>





```input1|2,3,6,7
3
4 4
2 2 3 3
6 7
1 1 2 3
9 9
5 1 3 6
```




```output1
4
2
3
```



## Note

<p>In test case 1, you can put obstacles on $(1,3), (2,3), (3,2), (4,2)$. Then the path from $(2,2)$ to $(3,3)$ will not exist.</p><center> <table class="tex-tabular"><tbody><tr><td class="tex-tabular-text-align-center"><img class="tex-graphics" src="file://YUcvRhBB.png" style="max-width: 100.0%;max-height: 100.0%;"></td></tr></tbody></table> </center>
