## Description

<div><p>While James is gone on business, Vesper takes her time and explores what the legendary Casino Royale has to offer to people who are fond of competitive programming.</p><p>Her attention was grabbed by the very new "Pull Your Luck" roulette which functions in a pretty peculiar way. The roulette's wheel consists of $n$ sectors number from $0$ to $n - 1$. There is no ball and the winning sector is determined by a static arrow pointing to one of the sectors. Sectors' indexes go in the natural order and the wheel always spins in the direction of indexes increment. That means that sector $i + 1$ goes right after sector $i$ for all $i$ from $0$ to $n - 2$, and sector $0$ goes right after sector $n - 1$.</p><p>After a bet is made, the player is allowed to pull the triggering handle herself and cause the wheel to spin. If the player's initial pull is made with the force equal to positive integer $f$, the wheel will spin for $f$ seconds. During the first second it will advance $f$ sectors, the next second it will advance $f - 1$ sectors, then $f - 2$ sectors, and so on until it comes to a complete stop. After the wheel comes to a complete stop, the sector which the arrow is pointing to is the winning one.</p><p>The roulette's arrow currently points at sector $x$. Vesper knows that she can pull the handle with any integer force from $1$ to $p$ inclusive. Note that it is not allowed to pull the handle with force $0$, i.&nbsp;e. not pull it all. The biggest prize is awarded if the winning sector is $0$. Now Vesper wonders if she can make sector $0$ win by pulling the triggering handle exactly once?</p></div><div class="input-specification"><p>The first line of the input contains a single integer $t$ ($1 \leq t \leq 10^4$)&nbsp;— the number of test cases. Then follow $t$ lines containing one test description each.</p><p>Each test description consists of three integers $n$, $x$ and $p$ ($3 \leq n \leq 10^5$, $0 \leq x &lt; n$, $1 \leq p \leq 10^9$). They are the number of sectors on the wheel, the current sector the arrow points at, and the maximum force that Vesper can pull the handle with, respectively.</p><p>It is guaranteed that the sum of $n$ over all test cases <span class="tex-font-style-bf">doesn't exceed $2 \cdot 10^5$</span>.</p></div><div class="output-specification"><p>Print $t$ lines, the $i$-th line should contain the answer for the $i$-th test case. If it is possible to pull the handle with the integer force from $1$ to $p$ in order to make sector $0$ win, print "<span class="tex-font-style-tt">Yes</span>". Otherwise, print "<span class="tex-font-style-tt">No</span>".</p><p>You can output the answer in any case (upper or lower). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as positive responses.</p></div>

## Input

<p>The first line of the input contains a single integer $t$ ($1 \leq t \leq 10^4$)&nbsp;— the number of test cases. Then follow $t$ lines containing one test description each.</p><p>Each test description consists of three integers $n$, $x$ and $p$ ($3 \leq n \leq 10^5$, $0 \leq x &lt; n$, $1 \leq p \leq 10^9$). They are the number of sectors on the wheel, the current sector the arrow points at, and the maximum force that Vesper can pull the handle with, respectively.</p><p>It is guaranteed that the sum of $n$ over all test cases <span class="tex-font-style-bf">doesn't exceed $2 \cdot 10^5$</span>.</p>

## Output

<p>Print $t$ lines, the $i$-th line should contain the answer for the $i$-th test case. If it is possible to pull the handle with the integer force from $1$ to $p$ in order to make sector $0$ win, print "<span class="tex-font-style-tt">Yes</span>". Otherwise, print "<span class="tex-font-style-tt">No</span>".</p><p>You can output the answer in any case (upper or lower). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as positive responses.</p>





```input1|2,4,6,8
7
5 2 1
5 2 2
10 0 100
11 7 100
3 1 1000
31 0 10
100 49 7
```




```output1
No
Yes
Yes
Yes
No
No
No
```



## Note

<p>In the first example, the only possible way to pull the handle is with force $1$. That is not enough to make the arrow point at sector $0$, at least force $2$ is required to do so.</p><p>In the second example, Vesper can pull the handle with the force $2$ so the wheel will spin $2 + 1 = 3$ sectors ahead and the arrow will point at sector $0$.</p><p>In the third example, Vesper can pull the handle with the force $4$ so the wheel will spin $4 + 3 + 2 + 1 = 10$ sectors and will point at sector $0$ again.</p><p>In the fourth example, Vesper can pull the handle with the force $5$ so the wheel will spin $5 + 4 + 3 + 2 + 1 = 15$ sectors. That will make the wheel make one full turn plus $4$ more sectors.</p><p>In the fifth example, whatever force Vesper chooses to pull the handle with, she can only make sectors $1$ and $2$ win.</p>
