## Description

<div><p>The rebels have been crushed in the most recent battle with the imperial forces, but there is a ray of new hope.</p><p>Meanwhile, on one of the conquered planets, Luke was getting ready for an illegal street race (which should come as no surprise, given his family history). Luke arrived at the finish line with 88 miles per hour on his speedometer. After getting out of the car, he was greeted by a new reality. It turns out that the battle has not happened yet and will start in exactly $k$ hours.</p><p>The rebels have placed a single battleship on each of the $n$ planets. $m$ unidirectional wormholes connect the planets. Traversing each wormhole takes exactly one hour. Generals of the Imperium have planned the battle precisely, but their troops cannot dynamically adapt to changing circumstances. Because of this, it is enough for the rebels to move some ships around before the battle to confuse the enemy, secure victory and change the galaxy's fate.</p><p>Owing to numerous strategical considerations, which we now omit, the rebels would like to choose two ships that will switch places so that both of them will be on the move for the whole time (exactly $k$ hours). In other words, rebels look for two planets, $x$ and $y$, such that paths of length $k$ exist from $x$ to $y$ and from $y$ to $x$.</p><p>Because of the limited fuel supply, choosing one ship would also be acceptable. This ship should fly through the wormholes for $k$ hours and then return to its initial planet.</p><p>How many ways are there to choose the ships for completing the mission? </p></div><div class="input-specification"><p>In the first line of input, there are three integer numbers $n$, $m$, and $k$ ($1 \leq n \leq 10^5$, $0 \leq m \leq 2 \cdot 10^5$, $n^3 \leq k \leq 10^{18}$) denoting respectively the number of planets, wormholes and hours left until the battle starts.</p><p>The following $m$ lines contain two integers each, $x$ and $y$ ($1 \leq x, y \leq n$, $x \ne y$), meaning that there is a wormhole from planet $x$ to planet $y$. It is guaranteed that there are no two identical wormholes, i.&nbsp;e. for every two wormholes, either $x_1 \neq x_2$ or $y_1 \neq y_2$.</p></div><div class="output-specification"><p>In the first and only line, your program should output the number of possible ways of choosing a pair or a single warship for the mission.</p></div>

## Input

<p>In the first line of input, there are three integer numbers $n$, $m$, and $k$ ($1 \leq n \leq 10^5$, $0 \leq m \leq 2 \cdot 10^5$, $n^3 \leq k \leq 10^{18}$) denoting respectively the number of planets, wormholes and hours left until the battle starts.</p><p>The following $m$ lines contain two integers each, $x$ and $y$ ($1 \leq x, y \leq n$, $x \ne y$), meaning that there is a wormhole from planet $x$ to planet $y$. It is guaranteed that there are no two identical wormholes, i.&nbsp;e. for every two wormholes, either $x_1 \neq x_2$ or $y_1 \neq y_2$.</p>

## Output

<p>In the first and only line, your program should output the number of possible ways of choosing a pair or a single warship for the mission.</p>





```input1
7 8 346
1 2
1 3
2 4
3 4
4 5
5 1
6 7
7 6
```




```input2
5 6 128
1 2
1 3
2 4
3 4
4 5
5 1
```




```input3
3 3 30
1 2
2 3
3 2
```




```output1
5
```




```output2
6
```




```output3
2
```



## Note

<p>In the first sample test, one can choose pairs of ships from the following planets: $2$ and $5$, $3$ and $5$, $1$ and $4$. Individual ships from planets $6$ and $7$ could also be chosen.</p><p>In the second sample test, one can choose a pair of ships from the following planets: $2$ and $3$. Individual ships from planets $1$, $2$, $3$, $4$, and $5$ could also be chosen.</p><p>In the third sample test, there are no pairs of ships we can choose. Individual ships from planets $2$ and $3$ could also be chosen.</p>
