## Description

<div><p>You have a horizontal strip of $n$ cells. Each cell is either white or black.</p><p>You can choose a <span class="tex-font-style-bf">continuous</span> segment of cells once and paint them all white. After this action, all the black cells in this segment will become white, and the white ones will remain white.</p><p>What is the minimum length of the segment that needs to be painted white in order for all $n$ cells to become white?</p></div><div class="input-specification"><p>The first line of the input contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. The descriptions of the test cases follow.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 10$)&nbsp;— the length of the strip.</p><p>The second line of each test case contains a string $s$, consisting of $n$ characters, each of which is either <span class="tex-font-style-tt">'W'</span> or <span class="tex-font-style-tt">'B'</span>. The symbol <span class="tex-font-style-tt">'W'</span> denotes a white cell, and <span class="tex-font-style-tt">'B'</span>&nbsp;— a black one. It is guaranteed that at least one cell of the given strip is black.</p></div><div class="output-specification"><p>For each test case, output a single number&nbsp;— the minimum length of a <span class="tex-font-style-bf">continuous</span> segment of cells that needs to be painted white in order for the <span class="tex-font-style-bf">entire</span> strip to become white.</p></div>

## Input

<p>The first line of the input contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. The descriptions of the test cases follow.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 10$)&nbsp;— the length of the strip.</p><p>The second line of each test case contains a string $s$, consisting of $n$ characters, each of which is either <span class="tex-font-style-tt">'W'</span> or <span class="tex-font-style-tt">'B'</span>. The symbol <span class="tex-font-style-tt">'W'</span> denotes a white cell, and <span class="tex-font-style-tt">'B'</span>&nbsp;— a black one. It is guaranteed that at least one cell of the given strip is black.</p>

## Output

<p>For each test case, output a single number&nbsp;— the minimum length of a <span class="tex-font-style-bf">continuous</span> segment of cells that needs to be painted white in order for the <span class="tex-font-style-bf">entire</span> strip to become white.</p>





```input1|2,3,6,7,10,11,14,15
8
6
WBBWBW
1
B
2
WB
3
BBW
4
BWWB
6
BWBWWB
6
WWBBWB
9
WBWBWWWBW
```




```output1
4
1
1
2
4
6
4
7
```



## Note

<p>In the first test case of the example for the strip "<span class="tex-font-style-tt">WBBWBW</span>", the minimum length of the segment to be repainted white is $4$. It is necessary to repaint to white the segment from the $2$-nd to the $5$-th cell (the cells are numbered from $1$ from left to right).</p>
