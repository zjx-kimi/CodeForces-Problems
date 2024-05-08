## Description

<div><p>All of us love treasures, right? That's why young Vasya is heading for a Treasure Island.</p><p>Treasure Island may be represented as a rectangular table $n \times m$ which is surrounded by the ocean. Let us number rows of the field with consecutive integers from $1$ to $n$ from top to bottom and columns with consecutive integers from $1$ to $m$ from left to right. Denote the cell in $r$-th row and $c$-th column as $(r, c)$. Some of the island cells contain impassable forests, and some cells are free and passable. Treasure is hidden in cell $(n, m)$.</p><p>Vasya got off the ship in cell $(1, 1)$. Now he wants to reach the treasure. He is hurrying up, so he can move only from cell to the cell in next row (downwards) or next column (rightwards), i.e. from cell $(x, y)$ he can move only to cells $(x+1, y)$ and $(x, y+1)$. Of course Vasya can't move through cells with impassable forests.</p><p>Evil Witch is aware of Vasya's journey and she is going to prevent him from reaching the treasure. Before Vasya's first move she is able to grow using her evil magic impassable forests in previously free cells. Witch is able to grow a forest in any number of any free cells except cells $(1, 1)$ where Vasya got off his ship and $(n, m)$ where the treasure is hidden.</p><p>Help Evil Witch by finding out the minimum number of cells she has to turn into impassable forests so that Vasya is no longer able to reach the treasure.</p></div><div class="input-specification"><p>First line of input contains two positive integers $n$, $m$ ($3 \le n \cdot m \le 1\,000\,000$), sizes of the island.</p><p>Following $n$ lines contains strings $s_i$ of length $m$ describing the island, $j$-th character of string $s_i$ equals "<span class="tex-font-style-tt">#</span>" if cell $(i, j)$ contains an impassable forest and "<span class="tex-font-style-tt">.</span>" if the cell is free and passable. Let us remind you that Vasya gets of his ship at the cell $(1, 1)$, i.e. the first cell of the first row, and he wants to reach cell $(n, m)$, i.e. the last cell of the last row.</p><p>It's guaranteed, that cells $(1, 1)$ and $(n, m)$ are empty.</p></div><div class="output-specification"><p>Print the only integer $k$, which is the minimum number of cells Evil Witch has to turn into impassable forest in order to prevent Vasya from reaching the treasure.</p></div>

## Input

<p>First line of input contains two positive integers $n$, $m$ ($3 \le n \cdot m \le 1\,000\,000$), sizes of the island.</p><p>Following $n$ lines contains strings $s_i$ of length $m$ describing the island, $j$-th character of string $s_i$ equals "<span class="tex-font-style-tt">#</span>" if cell $(i, j)$ contains an impassable forest and "<span class="tex-font-style-tt">.</span>" if the cell is free and passable. Let us remind you that Vasya gets of his ship at the cell $(1, 1)$, i.e. the first cell of the first row, and he wants to reach cell $(n, m)$, i.e. the last cell of the last row.</p><p>It's guaranteed, that cells $(1, 1)$ and $(n, m)$ are empty.</p>

## Output

<p>Print the only integer $k$, which is the minimum number of cells Evil Witch has to turn into impassable forest in order to prevent Vasya from reaching the treasure.</p>





```input1
2 2
..
..
```




```input2
4 4
....
#.#.
....
.#..
```




```input3
3 4
....
.##.
....
```




```output1
2
```




```output2
1
```




```output3
2
```



## Note

<p>The following picture illustrates the island in the third example. Blue arrows show possible paths Vasya may use to go from $(1, 1)$ to $(n, m)$. Red illustrates one possible set of cells for the Witch to turn into impassable forest to make Vasya's trip from $(1, 1)$ to $(n, m)$ impossible.</p><center> <img class="tex-graphics" src="file://GLaRs0wv.png" style="max-width: 100.0%;max-height: 100.0%;"> </center>
