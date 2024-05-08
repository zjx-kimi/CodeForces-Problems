## Description

<div><p>There are $n$ logs, the $i$-th log has a length of $a_i$ meters. Since chopping logs is tiring work, errorgorn and maomao90 have decided to play a game.</p><p>errorgorn and maomao90 will take turns chopping the logs with <span class="tex-font-style-bf">errorgorn chopping first</span>. On his turn, the player will pick a log and chop it into $2$ pieces. If the length of the chosen log is $x$, and the lengths of the resulting pieces are $y$ and $z$, then $y$ and $z$ have to be <span class="tex-font-style-bf">positive integers</span>, and $x=y+z$ must hold. For example, you can chop a log of length $3$ into logs of lengths $2$ and $1$, but not into logs of lengths $3$ and $0$, $2$ and $2$, or $1.5$ and $1.5$.</p><p>The player who is unable to make a chop will be the loser. Assuming that both errorgorn and maomao90 play optimally, who will be the winner?</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 100$) &nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \leq n \leq 50$) &nbsp;— the number of logs.</p><p>The second line of each test case contains $n$ integers $a_1,a_2, \ldots, a_n$ ($1 \leq a_i \leq 50$) &nbsp;— the lengths of the logs.</p><p>Note that there is no bound on the sum of $n$ over all test cases.</p></div><div class="output-specification"><p>For each test case, print "<span class="tex-font-style-tt">errorgorn</span>" if errorgorn wins or "<span class="tex-font-style-tt">maomao90</span>" if maomao90 wins. (Output without quotes).</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 100$) &nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \leq n \leq 50$) &nbsp;— the number of logs.</p><p>The second line of each test case contains $n$ integers $a_1,a_2, \ldots, a_n$ ($1 \leq a_i \leq 50$) &nbsp;— the lengths of the logs.</p><p>Note that there is no bound on the sum of $n$ over all test cases.</p>

## Output

<p>For each test case, print "<span class="tex-font-style-tt">errorgorn</span>" if errorgorn wins or "<span class="tex-font-style-tt">maomao90</span>" if maomao90 wins. (Output without quotes).</p>





```input1|2,3
2
4
2 4 2 1
1
1
```




```output1
errorgorn
maomao90
```



## Note

<p>In the first test case, errorgorn will be the winner. An optimal move is to chop the log of length $4$ into $2$ logs of length $2$. After this there will only be $4$ logs of length $2$ and $1$ log of length $1$.</p><p>After this, the only move any player can do is to chop any log of length $2$ into $2$ logs of length $1$. After $4$ moves, it will be maomao90's turn and he will not be able to make a move. Therefore errorgorn will be the winner.</p><p>In the second test case, errorgorn will not be able to make a move on his first turn and will immediately lose, making maomao90 the winner.</p>
