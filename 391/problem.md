## Description

<div><p>There is a matrix of size $n \times n$ which consists of <span class="tex-font-style-tt">0</span>s and <span class="tex-font-style-tt">1</span>s. The rows are numbered from $1$ to $n$ from top to bottom, the columns are numbered from $1$ to $n$ from left to right. The cell at the intersection of the $x$-th row and the $y$-th column is denoted as $(x, y)$.</p><p>AquaMoon wants to turn all elements of the matrix to <span class="tex-font-style-tt">0</span>s. In one step she can perform the following operation:</p><ul> <li> Select an arbitrary cell, let it be $(i, j)$, then invert the element in $(i, j)$ and also invert all elements in cells $(x, y)$ for $x &gt; i$ and $x - i \ge \left|y - j\right|$. To invert a value means to change it to the opposite: <span class="tex-font-style-tt">0</span> changes to <span class="tex-font-style-tt">1</span>, <span class="tex-font-style-tt">1</span> changes to <span class="tex-font-style-tt">0</span>. </li></ul><p>Help AquaMoon determine the minimum number of steps she need to perform to turn all elements of the matrix to <span class="tex-font-style-tt">0</span>s. We can show that an answer always exists.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^5$). The description of the test cases follows.</p><p>The first line of each test case contains an integer $n$ ($2 \le n \le 3000$).</p><p>The $i$-th of the following $n$ lines contains a binary string only of characters <span class="tex-font-style-tt">0</span> and <span class="tex-font-style-tt">1</span>, of length $n$.</p><p>It is guaranteed that the sum of $n^2$ over all test cases does not exceed $9\,000\,000$.</p></div><div class="output-specification"><p>For each test case, print the minimum number of steps.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^5$). The description of the test cases follows.</p><p>The first line of each test case contains an integer $n$ ($2 \le n \le 3000$).</p><p>The $i$-th of the following $n$ lines contains a binary string only of characters <span class="tex-font-style-tt">0</span> and <span class="tex-font-style-tt">1</span>, of length $n$.</p><p>It is guaranteed that the sum of $n^2$ over all test cases does not exceed $9\,000\,000$.</p>

## Output

<p>For each test case, print the minimum number of steps.</p>





```input1|2,3,4,5,6,7,12,13,14,15,16,17,18
3
5
00100
01110
11111
11111
11111
3
100
110
110
6
010101
111101
011110
000000
111010
001110
```




```output1
1
2
15
```



## Note

<p>In the first test case, we can use the following scheme:</p><ol> <li> perform the operation on the cell $(1, 3)$. </li></ol><p>Clearly, the elements of the initial matrix are not all <span class="tex-font-style-tt">0</span>, so at least one operation is required. Thus, $1$ is the answer.</p><p>In the second test case, we use the following scheme:</p><ol> <li> perform the operation on the cell $(3, 3)$; </li><li> perform the operation on the cell $(1, 1)$. </li></ol><p>It can be shown that there is no way to convert all elements to <span class="tex-font-style-tt">0</span>s in $0$ or $1$ steps, so the answer is exactly $2$.</p>
