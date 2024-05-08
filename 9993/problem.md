## Description

<div><p>Even in kindergarten, Sasha liked a girl. Therefore, he wanted to give her a drawing and attract her attention.</p><p>As a drawing, he decided to draw a square grid of size $n \times n$, in which some cells are colored. But coloring the cells is difficult, so he wants to color as few cells as possible. But at the same time, he wants <span class="tex-font-style-bf">at least</span> $k$ diagonals to have at least one colored cell. Note that the square grid of size $n \times n$ has a total of $4n - 2$ diagonals.</p><p>Help little Sasha to make the girl fall in love with him and tell him the minimum number of cells he needs to color.</p></div><div class="input-specification"><p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 1000$) — the number of test cases. The description of the test cases follows.</p><p>The only line of each test case contains two integers $n$ and $k$ ($2 \leq n \leq 10^8$, $1 \leq k \leq 4n - 2$) — the size of the square grid and the minimum number of diagonals in which there should be at least one colored cell.</p></div><div class="output-specification"><p>For each test case, output a single integer — the minimum number of cells that need to be colored.</p></div>

## Input

<p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 1000$) — the number of test cases. The description of the test cases follows.</p><p>The only line of each test case contains two integers $n$ and $k$ ($2 \leq n \leq 10^8$, $1 \leq k \leq 4n - 2$) — the size of the square grid and the minimum number of diagonals in which there should be at least one colored cell.</p>

## Output

<p>For each test case, output a single integer — the minimum number of cells that need to be colored.</p>





```input1|2,4,6,8
7
3 4
3 3
3 10
3 9
4 7
7 11
2 3
```




```output1
2
2
6
5
4
6
2
```



## Note

<p>In the pictures below, the colored cells are marked in black, and all diagonals are marked in purple.</p><p>In the first test case, you can color $2$ cells so that $4$ diagonals contain at least one colored cell:</p><center> <img class="tex-graphics" src="file://4xHxHeFV.png" style="max-width: 100.0%;max-height: 100.0%;"> </center><p>In the third test case, you can color $6$ cells so that all $10$ diagonals contain at least one colored cell:</p><center> <img class="tex-graphics" src="file://Q0clvRp4.png" style="max-width: 100.0%;max-height: 100.0%;"> </center>
