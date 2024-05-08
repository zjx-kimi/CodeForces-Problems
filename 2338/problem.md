## Description

<div><p>Alice and Bob have a rectangular board consisting of $n$ rows and $m$ columns. <span class="tex-font-style-bf">Each row contains exactly one chip.</span></p><p>Alice and Bob play the following game. They choose two integers $l$ and $r$ such that $1 \le l \le r \le m$ and cut the board in such a way that only the part of it between column $l$ and column $r$ (inclusive) remains. So, all columns to the left of column $l$ and all columns to the right of column $r$ no longer belong to the board.</p><p>After cutting the board, they move chips on the remaining part of the board (the part from column $l$ to column $r$). They make alternating moves, and the player which cannot make a move loses the game. The first move is made by Alice, the second — by Bob, the third — by Alice, and so on. During their move, the player must choose one of the chips from the board and move it any positive number of cells to the left (so, if the chip was in column $i$, it can move to any column $j &lt; i$, and the chips in the leftmost column cannot be chosen).</p><p>Alice and Bob have $q$ pairs of numbers $L_i$ and $R_i$. For each such pair, they want to determine who will be the winner of the game if $l = L_i$ and $r = R_i$. Note that these games should be considered independently (they don't affect the state of the board for the next games), and both Alice and Bob play optimally.</p></div><div class="input-specification"><p>The first line contains two integers $n$ and $m$ ($1 \le n, m \le 2 \cdot 10^5$) — the number of rows and columns on the board, respectively.</p><p>The second line contains $n$ integers $c_1, c_2, \dots, c_n$ ($1 \le c_i \le m$), where $c_i$ is the index of the column where the chip in the $i$-th row is located (so, the chip in the $i$-th row is in the $c_i$-th column).</p><p>The third line contains one integer $q$ ($1 \le q \le 2 \cdot 10^5$).</p><p>Then $q$ lines follow, the $i$-th of them contains two integers $L_i$ and $R_i$ ($1 \le L_i \le R_i \le m$).</p></div><div class="output-specification"><p>Print a string of $q$ characters. The $i$-th character should be <span class="tex-font-style-tt">A</span> if Alice wins the game with $l = L_i$ and $r = R_i$, or <span class="tex-font-style-tt">B</span> if Bob wins it.</p></div>

## Input

<p>The first line contains two integers $n$ and $m$ ($1 \le n, m \le 2 \cdot 10^5$) — the number of rows and columns on the board, respectively.</p><p>The second line contains $n$ integers $c_1, c_2, \dots, c_n$ ($1 \le c_i \le m$), where $c_i$ is the index of the column where the chip in the $i$-th row is located (so, the chip in the $i$-th row is in the $c_i$-th column).</p><p>The third line contains one integer $q$ ($1 \le q \le 2 \cdot 10^5$).</p><p>Then $q$ lines follow, the $i$-th of them contains two integers $L_i$ and $R_i$ ($1 \le L_i \le R_i \le m$).</p>

## Output

<p>Print a string of $q$ characters. The $i$-th character should be <span class="tex-font-style-tt">A</span> if Alice wins the game with $l = L_i$ and $r = R_i$, or <span class="tex-font-style-tt">B</span> if Bob wins it.</p>





```input1
8 10
1 3 3 7 4 2 6 9
7
2 3
1 3
1 4
1 10
5 10
8 10
9 10
```




```output1
BAAAAAB
```


