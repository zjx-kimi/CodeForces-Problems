## Description

<div><p>As you probably know, chess is a game that is played on a board with 64 squares arranged in an $8\times 8$ grid. Columns of this board are labeled with letters from <span class="tex-font-style-bf">a</span> to <span class="tex-font-style-bf">h</span>, and rows are labeled with digits from <span class="tex-font-style-bf">1</span> to <span class="tex-font-style-bf">8</span>. Each square is described by the row and column it belongs to.</p><center> <img class="tex-graphics" src="file://iKpCAj9r.png" style="max-width: 100.0%;max-height: 100.0%;"> </center><p>The rook is a piece in the game of chess. During its turn, it may move any non-zero number of squares horizontally or vertically. Your task is to find all possible moves for a rook on an empty chessboard.</p></div><div class="input-specification"><p>The first line of input contains single integer $t$ ($1 \le t \le 64$)&nbsp;— the number of test cases. The descriptions of test cases follow.</p><p>Each test case contains one string of two characters, description of the square where rook is positioned. The first character is a letter from <span class="tex-font-style-bf">a</span> to <span class="tex-font-style-bf">h</span>, the label of column, and the second character is a digit from <span class="tex-font-style-bf">1</span> to <span class="tex-font-style-bf">8</span>, the label of row. </p><p>The same position may occur in more than one test case.</p></div><div class="output-specification"><p>For each test case, output descriptions of all squares where the rook can move, in the same format as in the input. </p><p>You can output squares in any order per test case.</p></div>

## Input

<p>The first line of input contains single integer $t$ ($1 \le t \le 64$)&nbsp;— the number of test cases. The descriptions of test cases follow.</p><p>Each test case contains one string of two characters, description of the square where rook is positioned. The first character is a letter from <span class="tex-font-style-bf">a</span> to <span class="tex-font-style-bf">h</span>, the label of column, and the second character is a digit from <span class="tex-font-style-bf">1</span> to <span class="tex-font-style-bf">8</span>, the label of row. </p><p>The same position may occur in more than one test case.</p>

## Output

<p>For each test case, output descriptions of all squares where the rook can move, in the same format as in the input. </p><p>You can output squares in any order per test case.</p>





```input1|2
1
d5
```




```output1
d1
d2
b5
g5
h5
d3
e5
f5
d8
a5
d6
d7
c5
d4
```


