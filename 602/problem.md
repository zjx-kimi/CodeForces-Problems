## Description

<div><p><span class="tex-font-style-bf">This is an interactive problem.</span></p><p>There are $n$ distinct hidden points with real coordinates on a two-dimensional Euclidean plane. In one query, you can ask some line $ax + by + c = 0$ and get the projections of all $n$ points to this line in some order. The given projections are not exact, please read the interaction section for more clarity.</p><p>Using the minimum number of queries, guess all $n$ points and output them in some order. Here minimality means the minimum number of queries required to solve any possible test case with $n$ points.</p><p>The hidden points are fixed in advance and do not change throughout the interaction. In other words, the interactor is not adaptive.</p><p>A projection of point $A$ to line $ax + by + c = 0$ is the point on the line closest to $A$.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \leq t \leq 50$) — the number of test cases.</p><p>The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2 \leq n \leq 25$) — the number of hidden points.</p><p>For each test case, it is guaranteed that for any pair of hidden points, their $x$ coordinates differ by at least $1$. Analogously, $y$ coordinates of any pair also differ by at least $1$.</p><p>Coordinates $x$ and $y$ of all hidden points do not exceed $100$ by absolute value.</p></div><div><h2>Interaction</h2><p>To query a line $ax + by + c = 0$ you should print "<span class="tex-font-style-tt">? a b c</span>" where all <span class="tex-font-style-tt">a</span>, <span class="tex-font-style-tt">b</span> and <span class="tex-font-style-tt">c</span> are real numbers up to $100$ by absolute value. For less precision issues numbers $a$ and $b$ <span class="tex-font-style-bf">must satisfy the condition</span> $|a| + |b| \geq 0.1$, where $|a|$ is the absolute value of $a$. </p><p>As an answer to the query you will get $n$ points in the form "<span class="tex-font-style-tt">x_1 y_1 ... x_n y_n</span>", where points $(x_i, y_i)$ are projections to the line $ax + by + c = 0$. It is guaranteed that each printed point is no more than $10^{-4}$ away from the real projection point. Every coordinate is printed with at most 9 decimal places.</p><p>See the interaction example for more clarity.</p><p>If you ask too many queries, you will get <span class="tex-font-style-tt">Wrong answer</span>.</p><p>To output an answer you should print "<span class="tex-font-style-tt">! x_1 y_1 ... x_n y_n</span>", where $(x_i, y_i)$ are coordinates of the hidden points. You could output the hidden points in any order. The answer would be considered correct if each of the printed points is no more than $10^{-3}$ away from the corresponding hidden point. <span class="tex-font-style-bf">Printing the answer doesn't count as a query.</span></p><p>After printing a query or the answer, do not forget to output end of line and flush the output. Otherwise, you will get <span class="tex-font-style-tt">Idleness limit exceeded</span>. To do this, use:</p><ul> <li> <span class="tex-font-style-tt">fflush(stdout)</span> or <span class="tex-font-style-tt">cout.flush()</span> in C++; </li><li> <span class="tex-font-style-tt">System.out.flush()</span> in Java; </li><li> <span class="tex-font-style-tt">flush(output)</span> in Pascal; </li><li> <span class="tex-font-style-tt">stdout.flush()</span> in Python; </li><li> see the documentation for other languages </li></ul><p><span class="tex-font-style-bf"><span class="tex-font-style-section">Hacks</span></span></p><p>To make a hack, use the following test format.</p><p>In the first line output a single integer $t$ ($1 \leq t \leq 50$) — the number of test cases.</p><p>The description of the test cases follows.</p><p>In the first line of each test case output a single integer $n$ ($2 \leq n \leq 25$). In the next $n$ lines output two rational numbers each. The numbers in line $i$ should correspond to $x_i$ and $y_i$ respectively. Printed points must comply with all constraints from the input section.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \leq t \leq 50$) — the number of test cases.</p><p>The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2 \leq n \leq 25$) — the number of hidden points.</p><p>For each test case, it is guaranteed that for any pair of hidden points, their $x$ coordinates differ by at least $1$. Analogously, $y$ coordinates of any pair also differ by at least $1$.</p><p>Coordinates $x$ and $y$ of all hidden points do not exceed $100$ by absolute value.</p>





```input1
1
2

1 1 2.5 1

1.500000001 1.500000000 2 2
```




```output1
? 0 1 -1

? 0.2 -0.2 0

! 1 3 2.5 0.500000001
```



## Note

<p>In the sample the hidden points are $(1, 3)$ and $(2.5, 0.5)$</p><p>A picture, which describes the first query:</p><p><img class="tex-graphics" src="file://SZqohCSZ.png" style="max-width: 100.0%;max-height: 100.0%;"></p><p>A picture, which describes the second query:</p><p><img class="tex-graphics" src="file://C3BsC6Cv.png" style="max-width: 100.0%;max-height: 100.0%;"></p>
