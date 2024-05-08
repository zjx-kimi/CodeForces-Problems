## Description

<div><p>This is an interactive problem.</p><p>There is an $n$ by $n$ grid of conveyor belts, in positions $(1, 1)$ through $(n, n)$ of a coordinate plane. Every other square in the plane is empty. Each conveyor belt can be configured to move boxes up ('<span class="tex-font-style-tt">^</span>'), down ('<span class="tex-font-style-tt">v</span>'), left ('<span class="tex-font-style-tt">&lt;</span>'), or right ('<span class="tex-font-style-tt">&gt;</span>'). If a box moves onto an empty square, it stops moving.</p><p>However, one of the $n^2$ belts is stuck, and will always move boxes in the same direction, no matter how it is configured. Your goal is to perform a series of tests to determine which conveyor belt is stuck, and the direction in which it sends items.</p><p>To achieve this, you can perform up to $25$ tests. In each test, you assign a direction to all $n^2$ belts, place a box on top of one of them, and then turn all of the conveyors on. </p><center><img class="tex-graphics" src="file://cTFX3bpe.png" style="max-width: 100.0%;max-height: 100.0%;"><span class="tex-font-size-small">One possible result of a query with $n=4$. In this case, the box starts at $(2, 2)$. If there were no stuck conveyor, it would end up at $(5, 4)$, but because of the stuck '<span class="tex-font-style-tt">&gt;</span>' conveyor at $(3, 3)$, it enters an infinite loop.</span></center><p>The conveyors move the box around too quickly for you to see, so the only information you receive from a test is whether the box eventually stopped moving, and if so, the coordinates of its final position.</p></div><div><h2>Interaction</h2><p>You begin the interaction by reading a single integer $n$ ($2 \le n\le 100$)&nbsp;— the number of rows and columns in the grid.</p><p>Then, you can make at most $25$ queries.</p><p>Each query should begin with a line of the form <span class="tex-font-style-tt">? r c</span>, where <span class="tex-font-style-tt">r</span> and <span class="tex-font-style-tt">c</span> are the initial row and column of the box, respectively.</p><p>The next $n$ lines of the query should contain $n$ characters each. The $j$th character of the $i$th row should be one of '<span class="tex-font-style-tt">^</span>', '<span class="tex-font-style-tt">v</span>', '<span class="tex-font-style-tt">&lt;</span>', or '<span class="tex-font-style-tt">&gt;</span>', indicating the direction of conveyor $(i, j)$ for this query.</p><p>After each query, you will receive two integers $x$ and $y$. If $x = y = -1$, then the box entered an infinite loop. Otherwise, its final position was $(x, y)$.</p><p>If you make too many queries or make an invalid query, you will receive the <span class="tex-font-style-tt">Wrong Answer</span> verdict.</p><p>After you have found the stuck conveyor and its direction, print a single line <span class="tex-font-style-tt">! r c dir</span>, where <span class="tex-font-style-tt">r</span> and <span class="tex-font-style-tt">c</span> are the row and column of the stuck conveyor, respectively, and <span class="tex-font-style-tt">dir</span> is one of '<span class="tex-font-style-tt">^</span>', '<span class="tex-font-style-tt">v</span>', '<span class="tex-font-style-tt">&lt;</span>', or '<span class="tex-font-style-tt">&gt;</span>', indicating the direction of the stuck conveyor. Note that printing this answer does not count towards your total of $25$ queries. After printing this line, your program should terminate.</p><p>The interactor is non-adaptive. This means that the location and direction of the stuck belt is fixed at the start of the interaction, and does not change after the queries.</p><p>After printing a query do not forget to output the end of line and flush the output. Otherwise, you will get <span class="tex-font-style-tt">Idleness limit exceeded</span>. To do this, use:</p><ul> <li> <span class="tex-font-style-tt">fflush(stdout)</span> or <span class="tex-font-style-tt">cout.flush()</span> in C++; </li><li> <span class="tex-font-style-tt">System.out.flush()</span> in Java; </li><li> <span class="tex-font-style-tt">flush(output)</span> in Pascal; </li><li> <span class="tex-font-style-tt">stdout.flush()</span> in Python; </li><li> see the documentation for other languages. </li></ul><p><span class="tex-font-style-bf">Hacks</span></p><p>To make a hack, use the following format.</p><p>The first line should contain a single integer $n$ ($1 \le n \le 100$)&nbsp;— the number of rows and columns in the grid.</p><p>The next line should contain two integers $r$ and $c$ ($1 \le r, c \le n$), as well as a character $\mathrm{dir}$ ($\mathrm{dir}$ is one of '<span class="tex-font-style-tt">^</span>', '<span class="tex-font-style-tt">v</span>', '<span class="tex-font-style-tt">&lt;</span>', '<span class="tex-font-style-tt">&gt;</span>')&nbsp;— the position of the stuck conveyor and its fixed direction. These values should be separated by spaces.</p></div>





```input1
3




-1 -1




0 2
```




```input2
4





-1 -1
```




```output1
? 2 2
&gt;&gt;&lt;
&gt;&gt;v
^&lt;&lt;

? 1 1
&gt;&gt;&lt;
&gt;&gt;v
^&lt;&lt;

! 1 2 ^
```




```output2
? 2 2
v&gt;v&lt;
^v&lt;v
v&gt;v^
&gt;v&gt;v

! 3 3 &gt;
```



## Note

<p>For the first query of the first sample input, the box starts on $(2, 2)$ and enters an infinite loop containing rows $2$ and $3$. Because the stuck conveyor is in row $1$, it does not affect the outcome of the query.</p><p>For the second query of the first sample input, the conveyors are configured in the same way, but the box starts on $(1, 1)$. If there were no stuck conveyor, it would enter an infinite loop between $(1, 2)$ and $(1, 3)$. However, the stuck conveyor redirects it to $(0, 2)$.</p><p>After these two queries, the program is able to determine that the stuck conveyor is at $(1, 2)$ and directs items upward.</p><p>The query for the second sample input corresponds to the picture above. After asking the query, there are many possibilities for the stuck conveyor, but the program correctly guesses that it is at $(3, 3)$ and directs items to the right.</p>
