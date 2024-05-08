## Description

<div><p>An ant moves on the real line with constant speed of $1$ unit per second. It starts at $0$ and always moves to the right (so its position increases by $1$ each second).</p><p>There are $n$ portals, the $i$-th of which is located at position $x_i$ and teleports to position $y_i &lt; x_i$. Each portal can be either <span class="tex-font-style-it">active</span> or <span class="tex-font-style-it">inactive</span>. The initial state of the $i$-th portal is determined by $s_i$: if $s_i=0$ then the $i$-th portal is initially inactive, if $s_i=1$ then the $i$-th portal is initially active. When the ant travels through a portal (i.e., when its position coincides with the position of a portal): </p><ul> <li> if the portal is inactive, it becomes active (in this case the path of the ant is not affected); </li><li> if the portal is active, it becomes inactive and the ant is instantly teleported to the position $y_i$, where it keeps on moving as normal. </li></ul><p>How long (from the instant it starts moving) does it take for the ant to reach the position $x_n + 1$? It can be shown that this happens in a finite amount of time. Since the answer may be very large, compute it modulo $998\,244\,353$.</p></div><div class="input-specification"><p>The first line contains the integer $n$ ($1\le n\le 2\cdot 10^5$) — the number of portals.</p><p>The $i$-th of the next $n$ lines contains three integers $x_i$, $y_i$ and $s_i$ ($1\le y_i &lt; x_i\le 10^9$, $s_i\in\{0,1\}$) — the position of the $i$-th portal, the position where the ant is teleported when it travels through the $i$-th portal (if it is active), and the initial state of the $i$-th portal.</p><p>The positions of the portals are strictly increasing, that is $x_1&lt;x_2&lt;\cdots&lt;x_n$. It is guaranteed that the $2n$ integers $x_1, \, x_2, \, \dots, \, x_n, \, y_1, \, y_2, \, \dots, \, y_n$ are all distinct.</p></div><div class="output-specification"><p>Output the amount of time elapsed, in seconds, from the instant the ant starts moving to the instant it reaches the position $x_n+1$. Since the answer may be very large, output it modulo $998\,244\,353$.</p></div>

## Input

<p>The first line contains the integer $n$ ($1\le n\le 2\cdot 10^5$) — the number of portals.</p><p>The $i$-th of the next $n$ lines contains three integers $x_i$, $y_i$ and $s_i$ ($1\le y_i &lt; x_i\le 10^9$, $s_i\in\{0,1\}$) — the position of the $i$-th portal, the position where the ant is teleported when it travels through the $i$-th portal (if it is active), and the initial state of the $i$-th portal.</p><p>The positions of the portals are strictly increasing, that is $x_1&lt;x_2&lt;\cdots&lt;x_n$. It is guaranteed that the $2n$ integers $x_1, \, x_2, \, \dots, \, x_n, \, y_1, \, y_2, \, \dots, \, y_n$ are all distinct.</p>

## Output

<p>Output the amount of time elapsed, in seconds, from the instant the ant starts moving to the instant it reaches the position $x_n+1$. Since the answer may be very large, output it modulo $998\,244\,353$.</p>





```input1
4
3 2 0
6 5 1
7 4 0
8 1 1
```




```input2
1
454971987 406874902 1
```




```input3
5
243385510 42245605 0
644426565 574769163 0
708622105 208990040 0
786625660 616437691 0
899754846 382774619 0
```




```input4
5
200000000 100000000 1
600000000 400000000 0
800000000 300000000 0
900000000 700000000 1
1000000000 500000000 0
```




```output1
23
```




```output2
503069073
```




```output3
899754847
```




```output4
3511295
```



## Note

<p><span class="tex-font-style-bf">Explanation of the first sample:</span> The ant moves as follows (a curvy arrow denotes a teleporting, a straight arrow denotes normal movement with speed $1$ and the time spent during the movement is written above the arrow). $$ 0 \stackrel{6}{\longrightarrow} 6 \leadsto 5 \stackrel{3}{\longrightarrow} 8 \leadsto 1 \stackrel{2}{\longrightarrow} 3 \leadsto 2 \stackrel{4}{\longrightarrow} 6 \leadsto 5 \stackrel{2}{\longrightarrow} 7 \leadsto 4 \stackrel{2}{\longrightarrow} 6 \leadsto 5 \stackrel{4}{\longrightarrow} 9 $$ Notice that the total time is $6+3+2+4+2+2+4=23$.</p><p><span class="tex-font-style-bf">Explanation of the second sample:</span> The ant moves as follows (a curvy arrow denotes a teleporting, a straight arrow denotes normal movement with speed $1$ and the time spent during the movement is written above the arrow). $$ 0 \stackrel{454971987}{\longrightarrow} 454971987 \leadsto 406874902 \stackrel{48097086}{\longrightarrow} 454971988 $$ Notice that the total time is $454971987+48097086=503069073$.</p><p><span class="tex-font-style-bf">Explanation of the third sample:</span> Since all portals are initially off, the ant will not be teleported and will go straight from $0$ to $x_n+1=899754846+1=899754847$.</p>
