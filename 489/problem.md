## Description

<div><p>Rudolph invented the game of tic-tac-toe for three players. It has classic rules, except for the third player who plays with pluses. Rudolf has a $3 \times 3$ field &nbsp;— the result of the completed game. Each field cell contains either a cross, or a nought, or a plus sign, or nothing. The game is won by the player who makes a horizontal, vertical or diagonal row of $3$'s of their symbols.</p><p>Rudolph wants to find the result of the game. Either exactly one of the three players won or it ended in a draw. It is guaranteed that multiple players cannot win at the same time.</p></div><div class="input-specification"><p>The first line contains one integer $t$ ($1 \le t \le 10^4$) — the number of test cases.</p><p>Each test case consists of three lines, each of which consists of three characters. The symbol can be one of four: "X" means a cross, "O" means a nought, "+" means a plus, "." means an empty cell.</p></div><div class="output-specification"><p>For each test case, print the string "X" if the crosses won, "O" if the noughts won, "+" if the pluses won, "DRAW" if there was a draw.</p></div>

## Input

<p>The first line contains one integer $t$ ($1 \le t \le 10^4$) — the number of test cases.</p><p>Each test case consists of three lines, each of which consists of three characters. The symbol can be one of four: "X" means a cross, "O" means a nought, "+" means a plus, "." means an empty cell.</p>

## Output

<p>For each test case, print the string "X" if the crosses won, "O" if the noughts won, "+" if the pluses won, "DRAW" if there was a draw.</p>





```input1|2,3,4,8,9,10,14,15,16
5
+X+
OXO
OX.
O+.
+OX
X+O
.XO
OX.
+++
O.+
X.O
+..
.++
X.O
+..
```




```output1
X
O
+
DRAW
DRAW
```


