## Description

<div><p><span class="tex-font-style-it">This is an interactive problem.</span></p><p>Alice and Bob are playing a game on the chessboard of size $n \times m$ where $n$ and $m$ are <span class="tex-font-style-bf">even</span>. The rows are numbered from $1$ to $n$ and the columns are numbered from $1$ to $m$. There are two knights on the chessboard. A white one initially is on the position $(x_1, y_1)$, while the black one is on the position $(x_2, y_2)$. Alice will choose one of the knights to play with, and Bob will use the other one.</p><p>The Alice and Bob will play in turns and whoever controls <span class="tex-font-style-bf">the white</span> knight starts the game. During a turn, the player must move their knight adhering the chess rules. That is, if the knight is currently on the position $(x, y)$, it can be moved to any of those positions (as long as they are inside the chessboard):</p><center> $(x+1, y+2)$, $(x+1, y-2)$, $(x-1, y+2)$, $(x-1, y-2)$,<p>$(x+2, y+1)$, $(x+2, y-1)$, $(x-2, y+1)$, $(x-2, y-1)$. </p></center><p>We all know that knights are strongest in the middle of the board. Both knight have a single position they want to reach: </p><ul> <li> the owner of the white knight wins if it captures the black knight or if the white knight is at $(n/2, m/2)$ and this position is not under attack of the black knight at this moment; </li><li> The owner of the black knight wins if it captures the white knight or if the black knight is at $(n/2+1, m/2)$ and this position is not under attack of the white knight at this moment. </li></ul><p>Formally, the player who captures the other knight wins. The player who is at its target square ($(n/2, m/2)$ for white, $(n/2+1, m/2)$ for black) and this position is not under opponent's attack, also wins.</p><p>A position is under attack of a knight if it can move into this position. Capturing a knight means that a player moves their knight to the cell where the opponent's knight is.</p><p>If Alice made $350$ moves and nobody won, the game is a draw.</p><p>Alice is unsure in her chess skills, so she asks you for a help. Choose a knight and win the game for her. It can be shown, that Alice always has a winning strategy.</p></div><div><h2>Interaction</h2><p>The interaction starts with two integers $n$ and $m$ ($6 \le n,m \le 1000$, $n$ and $m$ are even) — the dimensions of the chessboard.</p><p>The second line contains four integers $x_1, y_1, x_2, y_2$ ($1 \le x_1, x_2 \le n$, $1 \le y_1, y_2 \le m$)&nbsp;— the positions of the white and the black knight. It is guaranteed that the two knights have different starting positions. It is also guaranteed that none of the knights are in their own target square in the beginning of the game (however, they can be on the opponent's target position).</p><p>Your program should reply with either "<span class="tex-font-style-tt">WHITE</span>" or "<span class="tex-font-style-tt">BLACK</span>", depending on the knight you want to play with. In case you select the white knight, you start the game.</p><p>During every your turn, you need to print two integers: $x$ and $y$, the position to move the knight. If you won the game by this turn, you must terminate your program immediately.</p><p>After every turn of the opponent, you will receive two integers: $x$ and $y$, the position where Bob moved his knight.</p><p>If your last move was illegal or you lost the game after jury's turn, or you made $350$ moves, and haven't won, you will receive "<span class="tex-font-style-tt">-1 -1</span>". In such cases, you should terminate your program and then you will get a <span class="tex-font-style-tt">Wrong Answer</span> verdict.</p><p>After printing anything, do not forget to output the end of line and flush the output. Otherwise, you might get <span class="tex-font-style-tt">Idleness limit exceeded</span>. To do this, use:</p><ul><li> <span class="tex-font-style-tt">fflush(stdout)</span> or <span class="tex-font-style-tt">cout.flush()</span> in C++;</li><li> <span class="tex-font-style-tt">System.out.flush()</span> in Java;</li><li> <span class="tex-font-style-tt">flush(output)</span> in Pascal;</li><li> <span class="tex-font-style-tt">stdout.flush()</span> in Python;</li><li> see documentation for other languages.</li></ul><p><span class="tex-font-style-bf">Hacks are disabled for this problem.</span></p><p>Jury's program is <span class="tex-font-style-it">adaptive</span>: the moves of jury may depend on the moves made by your program.</p></div>





```input1
8 8
2 3 1 8
```




```input2
6 6
4 4 2 2
6 3
```




```output1
WHITE
4 4
```




```output2
BLACK
4 3
```



## Note

<p>In the first example, the white knight can reach it's target square in one move.</p><p>In the second example black knight wins, no matter what white knight moves.</p>
