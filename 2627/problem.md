## Description

<div><p>Alice and Bob play ping-pong with simplified rules.</p><p>During the game, the player serving the ball commences a play. The server strikes the ball then the receiver makes a return by hitting the ball back. Thereafter, the server and receiver must alternately make a return until one of them doesn't make a return.</p><p>The one who doesn't make a return loses this play. The winner of the play commences the next play. Alice starts the first play.</p><p>Alice has $x$ stamina and Bob has $y$. To hit the ball (while serving or returning) each player spends $1$ stamina, so if they don't have any stamina, they can't return the ball (and lose the play) or can't serve the ball (in this case, the other player serves the ball instead). If both players run out of stamina, the game is over.</p><p>Sometimes, it's strategically optimal not to return the ball, lose the current play, but save the stamina. On the contrary, when the server commences a play, they have to hit the ball, if they have some stamina left.</p><p>Both Alice and Bob play optimally and want to, firstly, maximize their number of wins and, secondly, minimize the number of wins of their opponent.</p><p>Calculate the resulting number of Alice's and Bob's wins.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The first and only line of each test case contains two integers $x$ and $y$ ($1 \le x, y \le 10^6$)&nbsp;— Alice's and Bob's initial stamina.</p></div><div class="output-specification"><p>For each test case, print two integers&nbsp;— the resulting number of Alice's and Bob's wins, if both of them play optimally.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The first and only line of each test case contains two integers $x$ and $y$ ($1 \le x, y \le 10^6$)&nbsp;— Alice's and Bob's initial stamina.</p>

## Output

<p>For each test case, print two integers&nbsp;— the resulting number of Alice's and Bob's wins, if both of them play optimally.</p>





```input1
3
1 1
2 1
1 7
```




```output1
0 1
1 1
0 7
```



## Note

<p>In the first test case, Alice serves the ball and spends $1$ stamina. Then Bob returns the ball and also spends $1$ stamina. Alice can't return the ball since she has no stamina left and loses the play. Both of them ran out of stamina, so the game is over with $0$ Alice's wins and $1$ Bob's wins.</p><p>In the second test case, Alice serves the ball and spends $1$ stamina. Bob decides not to return the ball&nbsp;— he loses the play but saves stamina. Alice, as the winner of the last play, serves the ball in the next play and spends $1$ more stamina. This time, Bob returns the ball and spends $1$ stamina. Alice doesn't have any stamina left, so she can't return the ball and loses the play. Both of them ran out of stamina, so the game is over with $1$ Alice's and $1$ Bob's win.</p><p>In the third test case, Alice serves the ball and spends $1$ stamina. Bob returns the ball and spends $1$ stamina. Alice ran out of stamina, so she can't return the ball and loses the play. Bob, as a winner, serves the ball in the next $6$ plays. Each time Alice can't return the ball and loses each play. The game is over with $0$ Alice's and $7$ Bob's wins.</p>
