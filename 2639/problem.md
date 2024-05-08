## Description

<div><p>Gildong has a square board consisting of $n$ rows and $n$ columns of square cells, each consisting of a single digit (from $0$ to $9$). The cell at the $j$-th column of the $i$-th row can be represented as $(i, j)$, and the length of the side of each cell is $1$. Gildong likes big things, so for each digit $d$, he wants to find a triangle such that:</p><ul> <li> Each vertex of the triangle is in the center of a cell. </li><li> The digit of every vertex of the triangle is $d$. </li><li> At least one side of the triangle is parallel to one of the sides of the board. You may assume that a side of length $0$ is parallel to both sides of the board. </li><li> The area of the triangle is maximized. </li></ul><p>Of course, he can't just be happy with finding these triangles as is. Therefore, for each digit $d$, he's going to change the digit of exactly one cell of the board to $d$, then find such a triangle. He changes it back to its original digit after he is done with each digit. Find the maximum area of the triangle he can make for each digit.</p><p>Note that he can put multiple vertices of the triangle on the same cell, and the triangle can be a <a href="https://cutt.ly/NhbjZ2l">degenerate triangle</a>; i.e. the area of the triangle can be $0$. Also, note that he is allowed to change the digit of a cell from $d$ to $d$.</p></div><div class="input-specification"><p>Each test contains one or more test cases. The first line contains the number of test cases $t$ ($1 \le t \le 1000$).</p><p>The first line of each test case contains one integer $n$ ($1 \le n \le 2000$) — the number of rows and columns of the board.</p><p>The next $n$ lines of each test case each contain a string of $n$ digits without spaces. The $j$-th digit of the $i$-th line is the digit of the cell at $(i, j)$. Each digit is one of the characters from $0$ to $9$.</p><p>It is guaranteed that the sum of $n^2$ in all test cases doesn't exceed $4 \cdot 10^6$.</p></div><div class="output-specification"><p>For each test case, print one line with $10$ integers. The $i$-th integer is the maximum area of triangle Gildong can make when $d = i-1$, multiplied by $2$.</p></div>

## Input

<p>Each test contains one or more test cases. The first line contains the number of test cases $t$ ($1 \le t \le 1000$).</p><p>The first line of each test case contains one integer $n$ ($1 \le n \le 2000$) — the number of rows and columns of the board.</p><p>The next $n$ lines of each test case each contain a string of $n$ digits without spaces. The $j$-th digit of the $i$-th line is the digit of the cell at $(i, j)$. Each digit is one of the characters from $0$ to $9$.</p><p>It is guaranteed that the sum of $n^2$ in all test cases doesn't exceed $4 \cdot 10^6$.</p>

## Output

<p>For each test case, print one line with $10$ integers. The $i$-th integer is the maximum area of triangle Gildong can make when $d = i-1$, multiplied by $2$.</p>





```input1
5
3
000
122
001
2
57
75
4
0123
4012
3401
2340
1
9
8
42987101
98289412
38949562
87599023
92834718
83917348
19823743
38947912
```




```output1
4 4 1 0 0 0 0 0 0 0
0 0 0 0 0 1 0 1 0 0
9 6 9 9 6 0 0 0 0 0
0 0 0 0 0 0 0 0 0 0
18 49 49 49 49 15 0 30 42 42
```



## Note

<p>In the first case, for $d=0$, no matter which cell he chooses to use, the triangle with vertices at $(1, 1)$, $(1, 3)$, and $(3, 1)$ is the biggest triangle with area of $\cfrac{2 \cdot 2}{2} = 2$. Since we should print it multiplied by $2$, the answer for $d=0$ is $4$.</p><p>For $d=1$, Gildong can change the digit of the cell at $(1, 3)$ into $1$, making a triangle with vertices on all three $1$'s that has an area of $2$.</p><p>For $d=2$, Gildong can change the digit of one of the following six cells into $2$ to make a triangle with an area of $\cfrac{1}{2}$: $(1, 1)$, $(1, 2)$, $(1, 3)$, $(3, 1)$, $(3, 2)$, and $(3, 3)$.</p><p>For the remaining digits (from $3$ to $9$), the cell Gildong chooses to change will be the only cell that contains that digit. Therefore the triangle will always be a degenerate triangle with an area of $0$.</p><p>In the third case, for $d=4$, note that the triangle will be bigger than the answer if Gildong changes the digit of the cell at $(1, 4)$ and use it along with the cells at $(2, 1)$ and $(4, 3)$, but this is invalid because it violates the condition that at least one side of the triangle must be parallel to one of the sides of the board.</p>
