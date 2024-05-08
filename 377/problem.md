## Description

<div><p>Given a chessboard of size $N \times M$ ($N$ rows and $M$ columns). Each row is numbered from $1$ to $N$ from top to bottom and each column is numbered from $1$ to $M$ from left to right. The tile in row $r$ and column $c$ is denoted as $(r,c)$. There exists $K$ distinct special tiles on the chessboard with the $i$-th special tile being tile $(X_i,Y_i)$. It is guaranteed that tile $(1,1)$ is not a special tile.</p><p>A new chess piece has been invented, which is the castle. The castle moves similarly to a rook in regular chess, but slightly differently. In one move, a castle that is on some tile can only move to another tile in the same row or in the same column, but only in the right direction or the down direction. Formally, in one move, the castle on tile $(r,c)$ can only move to tile $(r',c')$ if and only if one of the following two conditions is satisfied: </p><ul> <li> $r'=r$ and $c'&gt;c$. </li><li> $c'=c$ and $r'&gt;r$. </li></ul><p>Chaneka and Bhinneka will play a game. In the beginning of the game, there is a castle in tile $(1,1)$. The two players will play alternatingly with Chaneka going first. In one turn, the player on that turn must move the castle following the movement rules of the castle.</p><p>If a player moves the castle to a special tile on her turn, then that player wins the game and the game ends. If on a turn, the castle cannot be moved, the player on that turn loses and the game ends.</p><p>Given the size of the board and the locations of each special tile. Determine the winner of this game if Chaneka and Bhinneka plays optimally.</p></div><div class="input-specification"><p>The first line contains three integers $N$, $M$, and $K$ ($1 \leq N,M \leq 2 \cdot 10^5$; $0 \leq K \leq \min(N \times M - 1, 2\cdot10^5)$) — the size of the chessboard and the number of special tiles.</p><p>The $i$-th of the next $K$ lines contains two integers $X_i$ and $Y_i$ ($1\leq X_i\leq N$; $1\leq Y_i\leq M$; $(X_i, Y_i) \neq (1,1)$) — the location of each special tile. The special tiles are pairwise distinct.</p></div><div class="output-specification"><p>Output <span class="tex-font-style-tt">Chaneka</span> if Chaneka is the winner, output <span class="tex-font-style-tt">Bhinneka</span> if Bhinneka is the winner.</p></div>

## Input

<p>The first line contains three integers $N$, $M$, and $K$ ($1 \leq N,M \leq 2 \cdot 10^5$; $0 \leq K \leq \min(N \times M - 1, 2\cdot10^5)$) — the size of the chessboard and the number of special tiles.</p><p>The $i$-th of the next $K$ lines contains two integers $X_i$ and $Y_i$ ($1\leq X_i\leq N$; $1\leq Y_i\leq M$; $(X_i, Y_i) \neq (1,1)$) — the location of each special tile. The special tiles are pairwise distinct.</p>

## Output

<p>Output <span class="tex-font-style-tt">Chaneka</span> if Chaneka is the winner, output <span class="tex-font-style-tt">Bhinneka</span> if Bhinneka is the winner.</p>





```input1
4 5 3
1 3
4 4
1 5
```




```input2
2 2 0
```




```output1
Chaneka
```




```output2
Bhinneka
```



## Note

<p>In the first example, the following is an illustration of the chessboard in the beginning of the game.</p><p> <img class="tex-graphics" src="file://RU5Uf3tS.png" style="max-width: 100.0%;max-height: 100.0%;" width="353px"></p><p>Chaneka can move the castle to special tile $(1,3)$ or $(1,5)$ directly on her first turn. Therefore, Chaneka is the winner.</p><p>In the second example, the following is an illustration of the chessboard in the beginning of the game.</p><p> <img class="tex-graphics" src="file://f1u3WZez.png" style="max-width: 100.0%;max-height: 100.0%;" width="158px"></p><p>Chaneka can only move the castle to tile $(1, 2)$ or $(2, 1)$ on her first turn. Whatever Chaneka does, Bhinneka will be able to directly move the castle to tile $(2, 2)$. After that, on Chaneka's turn, she cannot move the castle, so Chaneka loses. Therefore, Bhinneka is the winner.</p>
