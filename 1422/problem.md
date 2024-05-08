## Description

<div><p>You are given a grid with $n$ rows and $m$ columns, where each cell has a positive integer written on it. Let's call a grid <span class="tex-font-style-it">good</span>, if in each row the sequence of numbers is sorted in a non-decreasing order. It means, that for each $1 \le i \le n$ and $2 \le j \le m$ the following holds: $a_{i,j} \ge a_{i, j-1}$.</p><p>You have to to do the following operation exactly once: choose two columns with indexes $i$ and $j$ (<span class="tex-font-style-bf">not necessarily different</span>), $1 \le i, j \le m$, and swap them.</p><p>You are asked to determine whether it is possible to make the grid good after the swap and, if it is, find the columns that need to be swapped.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 100$). Description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $m$ ($1 \le n, m \le 2 \cdot 10^5$)&nbsp;— the number of rows and columns respectively.</p><p>Each of the next $n$ rows contains $m$ integers, $j$-th element of $i$-th row is $a_{i,j}$ ($1 \le a_{i,j} \le 10^9$)&nbsp;— the number written in the $j$-th cell of the $i$-th row.</p><p>It's guaranteed that the sum of $n \cdot m$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>If after the swap it is impossible to get a good grid, output $-1$.</p><p>In the other case output $2$ integers&nbsp;— the indices of the columns that should be swapped to get a good grid.</p><p>If there are multiple solutions, print any.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 100$). Description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $m$ ($1 \le n, m \le 2 \cdot 10^5$)&nbsp;— the number of rows and columns respectively.</p><p>Each of the next $n$ rows contains $m$ integers, $j$-th element of $i$-th row is $a_{i,j}$ ($1 \le a_{i,j} \le 10^9$)&nbsp;— the number written in the $j$-th cell of the $i$-th row.</p><p>It's guaranteed that the sum of $n \cdot m$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>If after the swap it is impossible to get a good grid, output $-1$.</p><p>In the other case output $2$ integers&nbsp;— the indices of the columns that should be swapped to get a good grid.</p><p>If there are multiple solutions, print any.</p>





```input1|2,3,4,8,9,10,14,15,16
5
2 3
1 2 3
1 1 1
2 2
4 1
2 3
2 2
2 1
1 1
2 3
6 2 1
5 4 3
2 1
1
2
```




```output1
1 1
-1
1 2
1 3
1 1
```



## Note

<p>In the first test case the grid is initially good, so we can, for example, swap the first column with itself.</p><p>In the second test case it is impossible to make the grid good.</p><p>In the third test case it is needed to swap the first and the second column, then the grid becomes good.</p>
