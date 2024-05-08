## Description

<div><p>Alice suggested Bob to play a game. Bob didn't like this idea, but he couldn't refuse Alice, so he asked you to write a program that would play instead of him.</p><p>The game starts with Alice taking out a grid sheet of size $n \times n$, the cells of which are <span class="tex-font-style-bf">initially not colored</span>. After that she colors some $2n$ cells with colors $1,2,\ldots, 2n$, respectively, and informs Bob about these cells.</p><p>In one move, Bob can point to a cell that has not been colored yet and ask Alice to color that cell. Alice colors that cell with one of the $2n$ colors of her choice, informing Bob of the chosen color. Bob can make no more than $10$ moves, after which he needs to find a <span class="tex-font-style-it">good</span> set of four cells.</p><p>A set of four cells is considered good if the following conditions are met:</p><ul> <li> All the cells in the set are colored; </li><li> No two cells in the set are colored with the same color; </li><li> The centers of the cells form a rectangle with sides parallel to the grid lines. </li></ul></div><div class="input-specification"><p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 200$) — the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($3 \le n \le 1000$) — the size of the grid.</p><p>The $i$-th of the following $2n$ lines contains two integers $x_i$ and $y_i$ ($1 \le x_i, y_i \le n$) — the coordinates of the cell colored with the $i$-th color.</p><p>It is guaranteed that all coordinates $(x_i, y_i)$ are pairwise distinct for the same test case.</p><p>After reading the input data for each test case, continue the interaction as described below.</p></div><div><h2>Interaction</h2><p>You can make no more than $10$ moves. To make a move, output "<span class="tex-font-style-tt">?</span> $x$ $y$" ($1 \leq x,y \leq n$). In response to this, the jury's program will output a single integer from $1$ to $2n$&nbsp;— the color of cell $(x,y)$.</p><p>After all moves (it is not necessary to make all $10$ moves and it is not necessary to make at least one move), output a string in the format "<span class="tex-font-style-tt">!</span> $x_1$ $x_2$ $y_1$ $y_2$" ($1 \leq x_1, x_2, y_1, y_2 \leq n, x_1 \ne x_2, y_1 \ne y_2$). If cells $(x_1, y_1)$, $(x_1, y_2)$, $(x_2, y_1)$, $(x_2, y_2)$ are colored with different colors, the jury's program will output "<span class="tex-font-style-tt">OK</span>". After that, proceed to the next test case or terminate the program if there are no more test cases left.</p><p>Otherwise, if any of the specified cells are colored with the same color or one of the cells is not colored yet, the jury's program will output "<span class="tex-font-style-tt">ERROR</span>". In this case, your program should immediately terminate its execution to receive the <span class="tex-font-style-tt">Wrong Answer</span> verdict. Otherwise, you may receive an arbitrary verdict.</p><p>After each move or answer, do not forget to output the end of line and flush the output. Otherwise, you will get the <span class="tex-font-style-tt">Idleness limit exceeded</span> verdict.</p><p>To do this, use:</p><ul> <li> <span class="tex-font-style-tt">fflush(stdout)</span> or <span class="tex-font-style-tt">cout.flush()</span> in C++; </li><li> <span class="tex-font-style-tt">System.out.flush()</span> in Java; </li><li> <span class="tex-font-style-tt">flush(output)</span> in Pascal; </li><li> <span class="tex-font-style-tt">stdout.flush()</span> in Python; </li><li> see documentation for other languages. </li></ul><p>Note that the interactor is <span class="tex-font-style-bf">adaptive</span>, meaning that the color Alice will use to color the cells during Bob's moves is not fixed in advance.</p><p><span class="tex-font-style-bf">Hacks</span></p><p>You cannot use hacks in this problem.</p></div>

## Input

<p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 200$) — the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($3 \le n \le 1000$) — the size of the grid.</p><p>The $i$-th of the following $2n$ lines contains two integers $x_i$ and $y_i$ ($1 \le x_i, y_i \le n$) — the coordinates of the cell colored with the $i$-th color.</p><p>It is guaranteed that all coordinates $(x_i, y_i)$ are pairwise distinct for the same test case.</p><p>After reading the input data for each test case, continue the interaction as described below.</p>





```input1
2
3
1 2
1 3
2 1
2 3
3 1
3 2

1

OK
3
1 1
1 2
1 3
2 1
2 2
2 3

OK
```




```output1
? 1 1

! 1 2 1 3








! 1 2 1 2
```



## Note

<p>In the first test case:</p><center>  <img class="tex-graphics" src="file://8MccnKsr.png" style="max-width: 100.0%;max-height: 100.0%;" width="600px">   </center><p>In the second test case, cells with coordinates $(1, 1), (1, 2), (2, 1), (2, 2)$ are initially colored by Alice in different colors.</p>
