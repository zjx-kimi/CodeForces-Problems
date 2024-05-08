## Description

<div><p><span class="tex-font-style-it">This is an interactive problem.</span></p><p><span class="tex-font-style-it">Made in Heaven</span> is a rather curious Stand. Of course, it is (arguably) the strongest Stand in existence, but it is also an ardent puzzle enjoyer. For example, it gave Qtaro the following problem recently:</p><p><span class="tex-font-style-it">Made in Heaven</span> has $n$ hidden integers $a_1, a_2, \dots, a_n$ ($3 \le n \le 5000$, $1 \le a_i \le 4$). Qtaro must determine all the $a_i$ by asking <span class="tex-font-style-it">Made in Heaven</span> some queries of the following form: </p><ul> <li> In one query Qtaro is allowed to give <span class="tex-font-style-it">Made in Heaven</span> three <span class="tex-font-style-bf">distinct</span> indexes $i$, $j$ and $k$ ($1 \leq i, j, k \leq n$). </li><li> If $a_i, a_j, a_k$ form the sides of a non-degenerate triangle$^\dagger$, <span class="tex-font-style-it">Made in Heaven</span> will respond with the area of this triangle. </li><li> Otherwise, <span class="tex-font-style-it">Made in Heaven</span> will respond with $0$. </li></ul><p>By asking at most $5500$ such questions, Qtaro must either tell <span class="tex-font-style-it">Made in Heaven</span> all the values of the $a_i$, or report that it is <span class="tex-font-style-bf">not</span> possible to <span class="tex-font-style-bf">uniquely</span> determine them.</p><p>Unfortunately due to the universe reboot, Qtaro is not as smart as Jotaro. Please help Qtaro solve <span class="tex-font-style-it">Made In Heaven</span>'s problem. </p><center> —————————————————————— </center><p>$^\dagger$ Three positive integers $a, b, c$ are said to form the sides of a non-degenerate triangle if and only if all of the following three inequalities hold: </p><ul> <li> $a+b &gt; c$, </li><li> $b+c &gt; a$, </li><li> $c+a &gt; b$. </li></ul></div><div><h2>Interaction</h2><p>The interaction begins with reading $n$ ($3 \le n \le 5000$), the number of hidden integers. </p><p>To ask a question corresponding to the triple $(i, j, k)$ ($1 \leq i &lt; j &lt; k \leq n$), output "<span class="tex-font-style-tt">?</span> $i$ $j$ $k$" without quotes. Afterward, you should read a <span class="tex-font-style-bf">single integer</span> $s$. </p><ul> <li> If $s = 0$, then $a_i$, $a_j$, and $a_k$ are not the sides of a non-degenerate triangle. </li><li> Otherwise, $s = 16 \Delta^2$, where $\Delta$ is the area of the triangle. The area is provided in this format for your convenience so that you need only take integer input. </li></ul><p>If the numbers $a_i$ cannot be uniquely determined print "<span class="tex-font-style-tt">!</span> $-1$" without quotes. On the other hand, if you have determined all the values of $a_i$ print "<span class="tex-font-style-tt">!</span> $a_1$ $a_2$ $\dots$ $a_n$" on a single line.</p><p>The interactor is <span class="tex-font-style-bf">non-adaptive</span>. The hidden array $a_1, a_2, \dots, a_n$ is <span class="tex-font-style-bf">fixed</span> beforehand and <span class="tex-font-style-bf">is not changed</span> during the interaction process.</p><p>After printing a query do not forget to output the end of line and flush the output. Otherwise, you will get <span class="tex-font-style-tt">Idleness limit exceeded</span>. To do this, use: </p><ul> <li> <span class="tex-font-style-tt">fflush(stdout)</span> or <span class="tex-font-style-tt">cout.flush()</span> in C++; </li><li> <span class="tex-font-style-tt">System.out.flush()</span> in Java; </li><li> <span class="tex-font-style-tt">flush(output)</span> in Pascal; </li><li> <span class="tex-font-style-tt">stdout.flush()</span> in Python; </li><li> see the documentation for other languages. </li></ul><p><span class="tex-font-style-bf">Hacks</span></p><p>You can hack a solution with the following input format.</p><p>The first line contains a single integer $n$ ($3 \le n \le 5000$)&nbsp;— the number of hidden integers.</p><p>The second line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le 4$)&nbsp;— the hidden array.</p></div>





```input1
3

63
```




```input2
6

0

0

0

63

15

135
```




```input3
15

3

3

3

3

3

0
```




```input4
15

3

15

0

3

3

3
```




```input5
10

3

48

3

48

63

0
```




```output1
? 1 2 3

! -1
```




```output2
? 1 2 3

? 2 3 4

? 4 5 6

? 1 5 6

? 3 5 6

? 1 2 4

! 3 2 1 4 2 2
```




```output3
? 1 2 3

? 4 6 7

? 8 9 10

? 11 12 13

? 13 14 15

? 4 5 6

! -1
```




```output4
? 1 2 3

? 3 4 5

? 4 5 6

? 7 8 9

? 10 11 12

? 13 14 15

! 1 1 1 2 2 4 1 1 1 1 1 1 1 1 1 1
```




```output5
? 1 3 5

? 4 6 8

? 1 5 9

? 6 8 10

? 4 2 6

? 7 10 8

! 1 3 1 2 1 2 4 2 1 2
```



## Note

<p>In the first example, the interaction process happens as follows:</p><center> <table class="tex-tabular"><tbody><tr><td class="tex-tabular-text-align-right tex-tabular-border-right tex-tabular-border-bottom"><span class="tex-font-style-bf">Stdin</span></td><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-right tex-tabular-border-bottom"><span class="tex-font-style-bf">Stdout</span></td><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-bottom"><span class="tex-font-style-bf">Explanation</span></td></tr><tr><td class="tex-tabular-text-align-right tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom"><span class="tex-font-style-tt">3</span></td><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom"></td><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-top tex-tabular-border-bottom">Read $n = 3$. There are $3$ hidden integers</td></tr><tr><td class="tex-tabular-text-align-right tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom"></td><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom"><span class="tex-font-style-tt">? 1 2 3</span></td><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-top tex-tabular-border-bottom">Ask for the area formed by $a_1$, $a_2$ and $a_3$</td></tr><tr><td class="tex-tabular-text-align-right tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom"><span class="tex-font-style-tt">63</span></td><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom"></td><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-top tex-tabular-border-bottom">Received $16\Delta^2 = 63$. So the area $\Delta = \sqrt{\frac{63}{16}} \approx 1.984313$</td></tr><tr><td class="tex-tabular-text-align-right tex-tabular-border-right tex-tabular-border-top"></td><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-right tex-tabular-border-top"><span class="tex-font-style-tt">! -1</span></td><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-top">Answer that there is no <span class="tex-font-style-bf">unique</span> array satisfying the queries.</td></tr></tbody></table> </center><p>From the area received, we can deduce that the numbers that forms the triangle are either ($4$, $4$, $1$) or ($3$, $2$, $2$) (in some order). As there are multiple arrays of numbers that satisfy the queries, a unique answer cannot be found.</p><p>In the second example, the interaction process happens as follows:</p><center> <table class="tex-tabular"><tbody><tr><td class="tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-bottom"><span class="tex-font-style-bf">Step</span></td><td class="tex-tabular-border-left tex-tabular-text-align-right tex-tabular-border-right tex-tabular-border-bottom"><span class="tex-font-style-bf">Stdin</span></td><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-right tex-tabular-border-bottom"><span class="tex-font-style-bf">Stdout</span></td><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-bottom"><span class="tex-font-style-bf">Explanation</span></td></tr><tr><td class="tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">1</td><td class="tex-tabular-border-left tex-tabular-text-align-right tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom"><span class="tex-font-style-tt">6</span></td><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom"></td><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-top tex-tabular-border-bottom">Read $n = 6$. There are $6$ hidden integers</td></tr><tr><td class="tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">2</td><td class="tex-tabular-border-left tex-tabular-text-align-right tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom"></td><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom"><span class="tex-font-style-tt">? 1 2 3</span></td><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-top tex-tabular-border-bottom">Ask for the area formed by $a_1$, $a_2$ and $a_3$</td></tr><tr><td class="tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">3</td><td class="tex-tabular-border-left tex-tabular-text-align-right tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom"><span class="tex-font-style-tt">0</span></td><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom"></td><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-top tex-tabular-border-bottom">Does not form a non-degenerate triangle</td></tr><tr><td class="tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">4</td><td class="tex-tabular-border-left tex-tabular-text-align-right tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom"></td><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom"><span class="tex-font-style-tt">? 2 3 4</span></td><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-top tex-tabular-border-bottom">Ask for the area formed by $a_2$, $a_3$ and $a_4$</td></tr><tr><td class="tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">5</td><td class="tex-tabular-border-left tex-tabular-text-align-right tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom"><span class="tex-font-style-tt">0</span></td><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom"></td><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-top tex-tabular-border-bottom">Does not form a non-degenerate triangle</td></tr><tr><td class="tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">6</td><td class="tex-tabular-border-left tex-tabular-text-align-right tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom"></td><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom"><span class="tex-font-style-tt">? 4 5 6</span></td><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-top tex-tabular-border-bottom">Ask for the area formed by $a_4$, $a_5$ and $a_6$</td></tr><tr><td class="tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">7</td><td class="tex-tabular-border-left tex-tabular-text-align-right tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom"><span class="tex-font-style-tt">0</span></td><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom"></td><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-top tex-tabular-border-bottom">Does not form a non-degenerate triangle</td></tr><tr><td class="tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top"></td></tr><tr><td class="tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-bottom">8</td><td class="tex-tabular-border-left tex-tabular-text-align-right tex-tabular-border-right tex-tabular-border-bottom"></td><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-right tex-tabular-border-bottom"><span class="tex-font-style-tt">? 1 5 6</span></td><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-bottom">Ask for the area formed by $a_1$, $a_5$ and $a_6$</td></tr><tr><td class="tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">9</td><td class="tex-tabular-border-left tex-tabular-text-align-right tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom"><span class="tex-font-style-tt">63</span></td><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom"></td><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-top tex-tabular-border-bottom">Received $16\Delta^2 = 63$. So the area $\Delta = \sqrt{\frac{63}{16}} \approx 1.984313$</td></tr><tr><td class="tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">10</td><td class="tex-tabular-border-left tex-tabular-text-align-right tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom"></td><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom"><span class="tex-font-style-tt">? 3 5 6</span></td><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-top tex-tabular-border-bottom">Ask for the area formed by $a_3$, $a_5$ and $a_6$</td></tr><tr><td class="tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">11</td><td class="tex-tabular-border-left tex-tabular-text-align-right tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom"><span class="tex-font-style-tt">15</span></td><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom"></td><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-top tex-tabular-border-bottom">Received $16\Delta^2 = 15$. So the area $\Delta = \sqrt{\frac{15}{16}} \approx 0.968245$</td></tr><tr><td class="tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">12</td><td class="tex-tabular-border-left tex-tabular-text-align-right tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom"></td><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom"><span class="tex-font-style-tt">? 1 2 4</span></td><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-top tex-tabular-border-bottom">Ask for the area formed by $a_3$, $a_5$ and $a_6$</td></tr><tr><td class="tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">13</td><td class="tex-tabular-border-left tex-tabular-text-align-right tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom"><span class="tex-font-style-tt">135</span></td><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom"></td><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-top tex-tabular-border-bottom">Received $16\Delta^2 = 135$. So the area $\Delta = \sqrt{\frac{135}{16}} \approx 2.904738$</td></tr><tr><td class="tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top">14</td><td class="tex-tabular-border-left tex-tabular-text-align-right tex-tabular-border-right tex-tabular-border-top"></td><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-right tex-tabular-border-top"><span class="tex-font-style-tt">! 3 2 1 4 2 2</span></td><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-top">A unique answer is found, which is $a = [3, 2, 1, 4, 2, 2]$.</td></tr></tbody></table> </center><p>From steps $10$ and $11$, we can deduce that the the <span class="tex-font-style-bf">multiset</span> $\left\{a_3, a_5, a_6\right\}$ must be $\left\{2, 2, 1\right\}$.</p><p>From steps $8$ and $9$, the <span class="tex-font-style-bf">multiset</span> $\left\{a_1, a_5, a_6\right\}$ must be either $\left\{4, 4, 1\right\}$ or $\left\{3, 2, 2\right\}$.</p><p>As $\left\{a_3, a_5, a_6\right\}$ and $\left\{a_1, a_5, a_6\right\}$ share $a_5$ and $a_6$, we conclude that $a_5 = a_6 = 2$, as well as $a_1 = 3$, $a_3 = 1$.</p><p>From steps $6$ and $7$, we know that $a_5 = a_6 = 2$, and $a_4$, $a_5$ and $a_6$ cannot form a non-degenerate triangle, hence $a_4 = 4$.</p><p>With all the known information, only $a_2 = 2$ satisfies the queries made in steps $2$, $3$, $4$, $5$, $12$ and $13$.</p><p>In the third example, one array that satisfies the queries is $[1, 1, 1, 1, 3, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1]$.</p>
