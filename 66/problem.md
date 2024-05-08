## Description

<div><p>You are given an <span class="tex-font-style-bf">even</span> integer $n$ and an integer $k$. Your task is to construct a matrix of size $n \times n$ consisting of numbers $0$ and $1$ in such a way that the following conditions are true, or report that it is impossible:</p><ul> <li> the sum of all the numbers in the matrix is exactly $k$; </li><li> the bitwise $\texttt{XOR}$ of all the numbers in the row $i$ is the same for each $i$; </li><li> the bitwise $\texttt{XOR}$ of all the numbers in the column $j$ is the same for each $j$. </li></ul></div><div class="input-specification"><p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 130$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>Each test case is described by a single line, which contains two integers $n$ and $k$ ($2 \leq n \leq 1000$, $n$ is even, $0 \leq k \leq n^2$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2000$.</p></div><div class="output-specification"><p>For each test case, output $\texttt{Yes}$ if it's possible to construct a matrix that satisfies all of the problem's conditions, and $\texttt{No}$ otherwise.</p><p>If it is possible to construct a matrix, the $i$-th of the next $n$ lines should contain $n$ integers representing the elements in the $i$-th row of the matrix.</p></div>

## Input

<p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 130$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>Each test case is described by a single line, which contains two integers $n$ and $k$ ($2 \leq n \leq 1000$, $n$ is even, $0 \leq k \leq n^2$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2000$.</p>

## Output

<p>For each test case, output $\texttt{Yes}$ if it's possible to construct a matrix that satisfies all of the problem's conditions, and $\texttt{No}$ otherwise.</p><p>If it is possible to construct a matrix, the $i$-th of the next $n$ lines should contain $n$ integers representing the elements in the $i$-th row of the matrix.</p>





```input1
5
4 0
6 6
6 5
4 2
6 36
```




```output1
Yes
0 0 0 0
0 0 0 0
0 0 0 0
0 0 0 0
Yes
1 0 0 0 0 0
0 1 0 0 0 0
0 0 1 0 0 0
0 0 0 1 0 0
0 0 0 0 1 0
0 0 0 0 0 1
No
No
Yes
1 1 1 1 1 1
1 1 1 1 1 1
1 1 1 1 1 1
1 1 1 1 1 1
1 1 1 1 1 1
1 1 1 1 1 1
```



## Note

<p>In the first example, all conditions are satisfied: </p><ul> <li> the sum of all the numbers in the matrix is exactly $0$; </li><li> the bitwise $\texttt{XOR}$ of all the numbers in the row $i$ is $0$ for each $i$; </li><li> the bitwise $\texttt{XOR}$ of all the numbers in the column $j$ is $0$ for each $j$. </li></ul><p>In the third example, it can be shown that it's impossible to find a matrix satisfying all the problem's conditions.</p>
