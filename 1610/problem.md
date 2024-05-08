## Description

<div><p>Marin feels exhausted after a long day of cosplay, so Gojou invites her to play a game!</p><p>Marin and Gojou take turns to place one of their tokens on an $n \times n$ grid with Marin starting first. There are some restrictions and allowances on where to place tokens: </p><ul> <li> Apart from the first move, the token placed by a player must be more than Manhattan distance $k$ away from the previous token placed on the matrix. In other words, if a player places a token at $(x_1, y_1)$, then the token placed <span class="tex-font-style-bf">by the other player</span> in the next move must be in a cell $(x_2, y_2)$ satisfying $|x_2 - x_1| + |y_2 - y_1| &gt; k$. </li><li> Apart from the previous restriction, a token can be placed anywhere on the matrix, <span class="tex-font-style-bf">including cells where tokens were previously placed by any player</span>. </li></ul><p>Whenever a player places a token on cell $(x, y)$, that player gets $v_{x,\ y}$ points. All values of $v$ on the grid are <span class="tex-font-style-bf">distinct</span>. You still get points from a cell even if tokens were already placed onto the cell. The game finishes when each player makes $10^{100}$ moves.</p><p>Marin and Gojou will play $n^2$ games. For each cell of the grid, there will be exactly one game where Marin places a token on that cell on her first move. Please answer for each game, if Marin and Gojou play optimally (after Marin's first move), who will have more points at the end? Or will the game end in a draw (both players have the same points at the end)?</p></div><div class="input-specification"><p>The first line contains two integers $n$, $k$ ($3 \le n \le 2000$, $1 \leq k \leq n - 2$). Note that under these constraints it is always possible to make a move.</p><p>The following $n$ lines contains $n$ integers each. The $j$-th integer in the $i$-th line is $v_{i,j}$ ($1 \le v_{i,j} \le n^2$). All elements in $v$ are distinct.</p></div><div class="output-specification"><p>You should print $n$ lines. In the $i$-th line, print $n$ characters, where the $j$-th character is the result of the game in which Marin places her first token in the cell $(i, j)$. Print '<span class="tex-font-style-tt">M</span>' if Marin wins, '<span class="tex-font-style-tt">G</span>' if Gojou wins, and '<span class="tex-font-style-tt">D</span>' if the game ends in a draw. Do not print spaces between the characters in one line.</p></div>

## Input

<p>The first line contains two integers $n$, $k$ ($3 \le n \le 2000$, $1 \leq k \leq n - 2$). Note that under these constraints it is always possible to make a move.</p><p>The following $n$ lines contains $n$ integers each. The $j$-th integer in the $i$-th line is $v_{i,j}$ ($1 \le v_{i,j} \le n^2$). All elements in $v$ are distinct.</p>

## Output

<p>You should print $n$ lines. In the $i$-th line, print $n$ characters, where the $j$-th character is the result of the game in which Marin places her first token in the cell $(i, j)$. Print '<span class="tex-font-style-tt">M</span>' if Marin wins, '<span class="tex-font-style-tt">G</span>' if Gojou wins, and '<span class="tex-font-style-tt">D</span>' if the game ends in a draw. Do not print spaces between the characters in one line.</p>





```input1
3 1
1 2 4
6 8 3
9 5 7
```




```output1
GGG
MGG
MGG
```


