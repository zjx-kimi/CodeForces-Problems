## Description

<div><p>There is a one-dimensional grid of length $n$. The $i$-th cell of the grid contains a character $s_i$, which is either '<span class="tex-font-style-tt">&lt;</span>' or '<span class="tex-font-style-tt">&gt;</span>'.</p><p>When a pinball is placed on one of the cells, it moves according to the following rules: </p><ul> <li> If the pinball is on the $i$-th cell and $s_i$ is '<span class="tex-font-style-tt">&lt;</span>', the pinball moves one cell to the left in the next second. If $s_i$ is '<span class="tex-font-style-tt">&gt;</span>', it moves one cell to the right. </li><li> After the pinball has moved, the character $s_i$ is inverted (i.&nbsp;e. if $s_i$ used to be '<span class="tex-font-style-tt">&lt;</span>', it becomes '<span class="tex-font-style-tt">&gt;</span>', and vice versa). </li><li> The pinball stops moving when it leaves the grid: either from the left border or from the right one. </li></ul><p>You need to answer $n$ <span class="tex-font-style-bf">independent</span> queries. In the $i$-th query, a pinball will be placed on the $i$-th cell. Note that we always place a pinball on the initial grid.</p><p>For each query, calculate how many seconds it takes the pinball to leave the grid. It can be shown that the pinball will always leave the grid within a finite number of steps.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^5$). The description of the test cases follows.</p><p>The first line of each test case contains an integer $n$ ($1 \le n \le 5 \cdot 10^5$).</p><p>The second line of each test case contains a string $s_1s_2 \ldots s_{n}$ of length $n$ consisting of characters '<span class="tex-font-style-tt">&lt;</span>' and '<span class="tex-font-style-tt">&gt;</span>'.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $5 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, for each $i$ ($1 \le i \le n$) output the answer if a pinball is initially placed on the $i$-th cell.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^5$). The description of the test cases follows.</p><p>The first line of each test case contains an integer $n$ ($1 \le n \le 5 \cdot 10^5$).</p><p>The second line of each test case contains a string $s_1s_2 \ldots s_{n}$ of length $n$ consisting of characters '<span class="tex-font-style-tt">&lt;</span>' and '<span class="tex-font-style-tt">&gt;</span>'.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $5 \cdot 10^5$.</p>

## Output

<p>For each test case, for each $i$ ($1 \le i \le n$) output the answer if a pinball is initially placed on the $i$-th cell.</p>





```input1|2,3,6,7
3
3
&gt;&lt;&lt;
4
&lt;&lt;&lt;&lt;
6
&lt;&gt;&lt;&lt;&lt;&gt;
```




```output1
3 6 5 
1 2 3 4 
1 4 7 10 8 1
```



## Note

<p>In the first test case, the movement of the pinball for $i=1$ is shown in the following pictures. It takes the pinball $3$ seconds to leave the grid.</p><center> <img class="tex-graphics" src="file://b3rXupoY.png" style="max-width: 100.0%;max-height: 100.0%;"> </center><p>The movement of the pinball for $i=2$ is shown in the following pictures. It takes the pinball $6$ seconds to leave the grid.</p><center> <img class="tex-graphics" src="file://N1VfqEpj.png" style="max-width: 100.0%;max-height: 100.0%;"> </center>
