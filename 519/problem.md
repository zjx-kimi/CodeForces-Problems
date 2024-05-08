## Description

<div><div class="epigraph"><div class="epigraph-text"><span class="tex-font-style-it">Tsondu always runs first! ! !</span></div></div><p>Tsondu and Tenzing are playing a card game. Tsondu has $n$ monsters with ability values $a_1, a_2, \ldots, a_n$ while Tenzing has $m$ monsters with ability values $b_1, b_2, \ldots, b_m$.</p><p>Tsondu and Tenzing take turns making moves, with Tsondu going first. In each move, the current player chooses two monsters: one on their side and one on the other side. Then, these monsters will fight each other. Suppose the ability values for the chosen monsters are $x$ and $y$ respectively, then the ability values of the monsters will become $x-y$ and $y-x$ respectively. If the ability value of any monster is smaller than or equal to $0$, the monster dies.</p><p>The game ends when at least one player has no monsters left alive. The winner is the player with at least one monster left alive. If both players have no monsters left alive, the game ends in a draw.</p><p>Find the result of the game when both players play optimally.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line of input contains a single integer $t$ ($1 \le t \le 2 \cdot 10^3$)&nbsp;— the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains two integers $n$ and $m$ ($1 \leq n,m \leq 50$)&nbsp;— the number of monsters Tsondu and Tenzing have respectively.</p><p>The second line of each test case contains $n$ integers $a_1,a_2,\ldots,a_n$ $(1 \leq a_i \leq 10^9$)&nbsp;— the ability values of Tsondu's monsters. </p><p>The third line of each test case contains $m$ integers $b_1,b_2,\ldots,b_m$ $(1 \leq b_i \leq 10^9$)&nbsp;— the ability values of Tenzing's monsters. </p></div><div class="output-specification"><p>For each test case, output "<span class="tex-font-style-tt">Tsondu</span>" if Tsondu wins, "<span class="tex-font-style-tt">Tenzing</span>" if Tenzing wins, and "<span class="tex-font-style-tt">Draw</span>" if the game ends in a draw. (Output without quotes.)</p><p>Note that the output is case-sensitive. For example, if the answer is "<span class="tex-font-style-tt">Tsondu</span>", the outputs "<span class="tex-font-style-tt">tsondu</span>", "<span class="tex-font-style-tt">TSONDU</span>", and "<span class="tex-font-style-tt">tSonDu</span>" will all be recognized as <span class="tex-font-style-bf">incorrect</span> outputs.</p></div>

## Input

<p>Each test contains multiple test cases. The first line of input contains a single integer $t$ ($1 \le t \le 2 \cdot 10^3$)&nbsp;— the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains two integers $n$ and $m$ ($1 \leq n,m \leq 50$)&nbsp;— the number of monsters Tsondu and Tenzing have respectively.</p><p>The second line of each test case contains $n$ integers $a_1,a_2,\ldots,a_n$ $(1 \leq a_i \leq 10^9$)&nbsp;— the ability values of Tsondu's monsters. </p><p>The third line of each test case contains $m$ integers $b_1,b_2,\ldots,b_m$ $(1 \leq b_i \leq 10^9$)&nbsp;— the ability values of Tenzing's monsters. </p>

## Output

<p>For each test case, output "<span class="tex-font-style-tt">Tsondu</span>" if Tsondu wins, "<span class="tex-font-style-tt">Tenzing</span>" if Tenzing wins, and "<span class="tex-font-style-tt">Draw</span>" if the game ends in a draw. (Output without quotes.)</p><p>Note that the output is case-sensitive. For example, if the answer is "<span class="tex-font-style-tt">Tsondu</span>", the outputs "<span class="tex-font-style-tt">tsondu</span>", "<span class="tex-font-style-tt">TSONDU</span>", and "<span class="tex-font-style-tt">tSonDu</span>" will all be recognized as <span class="tex-font-style-bf">incorrect</span> outputs.</p>





```input1|2,3,4,8,9,10,14,15,16
6
1 3
9
1 2 3
2 3
1 2
1 1 1
3 2
1 2 3
1 1
3 3
1 1 1
2 2 2
10 10
1 2 3 3 2 2 1 1 2 2
3 3 3 3 2 1 1 1 1 1
10 10
1 2 3 4 5 6 7 8 9 10
6 7 8 9 10 11 1 1 1 1
```




```output1
Tsondu
Draw
Tsondu
Tenzing
Draw
Draw
```



## Note

<p>Consider the first test case. It can be shown that Tsondu has a winning strategy. The following is a possible way that Tsondu can win (note that the players may not be playing optimally in this example):</p><ul> <li> In the first move, Tsondu chooses a monster with ability value $9$ on his side to fight against a monster with ability value $1$ on Tenzing's side, the ability value of both monsters become $8$ and $-8$ respectively. The monster with ability value $-8$ on Tenzing's side dies. </li><li> In the second move, Tenzing chooses a monster with ability value $2$ on his side to fight against a monster with ability value $8$ on Tsondu's side, the ability value of both monsters become $-6$ and $6$ respectively. The monster with ability value $-6$ on Tenzing's side dies. </li><li> In the third move, Tsondu chooses a monster with ability value $6$ on his side to fight against a monster with ability value $3$ onTenzing's side, the ability value of both monsters become $3$ and $-3$ respectively. The monster with ability value $-3$ on Tenzing's side dies. </li><li> Now, Tenzing has no monsters left alive. Since Tsondu still has monsters left alive, Tsondu wins. </li></ul>
