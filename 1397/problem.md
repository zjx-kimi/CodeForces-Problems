## Description

<div><p><span class="tex-font-style-it">Lena is a beautiful girl who likes logical puzzles.</span></p><p>As a gift for her birthday, Lena got a matrix puzzle!</p><p>The matrix consists of $n$ rows and $m$ columns, and each cell is either black or white. The coordinates $(i,j)$ denote the cell which belongs to the $i$-th row and $j$-th column for every $1\leq i \leq n$ and $1\leq j \leq m$. To solve the puzzle, Lena has to choose a cell that minimizes the Manhattan distance to the farthest black cell from the chosen cell.</p><p>More formally, let there be $k \ge 1$ black cells in the matrix with coordinates $(x_i,y_i)$ for every $1\leq i \leq k$. Lena should choose a cell $(a,b)$ that minimizes $$\max_{i=1}^{k}(|a-x_i|+|b-y_i|).$$</p><p>As Lena has no skill, she asked you for help. Will you tell her the optimal cell to choose? </p></div><div class="input-specification"><p>There are several test cases in the input data. The first line contains a single integer $t$ ($1\leq t\leq 10\,000$)&nbsp;— the number of test cases. This is followed by the test cases description.</p><p>The first line of each test case contains two integers $n$ and $m$ ($2\leq n,m \leq 1000$) &nbsp;— the dimensions of the matrix. </p><p>The following $n$ lines contain $m$ characters each, each character is either '<span class="tex-font-style-tt">W</span>' or '<span class="tex-font-style-tt">B</span>'. The $j$-th character in the $i$-th of these lines is '<span class="tex-font-style-tt">W</span>' if the cell $(i,j)$ is white, and '<span class="tex-font-style-tt">B</span>' if the cell $(i,j)$ is black. </p><p>It is guaranteed that at least one black cell exists.</p><p>It is guaranteed that the sum of $n\cdot m$ does not exceed $10^6$.</p></div><div class="output-specification"><p>For each test case, output the optimal cell $(a,b)$ to choose. If multiple answers exist, output any.</p></div>

## Input

<p>There are several test cases in the input data. The first line contains a single integer $t$ ($1\leq t\leq 10\,000$)&nbsp;— the number of test cases. This is followed by the test cases description.</p><p>The first line of each test case contains two integers $n$ and $m$ ($2\leq n,m \leq 1000$) &nbsp;— the dimensions of the matrix. </p><p>The following $n$ lines contain $m$ characters each, each character is either '<span class="tex-font-style-tt">W</span>' or '<span class="tex-font-style-tt">B</span>'. The $j$-th character in the $i$-th of these lines is '<span class="tex-font-style-tt">W</span>' if the cell $(i,j)$ is white, and '<span class="tex-font-style-tt">B</span>' if the cell $(i,j)$ is black. </p><p>It is guaranteed that at least one black cell exists.</p><p>It is guaranteed that the sum of $n\cdot m$ does not exceed $10^6$.</p>

## Output

<p>For each test case, output the optimal cell $(a,b)$ to choose. If multiple answers exist, output any.</p>





```input1
5
3 2
BW
WW
WB
3 3
WWB
WBW
BWW
2 3
BBB
BBB
5 5
BWBWB
WBWBW
BWBWB
WBWBW
BWBWB
9 9
WWWWWWWWW
WWWWWWWWW
BWWWWWWWW
WWWWWWWWW
WWWWBWWWW
WWWWWWWWW
WWWWWWWWW
WWWWWWWWW
WWWWWWWWB
```




```output1
2 1
2 2
1 2
3 3
6 5
```



## Note

<p>In the first test case the two black cells have coordinates $(1,1)$ and $(3,2)$. The four optimal cells are $(1,2)$, $(2,1)$, $(2,2)$ and $(3,1)$. It can be shown that no other cell minimizes the maximum Manhattan distance to every black cell.</p><p>In the second test case it is optimal to choose the black cell $(2,2)$ with maximum Manhattan distance being $2$.</p>
