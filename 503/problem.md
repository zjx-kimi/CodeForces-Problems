## Description

<div><p>You are given two positive integers, $a$ and $b$ ($a &lt; b$).</p><p>For some positive integer $n$, two players will play a game starting with a pile of $n$ stones. They take turns removing exactly $a$ or exactly $b$ stones from the pile. The player who is unable to make a move loses.</p><p>Find a positive integer $n$ such that the second player to move in this game has a winning strategy. This means that no matter what moves the first player makes, the second player can carefully choose their moves (possibly depending on the first player's moves) to ensure they win.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 100$). The description of the test cases follows.</p><p>The only line of each test case contains two integers, $a$ and $b$ ($1 \le a &lt; b \le 100$).</p></div><div class="output-specification"><p>For each test case, output any positive integer $n$ ($1 \le n \le 10^6$) such that the second player to move wins.</p><p>It can be proven that such an $n$ always exists under the constraints of the problem.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 100$). The description of the test cases follows.</p><p>The only line of each test case contains two integers, $a$ and $b$ ($1 \le a &lt; b \le 100$).</p>

## Output

<p>For each test case, output any positive integer $n$ ($1 \le n \le 10^6$) such that the second player to move wins.</p><p>It can be proven that such an $n$ always exists under the constraints of the problem.</p>





```input1|2,4
3
1 4
1 5
9 26
```




```output1
2
6
3
```



## Note

<p>In the first test case, when $n = 2$, the first player must remove $a = 1$ stone. Then, the second player can respond by removing $a = 1$ stone. The first player can no longer make a move, so the second player wins.</p><p>In the second test case, when $n = 6$, the first player has two options: </p><ul> <li> If they remove $b = 5$ stones, then the second player can respond by removing $a = 1$ stone. The first player can no longer make a move, so the second player wins. </li><li> If they remove $a = 1$ stone, then the second player can respond by removing $a = 1$ stone. Afterwards, the players can only alternate removing exactly $a = 1$ stone. The second player will take the last stone and win. </li></ul> Since the second player has a winning strategy no matter what the first player does, this is an acceptable output.<p>In the third test case, the first player cannot make any moves when $n = 3$, so the second player immediately wins.</p>
