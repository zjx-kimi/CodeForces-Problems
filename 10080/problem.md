## Description

<div><p>Rudolf and Bernard decided to play a game with their friends. $n$ people stand in a circle and start throwing a ball to each other. They are numbered from $1$ to $n$ in the clockwise order.</p><p>Let's call a transition a movement of the ball from one player to his neighbor. The transition can be made clockwise or counterclockwise.</p><p>Let's call the clockwise (counterclockwise) distance from player $y_1$ to player $y_2$ the number of transitions clockwise (counterclockwise) that need to be made to move from player $y_1$ to player $y_2$. For example, if $n=7$ then the clockwise distance from $2$ to $5$ is $3$, and the counterclockwise distance from $2$ to $5$ is $4$.</p><p>Initially, the ball is with the player number $x$ (players are numbered clockwise). On the $i$-th move the person with the ball throws it at a distance of $r_i$ ($1 \le r_i \le n - 1$) clockwise or counterclockwise. For example, if there are $7$ players, and the $2$nd player, after receiving the ball, throws it a distance of $5$, then the ball will be caught by either the $7$th player (throwing clockwise) or the $4$th player (throwing counterclockwise). An illustration of this example is shown below.</p><center> <img class="tex-graphics" src="file://v31UXqfG.png" style="max-width: 100.0%;max-height: 100.0%;"> </center><p>The game was interrupted after $m$ throws due to unexpected rain. When the rain stopped, the guys gathered again to continue. However, no one could remember who had the ball. As it turned out, Bernard remembered the distances for each of the throws and the direction for <span class="tex-font-style-bf">some</span> of the throws (clockwise or counterclockwise).</p><p>Rudolf asks you to help him and based on the information from Bernard, calculate the numbers of the players who could have the ball after $m$ throws.</p></div><div class="input-specification"><p>The first line of the input contains a single integer $t$ ($1 \le t \le 10^4$) — the number of test cases. Then follow the descriptions of the test cases.</p><p>The first line of each test case contains three integers $n, m, x$ ($2 \le n \le 1000$, $1 \le m \le 1000$, $1 \le x \le n$) — the number of players, the number of throws made, and the number of the player who threw the ball first, respectively.</p><p>The next $m$ lines contain information about each throw in order. Each of them contains an integer $r_i$ ($1 \le r_i \le n - 1$) — the distance at which the $i$-th throw was made, and a symbol $c_i$, equal to '<span class="tex-font-style-tt">0</span>', '<span class="tex-font-style-tt">1</span>', or '<span class="tex-font-style-tt">?</span>':</p><ul> <li> if $c_i$='<span class="tex-font-style-tt">0</span>', then the $i$-th throw was made clockwise, </li><li> if $c_i$='<span class="tex-font-style-tt">1</span>', then the $i$-th throw was made counterclockwise, </li><li> if $c_i$='<span class="tex-font-style-tt">?</span>', then Bernard does not remember the direction and the $i$-th throw could have been made either clockwise or counterclockwise. </li></ul><p>It is guaranteed that the sum $n \cdot m$ ($n$ multiplied by $m$) over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output two lines.</p><p>In the first line, output the number of players $k$ ($1 \le k \le n$) who could have the ball at the end of the game.</p><p>In the next line, output $k$ numbers $b_i$ ($1 \le b_i \le n$) — the numbers of the players in increasing order. All numbers must be different.</p></div>

## Input

<p>The first line of the input contains a single integer $t$ ($1 \le t \le 10^4$) — the number of test cases. Then follow the descriptions of the test cases.</p><p>The first line of each test case contains three integers $n, m, x$ ($2 \le n \le 1000$, $1 \le m \le 1000$, $1 \le x \le n$) — the number of players, the number of throws made, and the number of the player who threw the ball first, respectively.</p><p>The next $m$ lines contain information about each throw in order. Each of them contains an integer $r_i$ ($1 \le r_i \le n - 1$) — the distance at which the $i$-th throw was made, and a symbol $c_i$, equal to '<span class="tex-font-style-tt">0</span>', '<span class="tex-font-style-tt">1</span>', or '<span class="tex-font-style-tt">?</span>':</p><ul> <li> if $c_i$='<span class="tex-font-style-tt">0</span>', then the $i$-th throw was made clockwise, </li><li> if $c_i$='<span class="tex-font-style-tt">1</span>', then the $i$-th throw was made counterclockwise, </li><li> if $c_i$='<span class="tex-font-style-tt">?</span>', then Bernard does not remember the direction and the $i$-th throw could have been made either clockwise or counterclockwise. </li></ul><p>It is guaranteed that the sum $n \cdot m$ ($n$ multiplied by $m$) over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output two lines.</p><p>In the first line, output the number of players $k$ ($1 \le k \le n$) who could have the ball at the end of the game.</p><p>In the next line, output $k$ numbers $b_i$ ($1 \le b_i \le n$) — the numbers of the players in increasing order. All numbers must be different.</p>





```input1|2,3,4,5,8,9,10,11,12,13,14,15,20,21
5
6 3 2
2 ?
2 ?
2 ?
12 1 2
3 1
10 7 4
2 ?
9 1
4 ?
7 0
2 0
8 1
5 ?
5 3 1
4 0
4 ?
1 ?
4 1 1
2 ?
```




```output1
3
2 4 6 
1
11 
4
3 5 7 9 
3
2 3 5 
1
3
```



## Note

<p>Below is an illustration of three throws for the first test case. The arrows denote possible throw directions. Players who could have the ball after the throw are highlighted in gray.</p><center> <img class="tex-graphics" src="file://rpn53g5T.png" style="max-width: 100.0%;max-height: 100.0%;"> <img class="tex-graphics" src="file://QN1HVzko.png" style="max-width: 100.0%;max-height: 100.0%;"> <img class="tex-graphics" src="file://28mXQqNF.png" style="max-width: 100.0%;max-height: 100.0%;"> </center>
