## Description

<div><p>Vladislav has a grid of size $7 \times 7$, where each cell is colored black or white. In one operation, he can choose any cell and change its color (black $\leftrightarrow$ white).</p><p>Find the minimum number of operations required to ensure that there are no black cells with four diagonal neighbors also being black.</p><center> <img class="tex-graphics" src="file://iULz3cnL.png" style="max-width: 100.0%;max-height: 100.0%;"><p><span class="tex-font-size-small">The left image shows that initially there are two black cells violating the condition. By flipping one cell, the grid will work.</span> </p></center></div><div class="input-specification"><p>The first line of input contains a single integer $t$ ($1 \leq t \leq 200$)&nbsp;— the number of test cases. Then follows the description of the test cases.</p><p>Each test case consists of $7$ lines, each containing $7$ characters. Each of these characters is either $\texttt{W}$ or $\texttt{B}$, denoting a white or black cell, respectively.</p></div><div class="output-specification"><p>For each test case, output a single integer&nbsp;— the minimum number of operations required to ensure that there are no black cells with all four diagonal neighbors also being black.</p></div>

## Input

<p>The first line of input contains a single integer $t$ ($1 \leq t \leq 200$)&nbsp;— the number of test cases. Then follows the description of the test cases.</p><p>Each test case consists of $7$ lines, each containing $7$ characters. Each of these characters is either $\texttt{W}$ or $\texttt{B}$, denoting a white or black cell, respectively.</p>

## Output

<p>For each test case, output a single integer&nbsp;— the minimum number of operations required to ensure that there are no black cells with all four diagonal neighbors also being black.</p>





```input1|2,3,4,5,6,7,8,16,17,18,19,20,21,22
4
WWWWWWW
WWWWBBB
WWWWWBW
WWBBBBB
WWWBWWW
WWBBBWW
WWWWWWW
WWWWWWW
WWWWWWW
WBBBBBW
WBBBBBW
WBBBBBW
WWWWWWW
WWWWWWW
WWWWWWW
WWWWWWW
WWWWWWW
WWWWWWW
WWWWWWW
WWWWWWW
WWWWWWW
WBBBBBW
BBBBBBB
BBBBBBB
WWWWWWW
BBBBBBB
BBBBBBB
BBBBBBB
```




```output1
1
2
0
5
```



## Note

<p>The first test case is illustrated in the statement.</p><p>The second test case is illustrated below: </p><center> <img class="tex-graphics" src="file://4wdnHBn3.png" style="max-width: 100.0%;max-height: 100.0%;"> </center><p>In the third test case, the grid already satisfies the condition.</p>
