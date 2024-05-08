## Description

<div><p>The girl Umka loves to travel and participate in math olympiads. One day she was flying by plane to the next olympiad and out of boredom explored a huge checkered sheet of paper.</p><p>Denote the $n$-th Fibonacci number as $F_n = \begin{cases} 1, &amp; n = 0; \\ 1, &amp; n = 1; \\ F_{n-2} + F_{n-1}, &amp; n \ge 2. \end{cases}$</p><p>A checkered rectangle with a height of $F_n$ and a width of $F_{n+1}$ is called a Fibonacci rectangle <span class="tex-font-style-it">of order</span> $n$.</p><p>Umka has a Fibonacci rectangle <span class="tex-font-style-it">of order</span> $n$. Someone colored a cell in it at the intersection of the row $x$ and the column $y$.</p><p>It is necessary to cut this rectangle <span class="tex-font-style-bf">exactly</span> into $n+1$ squares in such way that</p><ul> <li> the painted cell was in a square with a side of $1$; </li><li> there was <span class="tex-font-style-bf">at most one</span> pair of squares with equal sides; </li><li> the side of each square was equal to a Fibonacci number. </li></ul><p>Will Umka be able to cut this rectangle in that way?</p></div><div class="input-specification"><p>The first line contains an integer $t$ ($1 \le t \le 2 \cdot 10^5$)&nbsp;— number of test cases.</p><p>For each test case the integers $n$, $x$, $y$ are given ($1 \le n \le 44$, $1 \le x \le F_n$, $1 \le y \le F_{n+1}$)&nbsp;— <span class="tex-font-style-it">the order</span> of the Fibonacci rectangle and the coordinates of the colored cell.</p></div><div class="output-specification"><p>For each test case, print "<span class="tex-font-style-tt">YES</span>" if the answer is positive, and "<span class="tex-font-style-tt">NO</span>" otherwise.</p><p>You can print "<span class="tex-font-style-tt">YES</span>" and "<span class="tex-font-style-tt">NO</span>" in any case (for example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>" and "<span class="tex-font-style-tt">Yes</span>" will be recognized as a positive answer).</p></div>

## Input

<p>The first line contains an integer $t$ ($1 \le t \le 2 \cdot 10^5$)&nbsp;— number of test cases.</p><p>For each test case the integers $n$, $x$, $y$ are given ($1 \le n \le 44$, $1 \le x \le F_n$, $1 \le y \le F_{n+1}$)&nbsp;— <span class="tex-font-style-it">the order</span> of the Fibonacci rectangle and the coordinates of the colored cell.</p>

## Output

<p>For each test case, print "<span class="tex-font-style-tt">YES</span>" if the answer is positive, and "<span class="tex-font-style-tt">NO</span>" otherwise.</p><p>You can print "<span class="tex-font-style-tt">YES</span>" and "<span class="tex-font-style-tt">NO</span>" in any case (for example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>" and "<span class="tex-font-style-tt">Yes</span>" will be recognized as a positive answer).</p>





```input1|2,4,6,8,10,12
12
1 1 1
2 1 2
3 1 4
3 3 2
4 4 6
4 3 3
5 6 5
5 4 12
5 2 12
4 2 1
1 1 2
44 758465880 1277583853
```




```output1
YES
NO
YES
YES
YES
NO
YES
NO
NO
YES
YES
NO
```



## Note

<center> <table class="tex-tabular"><tbody><tr><td class="tex-tabular-text-align-center"><img class="tex-graphics" src="file://K9WHU221.png" style="max-width: 100.0%;max-height: 100.0%;"></td><td class="tex-tabular-text-align-center"><img class="tex-graphics" src="file://Pf03kXNe.png" style="max-width: 100.0%;max-height: 100.0%;"></td><td><img class="tex-graphics" src="file://6Y4EzNXv.png" style="max-width: 100.0%;max-height: 100.0%;"></td></tr></tbody></table> <span class="tex-font-size-small">The first, third and fourth test cases.</span> </center>
