## Description

<div><p>There is a ribbon divided into $n$ cells, numbered from $1$ to $n$ from left to right. Each cell either contains a chip or is free.</p><p>You can perform the following operation any number of times (possibly zero): choose a chip and move it to the <span class="tex-font-style-bf">closest free cell to the left</span>. You can choose any chip that you want, provided that there is at least one free cell to the left of it. When you move the chip, the cell where it was before the operation becomes free.</p><p>Your goal is to move the chips in such a way that <span class="tex-font-style-bf">they form a single block, without any free cells between them</span>. What is the minimum number of operations you have to perform?</p></div><div class="input-specification"><p>The first line contains one integer $t$ ($1 \le t \le 1000$) — the number of test cases.</p><p>Each test case consists of two lines:</p><ul> <li> the first line contains one integer $n$ ($2 \le n \le 50$) — the number of cells; </li><li> the second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($0 \le a_i \le 1$); $a_i = 0$ means that the $i$-th cell is free; $a_i = 1$ means that the $i$-th cell contains a chip. </li></ul><p>Additional constraint on the input: in each test case, at least one cell contains a chip.</p></div><div class="output-specification"><p>For each test case, print one integer — the minimum number of operations you have to perform so that all chips form a single block without any free cells between them.</p></div>

## Input

<p>The first line contains one integer $t$ ($1 \le t \le 1000$) — the number of test cases.</p><p>Each test case consists of two lines:</p><ul> <li> the first line contains one integer $n$ ($2 \le n \le 50$) — the number of cells; </li><li> the second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($0 \le a_i \le 1$); $a_i = 0$ means that the $i$-th cell is free; $a_i = 1$ means that the $i$-th cell contains a chip. </li></ul><p>Additional constraint on the input: in each test case, at least one cell contains a chip.</p>

## Output

<p>For each test case, print one integer — the minimum number of operations you have to perform so that all chips form a single block without any free cells between them.</p>





```input1|2,3,6,7,10,11
5
8
0 1 1 1 0 1 1 0
6
0 1 0 0 0 0
6
1 1 1 1 1 1
5
1 0 1 0 1
9
0 1 1 0 0 0 1 1 0
```




```output1
1
0
0
2
3
```



## Note

<p>In the first example, you can perform the operation on the chip in the $7$-th cell. The closest free cell to the left is the $5$-th cell, so it moves there. After that, all chips form a single block.</p><p>In the second example, all chips are already in a single block. Same for the third example.</p>
