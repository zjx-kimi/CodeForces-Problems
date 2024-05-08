## Description

<div><p>You are playing "Grid Game 2" with your friend. There is a grid with $10^9$ rows (numbered from $1$ to $10^9$) and $10^9$ columns (numbered from $1$ to $10^9$). The cell at row $r$ and column $c$ is denoted as $(r, c)$.</p><p>Each cell can have a colour of either black or white. Initially, there are exactly $N$ black cells (numbered from $1$ to $N$). Black cell $i$ is located at $(R_i, C_i)$. The rest of the cells are white.</p><p>You and your friend will alternately take turn playing on this grid, and you are playing in the first turn. In one turn, a player will choose a black cell $(r, c)$, then toggle cells $(r - x, c - y)$ for all $0 \leq x, y &lt; \min(r, c)$. If a cell is toggled, then the cell becomes black if it was a white cell, and the cell becomes white if it was a black cell.</p><p>For example, the following illustration shows how the grid changes after a player chooses a black cell $(5, 4)$ in their turn.</p><center> <img class="tex-graphics" src="file://SIrJOTcx.png" style="max-width: 100.0%;max-height: 100.0%;" width="302px"> </center><p>A player who is unable to play on their turn, i.e. no remaining black cells, loses the game, and the opposing player wins the game. If you and your friend are playing optimally, determine who will win the game.</p></div><div class="input-specification"><p>The first line consists of an integer $N$ ($1 \le N \le 200\,000$).</p><p>Each of the next $N$ lines consists of two integers $R_i$ $C_i$ ($1 \leq R_i, C_i \leq 10^9)$. For $1 \leq i &lt; j \leq N$, $(R_i, C_i) \neq (R_j, C_j)$.</p></div><div class="output-specification"><p>Output <span class="tex-font-style-tt">FIRST</span> if you will win the game, or <span class="tex-font-style-tt">SECOND</span> otherwise.</p></div>

## Input

<p>The first line consists of an integer $N$ ($1 \le N \le 200\,000$).</p><p>Each of the next $N$ lines consists of two integers $R_i$ $C_i$ ($1 \leq R_i, C_i \leq 10^9)$. For $1 \leq i &lt; j \leq N$, $(R_i, C_i) \neq (R_j, C_j)$.</p>

## Output

<p>Output <span class="tex-font-style-tt">FIRST</span> if you will win the game, or <span class="tex-font-style-tt">SECOND</span> otherwise.</p>





```input1
2
2 3
2 4
```




```input2
1
2 2
```




```input3
13
1 1
1 4
1 5
2 1
2 4
2 5
4 1
4 2
4 4
5 1
5 2
5 4
5 5
```




```output1
FIRST
```




```output2
SECOND
```




```output3
SECOND
```



## Note

<p><span class="tex-font-style-it">Explanation for the sample input/output #1</span></p><p>You can start your move by choosing $(2, 4)$, whose effect was demonstrated in the following illustration.</p><center> <img class="tex-graphics" src="file://HttqDGVl.png" style="max-width: 100.0%;max-height: 100.0%;" width="302px"> </center><p>The remaining black cells are $(1, 3)$ and $(1, 4)$, each of which will only toggle itself when chosen. Whichever your friend chooses on the next move, the you can choose the remaining black cell.</p><p><span class="tex-font-style-it">Explanation for the sample input/output #2</span></p><p>You have only one cell to choose, and will toggle cells $(1, 1)$, $(1, 2)$, $(2, 1)$, and $(2, 2)$. Your friend and you will alternately choose the remaining black cells with your friend choosing the last black cell.</p>
