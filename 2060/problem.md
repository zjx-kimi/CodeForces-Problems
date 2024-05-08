## Description

<div><p>Alice has a grid with $2$ rows and $n$ columns. She fully covers the grid using $n$ dominoes of size $1 \times 2$&nbsp;— Alice may place them vertically or horizontally, and each cell should be covered by exactly one domino.</p><p>Now, she decided to show one row of the grid to Bob. Help Bob and figure out what the other row of the grid looks like!</p></div><div class="input-specification"><p>The input consists of multiple test cases. The first line contains an integer $t$ ($1 \leq t \leq 5000$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains an integer $n$ ($1 \leq n \leq 100$)&nbsp;— the width of the grid.</p><p>The second line of each test case contains a string $s$ consisting of $n$ characters, each of which is either <span class="tex-font-style-tt">L</span>, <span class="tex-font-style-tt">R</span>, <span class="tex-font-style-tt">U</span>, or <span class="tex-font-style-tt">D</span>, representing the left, right, top, or bottom half of a domino, respectively (see notes for better understanding). This string represents one of the rows of the grid. </p><p><span class="tex-font-style-bf">Additional constraint on the input:</span> each input corresponds to at least one valid tiling.</p></div><div class="output-specification"><p>For each test case, output one string&nbsp;— the other row of the grid, using the same format as the input string. If there are multiple answers, print any.</p></div>

## Input

<p>The input consists of multiple test cases. The first line contains an integer $t$ ($1 \leq t \leq 5000$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains an integer $n$ ($1 \leq n \leq 100$)&nbsp;— the width of the grid.</p><p>The second line of each test case contains a string $s$ consisting of $n$ characters, each of which is either <span class="tex-font-style-tt">L</span>, <span class="tex-font-style-tt">R</span>, <span class="tex-font-style-tt">U</span>, or <span class="tex-font-style-tt">D</span>, representing the left, right, top, or bottom half of a domino, respectively (see notes for better understanding). This string represents one of the rows of the grid. </p><p><span class="tex-font-style-bf">Additional constraint on the input:</span> each input corresponds to at least one valid tiling.</p>

## Output

<p>For each test case, output one string&nbsp;— the other row of the grid, using the same format as the input string. If there are multiple answers, print any.</p>





```input1
4
1
U
2
LR
5
LRDLR
6
UUUUUU
```




```output1
D
LR
LRULR
DDDDDD
```



## Note

<p>In the first test case, Alice shows Bob the <span class="tex-font-style-it">top</span> row, the whole grid may look like: </p><center> <img class="tex-graphics" src="file://u813tAWZ.png" style="max-width: 100.0%;max-height: 100.0%;"> </center><p>In the second test case, Alice shows Bob the <span class="tex-font-style-it">bottom</span> row, the whole grid may look like: </p><center> <img class="tex-graphics" src="file://LE08ozmC.png" style="max-width: 100.0%;max-height: 100.0%;"> </center><p>In the third test case, Alice shows Bob the <span class="tex-font-style-it">bottom</span> row, the whole grid may look like: </p><center> <img class="tex-graphics" src="file://QsQLstBs.png" style="max-width: 100.0%;max-height: 100.0%;"> </center><p>In the fourth test case, Alice shows Bob the <span class="tex-font-style-it">top</span> row, the whole grid may look like: </p><center> <img class="tex-graphics" src="file://PvQNEzSa.png" style="max-width: 100.0%;max-height: 100.0%;"> </center>
