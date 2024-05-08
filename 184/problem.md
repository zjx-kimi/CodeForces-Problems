## Description

<div><p>There is a ribbon divided into $n$ cells, numbered from $1$ to $n$ from left to right. Initially, an integer $0$ is written in each cell.</p><p>Monocarp plays a game with a chip. The game consists of several turns. During the first turn, Monocarp places the chip in the $1$-st cell of the ribbon. During each turn <span class="tex-font-style-bf">except for the first turn</span>, Monocarp does <span class="tex-font-style-bf">exactly one</span> of the two following actions:</p><ul> <li> move the chip to the next cell (i. e. if the chip is in the cell $i$, it is moved to the cell $i+1$). This action is impossible if the chip is in the last cell; </li><li> choose any cell $x$ and teleport the chip into that cell. <span class="tex-font-style-bf">It is possible to choose the cell where the chip is currently located</span>. </li></ul><p>At the end of each turn, the integer written in the cell with the chip is increased by $1$.</p><p>Monocarp's goal is to make some turns so that the $1$-st cell contains the integer $c_1$, the $2$-nd cell contains the integer $c_2$, ..., the $n$-th cell contains the integer $c_n$. He wants to teleport the chip as few times as possible.</p><p>Help Monocarp calculate the minimum number of times he has to teleport the chip. </p></div><div class="input-specification"><p>The first line contains one integer $t$ ($1 \le t \le 10^4$) — the number of test cases.</p><p>Each test case consists of two lines: </p><ul> <li> the first line contains one integer $n$ ($1 \le n \le 2 \cdot 10^5$); </li><li> the second line contains $n$ integers $c_1, c_2, \dots, c_n$ ($0 \le c_i \le 10^9$; $c_1 \ge 1$). </li></ul><p>It can be shown that under these constraints, it is always possible to make a finite amount of turns so that the integers in the cells match the sequence $c_1, c_2, \dots, c_n$.</p><p>Additional constraint on the input: the sum of values of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, print one integer — the minimum number of times Monocarp has to teleport the chip.</p></div>

## Input

<p>The first line contains one integer $t$ ($1 \le t \le 10^4$) — the number of test cases.</p><p>Each test case consists of two lines: </p><ul> <li> the first line contains one integer $n$ ($1 \le n \le 2 \cdot 10^5$); </li><li> the second line contains $n$ integers $c_1, c_2, \dots, c_n$ ($0 \le c_i \le 10^9$; $c_1 \ge 1$). </li></ul><p>It can be shown that under these constraints, it is always possible to make a finite amount of turns so that the integers in the cells match the sequence $c_1, c_2, \dots, c_n$.</p><p>Additional constraint on the input: the sum of values of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, print one integer — the minimum number of times Monocarp has to teleport the chip.</p>





```input1|2,3,6,7
4
4
1 2 2 1
5
1 0 1 0 1
5
5 4 3 2 1
1
12
```




```output1
1
2
4
11
```



## Note

<p>In the first test case of the example, Monocarp can perform the turns as follows:</p><ul> <li> place the chip in the $1$-st cell; the numbers in the cells are $[1, 0, 0, 0]$; </li><li> move the chip to the next ($2$-nd) cell; the numbers in the cells are $[1, 1, 0, 0]$; </li><li> move the chip to the next ($3$-rd) cell; the numbers in the cells are $[1, 1, 1, 0]$; </li><li> teleport the chip to the $2$-nd cell; the numbers in the cells are $[1, 2, 1, 0]$; </li><li> move the chip to the next ($3$-rd) cell; the numbers in the cells are $[1, 2, 2, 0]$; </li><li> move the chip to the next ($4$-th) cell; the numbers in the cells are $[1, 2, 2, 1]$. </li></ul>
