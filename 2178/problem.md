## Description

<div><p>After defeating a Blacklist Rival, you get a chance to draw $1$ reward slip out of $x$ hidden valid slips. Initially, $x=3$ and these hidden valid slips are Cash Slip, Impound Strike Release Marker and Pink Slip of Rival's Car. Initially, the probability of drawing these in a random guess are $c$, $m$, and $p$, respectively. There is also a volatility factor $v$. You can play any number of Rival Races as long as you don't draw a Pink Slip. Assume that you win each race and get a chance to draw a reward slip. In each draw, you draw one of the $x$ valid items with their respective probabilities. Suppose you draw a particular item and its probability of drawing before the draw was $a$. Then,</p><ul> <li> If the item was a Pink Slip, the quest is over, and you will not play any more races. </li><li> Otherwise, <ol> <li> If $a\leq v$, the probability of the item drawn becomes $0$ and the item is no longer a valid item for all the further draws, reducing $x$ by $1$. Moreover, the reduced probability $a$ is distributed equally among the other remaining valid items. </li><li> If $a &gt; v$, the probability of the item drawn reduces by $v$ and the reduced probability is distributed equally among the other valid items. </li></ol> </li></ul><p>For example,</p><ul> <li> If $(c,m,p)=(0.2,0.1,0.7)$ and $v=0.1$, after drawing Cash, the new probabilities will be $(0.1,0.15,0.75)$. </li><li> If $(c,m,p)=(0.1,0.2,0.7)$ and $v=0.2$, after drawing Cash, the new probabilities will be $(Invalid,0.25,0.75)$. </li><li> If $(c,m,p)=(0.2,Invalid,0.8)$ and $v=0.1$, after drawing Cash, the new probabilities will be $(0.1,Invalid,0.9)$. </li><li> If $(c,m,p)=(0.1,Invalid,0.9)$ and $v=0.2$, after drawing Cash, the new probabilities will be $(Invalid,Invalid,1.0)$. </li></ul><p>You need the cars of Rivals. So, you need to find the expected number of races that you must play in order to draw a pink slip.</p></div><div class="input-specification"><p>The first line of input contains a single integer $t$ ($1\leq t\leq 10$) &nbsp;— the number of test cases.</p><p>The first and the only line of each test case contains four real numbers $c$, $m$, $p$ and $v$ ($0 &lt; c,m,p &lt; 1$, $c+m+p=1$, $0.1\leq v\leq 0.9$).</p><p>Additionally, it is guaranteed that each of $c$, $m$, $p$ and $v$ have at most $4$ decimal places.</p></div><div class="output-specification"><p>For each test case, output a single line containing a single real number&nbsp;— the expected number of races that you must play in order to draw a Pink Slip.</p><p>Your answer is considered correct if its absolute or relative error does not exceed $10^{-6}$.</p><p>Formally, let your answer be $a$, and the jury's answer be $b$. Your answer is accepted if and only if $\frac{|a - b|}{\max{(1, |b|)}} \le 10^{-6}$.</p></div>

## Input

<p>The first line of input contains a single integer $t$ ($1\leq t\leq 10$) &nbsp;— the number of test cases.</p><p>The first and the only line of each test case contains four real numbers $c$, $m$, $p$ and $v$ ($0 &lt; c,m,p &lt; 1$, $c+m+p=1$, $0.1\leq v\leq 0.9$).</p><p>Additionally, it is guaranteed that each of $c$, $m$, $p$ and $v$ have at most $4$ decimal places.</p>

## Output

<p>For each test case, output a single line containing a single real number&nbsp;— the expected number of races that you must play in order to draw a Pink Slip.</p><p>Your answer is considered correct if its absolute or relative error does not exceed $10^{-6}$.</p><p>Formally, let your answer be $a$, and the jury's answer be $b$. Your answer is accepted if and only if $\frac{|a - b|}{\max{(1, |b|)}} \le 10^{-6}$.</p>





```input1
4
0.2 0.2 0.6 0.2
0.4 0.2 0.4 0.8
0.4998 0.4998 0.0004 0.1666
0.3125 0.6561 0.0314 0.2048
```




```output1
1.532000000000
1.860000000000
5.005050776521
4.260163673896
```



## Note

<p>For the first test case, the possible drawing sequences are: </p><ul> <li> <span class="tex-font-style-tt">P</span> with a probability of $0.6$; </li><li> <span class="tex-font-style-tt">CP</span> with a probability of $0.2\cdot 0.7 = 0.14$; </li><li> <span class="tex-font-style-tt">CMP</span> with a probability of $0.2\cdot 0.3\cdot 0.9 = 0.054$; </li><li> <span class="tex-font-style-tt">CMMP</span> with a probability of $0.2\cdot 0.3\cdot 0.1\cdot 1 = 0.006$; </li><li> <span class="tex-font-style-tt">MP</span> with a probability of $0.2\cdot 0.7 = 0.14$; </li><li> <span class="tex-font-style-tt">MCP</span> with a probability of $0.2\cdot 0.3\cdot 0.9 = 0.054$; </li><li> <span class="tex-font-style-tt">MCCP</span> with a probability of $0.2\cdot 0.3\cdot 0.1\cdot 1 = 0.006$. </li></ul> So, the expected number of races is equal to $1\cdot 0.6 + 2\cdot 0.14 + 3\cdot 0.054 + 4\cdot 0.006 + 2\cdot 0.14 + 3\cdot 0.054 + 4\cdot 0.006 = 1.532$.<p>For the second test case, the possible drawing sequences are: </p><ul> <li> <span class="tex-font-style-tt">P</span> with a probability of $0.4$; </li><li> <span class="tex-font-style-tt">CP</span> with a probability of $0.4\cdot 0.6 = 0.24$; </li><li> <span class="tex-font-style-tt">CMP</span> with a probability of $0.4\cdot 0.4\cdot 1 = 0.16$; </li><li> <span class="tex-font-style-tt">MP</span> with a probability of $0.2\cdot 0.5 = 0.1$; </li><li> <span class="tex-font-style-tt">MCP</span> with a probability of $0.2\cdot 0.5\cdot 1 = 0.1$. </li></ul><p>So, the expected number of races is equal to $1\cdot 0.4 + 2\cdot 0.24 + 3\cdot 0.16 + 2\cdot 0.1 + 3\cdot 0.1 = 1.86$.</p>
