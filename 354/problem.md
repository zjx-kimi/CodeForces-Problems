## Description

<div><p>You are given two integers $n$ and $k$. You are also given an array of integers $a_1, a_2, \ldots, a_n$ of size $n$. It is known that for all $1 \leq i \leq n$, $1 \leq a_i \leq k$.</p><p>Define a two-dimensional array $b$ of size $n \times n$ as follows: $b_{i, j} = \min(a_i, a_j)$. Represent array $b$ as a square, where the upper left cell is $b_{1, 1}$, rows are numbered from top to bottom from $1$ to $n$, and columns are numbered from left to right from $1$ to $n$. Let the color of a cell be the number written in it (for a cell with coordinates $(i, j)$, this is $b_{i, j}$).</p><p>For each color from $1$ to $k$, find the smallest rectangle in the array $b$ containing all cells of this color. Output the sum of width and height of this rectangle.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \leq t \leq 10^4$) — the number of test cases. Then follows the description of the test cases.</p><p>The first line of each test case contains two integers $n$ and $k$ ($1 \leq n, k \leq 10^5$) — the size of array $a$ and the number of colors.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \leq a_i \leq k$) — the array $a$.</p><p>It is guaranteed that the sum of the values of $n$ and $k$ over all test cases does not exceed $10^5$.</p></div><div class="output-specification"><p>For each test case, output $k$ numbers: the sums of width and height of the smallest rectangle containing all cells of a color, for each color from $1$ to $k$.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \leq t \leq 10^4$) — the number of test cases. Then follows the description of the test cases.</p><p>The first line of each test case contains two integers $n$ and $k$ ($1 \leq n, k \leq 10^5$) — the size of array $a$ and the number of colors.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \leq a_i \leq k$) — the array $a$.</p><p>It is guaranteed that the sum of the values of $n$ and $k$ over all test cases does not exceed $10^5$.</p>

## Output

<p>For each test case, output $k$ numbers: the sums of width and height of the smallest rectangle containing all cells of a color, for each color from $1$ to $k$.</p>





```input1|2,3,6,7,10,11
5
2 1
1 1
2 2
1 2
3 5
3 2 4
4 2
1 2 1 2
5 3
1 2 3 2 1
```




```output1
4 
4 2 
0 6 6 2 0 
8 6 
10 6 2
```



## Note

<p>In the first test case, the entire array $b$ consists of color $1$, so the smallest rectangle for color $1$ has a size of $2 \times 2$, and the sum of its sides is $4$.</p><p>In the second test case, the array $b$ looks like this:</p><p></p><table class="tex-tabular"><tbody><tr><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">1</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">1</td></tr><tr><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">1</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">2</td></tr></tbody></table><p></p><p>One of the corner cells has color $2$, and the other three cells have color $1$. Therefore, the smallest rectangle for color $1$ has a size of $2 \times 2$, and for color $2$ it is $1 \times 1$.</p><p>In the last test case, the array $b$ looks like this:</p><p></p><table class="tex-tabular"><tbody><tr><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">1</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">1</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">1</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">1</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">1</td></tr><tr><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">1</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">2</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">2</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">2</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">1</td></tr><tr><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">1</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">2</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">3</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">2</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">1</td></tr><tr><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">1</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">2</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">2</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">2</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">1</td></tr><tr><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">1</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">1</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">1</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">1</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">1</td></tr></tbody></table><p></p>
