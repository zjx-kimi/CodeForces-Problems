## Description

<div><p>Alice and Bob play a game. They have a blackboard; initially, there are $n$ integers written on it, and each integer is equal to $1$.</p><p>Alice and Bob take turns; Alice goes first. On their turn, the player has to choose several (<span class="tex-font-style-bf">at least two</span>) <span class="tex-font-style-bf">equal</span> integers on the board, wipe them and write a new integer which is equal to their sum.</p><p>For example, if the board currently contains integers $\{1, 1, 2, 2, 2, 3\}$, then the following moves are possible:</p><ul> <li> choose two integers equal to $1$, wipe them and write an integer $2$, then the board becomes $\{2, 2, 2, 2, 3\}$; </li><li> choose two integers equal to $2$, wipe them and write an integer $4$, then the board becomes $\{1, 1, 2, 3, 4\}$; </li><li> choose three integers equal to $2$, wipe them and write an integer $6$, then the board becomes $\{1, 1, 3, 6\}$. </li></ul><p>If a player cannot make a move (all integers on the board are different), that player <span class="tex-font-style-bf">wins the game</span>.</p><p>Determine who wins if both players play optimally.</p></div><div class="input-specification"><p>The first line contains one integer $t$ ($1 \le t \le 99$) — the number of test cases.</p><p>Each test case consists of one line containing one integer $n$ ($2 \le n \le 100$) — the number of integers equal to $1$ on the board.</p></div><div class="output-specification"><p>For each test case, print <span class="tex-font-style-tt">Alice</span> if Alice wins when both players play optimally. Otherwise, print <span class="tex-font-style-tt">Bob</span>.</p></div>

## Input

<p>The first line contains one integer $t$ ($1 \le t \le 99$) — the number of test cases.</p><p>Each test case consists of one line containing one integer $n$ ($2 \le n \le 100$) — the number of integers equal to $1$ on the board.</p>

## Output

<p>For each test case, print <span class="tex-font-style-tt">Alice</span> if Alice wins when both players play optimally. Otherwise, print <span class="tex-font-style-tt">Bob</span>.</p>





```input1|2
2
3
6
```




```output1
Bob
Alice
```



## Note

<p>In the first test case, $n = 3$, so the board initially contains integers $\{1, 1, 1\}$. We can show that Bob can always win as follows: there are two possible first moves for Alice.</p><ul> <li> if Alice chooses two integers equal to $1$, wipes them and writes $2$, the board becomes $\{1, 2\}$. Bob cannot make a move, so he wins; </li><li> if Alice chooses three integers equal to $1$, wipes them and writes $3$, the board becomes $\{3\}$. Bob cannot make a move, so he wins. </li></ul><p>In the second test case, $n = 6$, so the board initially contains integers $\{1, 1, 1, 1, 1, 1\}$. Alice can win by, for example, choosing two integers equal to $1$, wiping them and writing $2$ on the first turn. Then the board becomes $\{1, 1, 1, 1, 2\}$, and there are three possible responses for Bob:</p><ul> <li> if Bob chooses four integers equal to $1$, wipes them and writes $4$, the board becomes $\{2,4\}$. Alice cannot make a move, so she wins; </li><li> if Bob chooses three integers equal to $1$, wipes them and writes $3$, the board becomes $\{1,2,3\}$. Alice cannot make a move, so she wins; </li><li> if Bob chooses two integers equal to $1$, wipes them and writes $2$, the board becomes $\{1, 1, 2, 2\}$. Alice can continue by, for example, choosing two integers equal to $2$, wiping them and writing $4$. Then the board becomes $\{1,1,4\}$. The only possible response for Bob is to choose two integers equal to $1$ and write $2$ instead of them; then the board becomes $\{2,4\}$, Alice cannot make a move, so she wins. </li></ul>
