## Description

<div><p>During your journey through computer universes, you stumbled upon a very interesting world. It is a path with $n$ consecutive cells, each of which can either be empty, contain thorns, or a coin. In one move, you can move one or two cells along the path, provided that the destination cell does not contain thorns (and belongs to the path). If you move to the cell with a coin, you pick it up.</p><center> <img class="tex-graphics" src="file://rw9Ym4mc.png" style="max-width: 100.0%;max-height: 100.0%;">   <span class="tex-font-size-small">Here, green arrows correspond to legal moves, and the red arrow corresponds to an illegal move.</span> </center><p>You want to collect as many coins as possible. Find the maximum number of coins you can collect in the discovered world if you start in the leftmost cell of the path.</p></div><div class="input-specification"><p>The first line of input contains a single integer $t$ ($1 \le t \le 1000$)&nbsp;— the number of test cases. Then the descriptions of the test cases follow.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 50$)&nbsp;— the length of the path.</p><p>The second line of each test case contains a string of $n$ characters, the description of the path. The character <span class="tex-font-style-tt">'.'</span> denotes an empty cell, <span class="tex-font-style-tt">'@'</span> denotes a cell with a coin, and <span class="tex-font-style-tt">'*'</span> denotes a cell with thorns. It is guaranteed that the first cell is empty.</p></div><div class="output-specification"><p>For each test case, output a single integer, the maximum number of coins you can collect.</p></div>

## Input

<p>The first line of input contains a single integer $t$ ($1 \le t \le 1000$)&nbsp;— the number of test cases. Then the descriptions of the test cases follow.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 50$)&nbsp;— the length of the path.</p><p>The second line of each test case contains a string of $n$ characters, the description of the path. The character <span class="tex-font-style-tt">'.'</span> denotes an empty cell, <span class="tex-font-style-tt">'@'</span> denotes a cell with a coin, and <span class="tex-font-style-tt">'*'</span> denotes a cell with thorns. It is guaranteed that the first cell is empty.</p>

## Output

<p>For each test case, output a single integer, the maximum number of coins you can collect.</p>





```input1|2,3,6,7
3
10
.@@*@.**@@
5
.@@@@
15
.@@..@***..@@@*
```




```output1
3
4
3
```



## Note

<p>The picture for the first example is in the problem statement.</p><p>Here is the picture for the second example:</p><center> <img class="tex-graphics" src="file://pZQSjZW9.png" style="max-width: 100.0%;max-height: 100.0%;"> </center><p>And here is the picture for the third example:</p><center> <img class="tex-graphics" src="file://RWX73RAI.png" style="max-width: 100.0%;max-height: 100.0%;"> </center>
