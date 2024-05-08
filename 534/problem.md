## Description

<div><p><span class="tex-font-style-bf">This is an interactive problem.</span></p><p>Consider the following game for two players:</p><ul> <li> Initially, an array of integers $a_1, a_2, \ldots, a_n$ of length $n$ is written on blackboard.</li><li> Game consists of <span class="tex-font-style-it">rounds</span>. On each round, the following happens: <ul> <li> The first player selects any $i$ such that $a_i \gt 0$. If there is no such $i$, the first player loses the game (the second player wins) and game ends. </li><li> The second player selects any $j \neq i$ such that $a_j \gt 0$. If there is no such $j$, the second player loses the game (the first player wins) and game ends. </li><li> Let $d = \min(a_i, a_j)$. The values of $a_i$ and $a_j$ are simultaneously decreased by $d$ and the next round starts. </li></ul> </li></ul><p>It can be shown that game always ends after the finite number of rounds.</p><p>You have to select which player you will play for (first or second) and win the game.</p></div><div class="input-specification"><p>The first line contains a single integer $n$ ($1 \le n \le 300$)&nbsp;— the length of array $a$.</p><p>The second line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le 300$)&nbsp;— array $a$.</p></div><div><h2>Interaction</h2><p>Interaction begins after reading $n$ and array $a$.</p><p>You should start interaction by printing a single line, containing either "<span class="tex-font-style-tt">First</span>" or "<span class="tex-font-style-tt">Second</span>", representing the player you select.</p><p>On each round, the following happens: </p><ul> <li> If you are playing as the first player, you should print a single integer $i$ ($1 \le i \le n$) on a separate line. After that, you should read a single integer $j$ ($-1 \le j \le n$) written on a separate line.<p>If $j = -1$, then you made an incorrect move. In this case your program should terminate immediately.</p><p>If $j = 0$, then the second player can't make a correct move and you win the game. In this case your program should also terminate immediately.</p><p>Otherwise $j$ is equal to the index chosen by the second player, and you should proceed to the next round.</p></li><li> If you are playing as the second player, you should read a single integer $i$ ($-1 \le i \le n$) written on a separate line.<p>If $i = -1$, then you made an incorrect move on the previous round (this cannot happen on the first round). In that case your program should terminate immediately.</p><p>If $i = 0$, then the first player can't make a correct move and you win the game. In this case your program should also terminate immediately.</p><p>Otherwise $i$ is equal to the index chosen by first player. In this case you should write single integer $j$ ($1 \le j \le n$) on a separate line and proceed to the next round. </p></li></ul><p>After printing $i$ or $j$, do not forget to output the end of line and flush the output. Otherwise, you will get <span class="tex-font-style-tt">Idleness limit exceeded</span>. To do this, use:</p><ul> <li> <span class="tex-font-style-tt">fflush(stdout)</span> or <span class="tex-font-style-tt">cout.flush()</span> in C++; </li><li> <span class="tex-font-style-tt">System.out.flush()</span> in Java; </li><li> <span class="tex-font-style-tt">flush(output)</span> in Pascal; </li><li> <span class="tex-font-style-tt">stdout.flush()</span> in Python; </li><li> see the documentation for other languages. </li></ul><p><span class="tex-font-style-bf">Hacks</span></p><p>Hacks are disabled in this problem.</p></div>

## Input

<p>The first line contains a single integer $n$ ($1 \le n \le 300$)&nbsp;— the length of array $a$.</p><p>The second line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le 300$)&nbsp;— array $a$.</p>





```input1
4
10 4 6 3


3

1

0
```




```input2
6
4 5 5 11 3 2

2

5

4

6

1

0
```




```output1
First
1

2

4
```




```output2
Second 

4

4

3

1

3
```



## Note

<p>In the first example $n = 4$ and array $a$ is $[\, 10, 4, 6, 3 \,]$. The game goes as follows: </p><ul> <li> After reading array $a$ contestant's program chooses to play as the first player and prints "<span class="tex-font-style-tt">First</span>".</li><li> First round: the first player chooses $i = 1$, the second player chooses $j = 3$. $d = \min(a_1, a_3) = \min(10, 6) = 6$ is calculated. Elements $a_1$ and $a_3$ are decreased by $6$. Array $a$ becomes equal to $[\, 4, 4, 0, 3 \,]$.</li><li> Second round: the first player chooses $i = 2$, the second player chooses $j = 1$. $d = \min(a_2, a_1) = \min(4, 4) = 4$ is calculated. Elements $a_2$ and $a_1$ are decreased by $4$. Array $a$ becomes equal to $[\, 0, 0, 0, 3 \,]$.</li><li> Third round: the first player chooses $i = 4$. There is no $j \neq 4$ such that $a_j &gt; 0$, so the second player can't make a correct move and the first player wins. Jury's program prints $j = 0$. After reading it, contestant's program terminates. </li></ul><p>In the second example $n = 6$ and array $a$ is $[\, 4, 5, 5, 11, 3, 2 \,]$. The game goes as follows:</p><ul> <li> Contestant's program chooses to play as the second player and prints "<span class="tex-font-style-tt">Second</span>". </li><li> First round: $i = 2$, $j = 4$, $a = [\, 4, 0, 5, 6, 3, 2 \,]$. </li><li> Second round: $i = 5$, $j = 4$, $a = [\, 4, 0, 5, 3, 0, 2 \,]$. </li><li> Third round: $i = 4$, $j = 3$, $a = [\, 4, 0, 2, 0, 0, 2 \,]$. </li><li> Fourth round: $i = 6$, $j = 1$, $a = [\, 2, 0, 2, 0, 0, 0 \,]$. </li><li> Fifth round: $i = 1$, $j = 3$, $a = [\, 0, 0, 0, 0, 0, 0 \,]$. </li><li> Sixth round: the first player can't make a correct move and the second player wins. Jury's program prints $i = 0$. After reading it, contestant's program terminates. </li></ul><p>Note that the example interaction contains extra empty lines so that it's easier to read. The real interaction doesn't contain any empty lines and you shouldn't print any extra empty lines as well.</p>
