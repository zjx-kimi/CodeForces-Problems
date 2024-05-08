## Description

<div><p>Conveyor matrix $m_n$ is matrix of size $n \times n$, where $n$ is an <span class="tex-font-style-bf">even</span> number. The matrix consists of concentric ribbons moving clockwise.</p><p>In other words, the conveyor matrix for $n = 2$ is simply a matrix $2 \times 2$, whose cells form a cycle of length $4$ clockwise. For any natural $k \ge 2$, the matrix $m_{2k}$ is obtained by adding to the matrix $m_{2k - 2}$ an outer layer forming a clockwise cycle.</p><center> <img class="tex-graphics" src="file://sclNyAV2.png" style="max-width: 100.0%;max-height: 100.0%;">   <span class="tex-font-size-small">The conveyor matrix $8 \times 8$</span>.   </center><p>You are standing in a cell with coordinates $x_1, y_1$ and you want to get into a cell with coordinates $x_2, y_2$. A cell has coordinates $x, y$ if it is located at the intersection of the $x$th row and the $y$th column.</p><p>Standing on some cell, every second you will move to the cell next in the direction of movement of the tape on which you are. You can also move to a neighboring cell by spending one unit of energy. Movements happen instantly and you can make an unlimited number of them at any time.</p><p>Your task is to find the minimum amount of energy that will have to be spent to get from the cell with coordinates $x_1, y_1$ to the cell with coordinates $x_2, y_2$.</p><p>For example, $n=8$ initially you are in a cell with coordinates $1,3$ and you want to get into a cell with coordinates $6, 4$. You can immediately make $2$ movements, once you are in a cell with coordinates $3, 3$, and then after $8$ seconds you will be in the right cell.</p></div><div class="input-specification"><p>The first line contains an integer $t$ ($1 \le t \le 2 \cdot 10^5$) — the number of test cases.</p><p>The descriptions of the test cases follow.</p><p>The description of each test case consists of one string containing five integers $n$, $x_1$, $y_1$, $x_2$ and $y_2$ ($1 \le x_1, y_1, x_2, y_2 \le n \le 10^9$) — matrix size and the coordinates of the start and end cells. It is guaranteed that the number $n$ is even.</p></div><div class="output-specification"><p>For each test case, print one integer in a separate line — the minimum amount of energy that will have to be spent to get from the cell with coordinates $x_1, y_1$ to the cell with coordinates $x_2, y_2$.</p></div>

## Input

<p>The first line contains an integer $t$ ($1 \le t \le 2 \cdot 10^5$) — the number of test cases.</p><p>The descriptions of the test cases follow.</p><p>The description of each test case consists of one string containing five integers $n$, $x_1$, $y_1$, $x_2$ and $y_2$ ($1 \le x_1, y_1, x_2, y_2 \le n \le 10^9$) — matrix size and the coordinates of the start and end cells. It is guaranteed that the number $n$ is even.</p>

## Output

<p>For each test case, print one integer in a separate line — the minimum amount of energy that will have to be spent to get from the cell with coordinates $x_1, y_1$ to the cell with coordinates $x_2, y_2$.</p>





```input1|2,4,6
5
2 1 1 2 2
4 1 4 3 3
8 1 3 4 6
100 10 20 50 100
1000000000 123456789 987654321 998244353 500000004
```




```output1
0
1
2
9
10590032
```


