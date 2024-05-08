## Description

<div><p>A horizontal grid strip of $n$ cells is given. In the $i$-th cell, there is a paint charge of size $a_i$. This charge can be:</p><ul> <li> either used to the left — then all cells to the left at a distance less than $a_i$ (from $\max(i - a_i + 1, 1)$ to $i$ inclusive) will be painted, </li><li> or used to the right — then all cells to the right at a distance less than $a_i$ (from $i$ to $\min(i + a_i - 1, n)$ inclusive) will be painted, </li><li> or not used at all. </li></ul><p>Note that a charge can be used no more than once (that is, it <span class="tex-font-style-bf">cannot</span> be used simultaneously to the left and to the right). It is allowed for a cell to be painted more than once.</p><p>What is the minimum number of times a charge needs to be used to paint all the cells of the strip?</p></div><div class="input-specification"><p>The first line of the input contains an integer $t$ ($1 \le t \le 100$) — the number of test cases in the test. This is followed by descriptions of $t$ test cases.</p><p>Each test case is specified by two lines. The first one contains an integer $n$ ($1 \le n \le 100$) — the number of cells in the strip. The second line contains $n$ positive integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le n$), where $a_i$ is the size of the paint charge in the $i$-th cell from the left of the strip.</p><p>It is guaranteed that the sum of the values of $n$ in the test does not exceed $1000$.</p></div><div class="output-specification"><p>For each test case, output the minimum number of times the charges need to be used to paint all the cells of the strip.</p></div>

## Input

<p>The first line of the input contains an integer $t$ ($1 \le t \le 100$) — the number of test cases in the test. This is followed by descriptions of $t$ test cases.</p><p>Each test case is specified by two lines. The first one contains an integer $n$ ($1 \le n \le 100$) — the number of cells in the strip. The second line contains $n$ positive integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le n$), where $a_i$ is the size of the paint charge in the $i$-th cell from the left of the strip.</p><p>It is guaranteed that the sum of the values of $n$ in the test does not exceed $1000$.</p>

## Output

<p>For each test case, output the minimum number of times the charges need to be used to paint all the cells of the strip.</p>





```input1|2,3,6,7,10,11,14,15,18,19,22,23,26,27
13
1
1
2
1 1
2
2 1
2
1 2
2
2 2
3
1 1 1
3
3 1 2
3
1 3 1
7
1 2 3 1 2 4 2
7
2 1 1 1 2 3 1
10
2 2 5 1 6 1 8 2 8 2
6
2 1 2 1 1 2
6
1 1 4 1 3 2
```




```output1
1
2
1
1
1
3
1
2
3
4
2
3
3
```



## Note

<p>In the third test case of the example, it is sufficient to use the charge from the $1$-st cell to the right, then it will cover both cells $1$ and $2$.</p><p>In the ninth test case of the example, you need to: </p><ul> <li> use the charge from the $3$-rd cell to the left, covering cells from the $1$-st to the $3$-rd; </li><li> use the charge from the $5$-th cell to the left, covering cells from the $4$-th to the $5$-th; </li><li> use the charge from the $7$-th cell to the left, covering cells from the $6$-th to the $7$-th. </li></ul><p>In the eleventh test case of the example, you need to: </p><ul> <li> use the charge from the $5$-th cell to the right, covering cells from the $5$-th to the $10$-th; </li><li> use the charge from the $7$-th cell to the left, covering cells from the $1$-st to the $7$-th. </li></ul>
