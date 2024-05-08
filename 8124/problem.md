## Description

<div><p>Vasya decided to learn to play chess. Classic chess doesn't seem interesting to him, so he plays his own sort of chess.</p><p>The queen is the piece that captures all squares on its vertical, horizontal and diagonal lines. If the cell is located on the same vertical, horizontal or diagonal line with queen, and the cell contains a piece of the enemy color, the queen is able to move to this square. After that the enemy's piece is removed from the board. The queen cannot move to a cell containing an enemy piece if there is some other piece between it and the queen. </p><p>There is an <span class="tex-span"><i>n</i> × <i>n</i></span> chessboard. We'll denote a cell on the intersection of the <span class="tex-span"><i>r</i></span>-th row and <span class="tex-span"><i>c</i></span>-th column as <span class="tex-span">(<i>r</i>, <i>c</i>)</span>. The square <span class="tex-span">(1, 1)</span> contains the white queen and the square <span class="tex-span">(1, <i>n</i>)</span> contains the black queen. All other squares contain green pawns that don't belong to anyone.</p><p>The players move in turns. The player that moves first plays for the white queen, his opponent plays for the black queen.</p><p>On each move the player has to capture some piece with his queen (that is, move to a square that contains either a green pawn or the enemy queen). The player loses if either he cannot capture any piece during his move or the opponent took his queen during the previous move. </p><p>Help Vasya determine who wins if both players play with an optimal strategy on the board <span class="tex-span"><i>n</i> × <i>n</i></span>.</p></div><div class="input-specification"><p>The input contains a single number <span class="tex-span"><i>n</i></span> (<span class="tex-span">2 ≤ <i>n</i> ≤ 10<sup class="upper-index">9</sup></span>) — the size of the board.</p></div><div class="output-specification"><p>On the first line print the answer to problem — string "<span class="tex-font-style-tt">white</span>" or string "<span class="tex-font-style-tt">black</span>", depending on who wins if the both players play optimally. </p><p>If the answer is "<span class="tex-font-style-tt">white</span>", then you should also print two integers <span class="tex-span"><i>r</i></span> and <span class="tex-span"><i>c</i></span> representing the cell <span class="tex-span">(<i>r</i>, <i>c</i>)</span>, where the first player should make his first move to win. If there are multiple such cells, print the one with the minimum <span class="tex-span"><i>r</i></span>. If there are still multiple squares, print the one with the minimum <span class="tex-span"><i>c</i></span>.</p></div>

## Input

<p>The input contains a single number <span class="tex-span"><i>n</i></span> (<span class="tex-span">2 ≤ <i>n</i> ≤ 10<sup class="upper-index">9</sup></span>) — the size of the board.</p>

## Output

<p>On the first line print the answer to problem — string "<span class="tex-font-style-tt">white</span>" or string "<span class="tex-font-style-tt">black</span>", depending on who wins if the both players play optimally. </p><p>If the answer is "<span class="tex-font-style-tt">white</span>", then you should also print two integers <span class="tex-span"><i>r</i></span> and <span class="tex-span"><i>c</i></span> representing the cell <span class="tex-span">(<i>r</i>, <i>c</i>)</span>, where the first player should make his first move to win. If there are multiple such cells, print the one with the minimum <span class="tex-span"><i>r</i></span>. If there are still multiple squares, print the one with the minimum <span class="tex-span"><i>c</i></span>.</p>





```input1
2

```




```input2
3

```




```output1
white
1 2

```




```output2
black

```



## Note

<p>In the first sample test the white queen can capture the black queen at the first move, so the white player wins.</p><p>In the second test from the statement if the white queen captures the green pawn located on the central vertical line, then it will be captured by the black queen during the next move. So the only move for the white player is to capture the green pawn located at <span class="tex-span">(2, 1)</span>. </p><p>Similarly, the black queen doesn't have any other options but to capture the green pawn located at <span class="tex-span">(2, 3)</span>, otherwise if it goes to the middle vertical line, it will be captured by the white queen.</p><p>During the next move the same thing happens — neither the white, nor the black queen has other options rather than to capture green pawns situated above them. Thus, the white queen ends up on square <span class="tex-span">(3, 1)</span>, and the black queen ends up on square <span class="tex-span">(3, 3)</span>. </p><p>In this situation the white queen has to capture any of the green pawns located on the middle vertical line, after that it will be captured by the black queen. Thus, the player who plays for the black queen wins.</p>
