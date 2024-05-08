## Description

<div><p>In a certain video game, the player controls a hero characterized by a single integer value: <span class="tex-font-style-it">power</span>.</p><p>On the current level, the hero got into a system of $n$ caves numbered from $1$ to $n$, and $m$ tunnels between them. Each tunnel connects two distinct caves. Any two caves are connected with at most one tunnel. Any cave can be reached from any other cave by moving via tunnels.</p><p>The hero starts the level in cave $1$, and every other cave contains a monster.</p><p>The hero can move between caves via tunnels. If the hero leaves a cave and enters a tunnel, he must finish his movement and arrive at the opposite end of the tunnel.</p><p>The hero can use each tunnel to move in both directions. However, the hero <span class="tex-font-style-bf">can not</span> use the same tunnel <span class="tex-font-style-bf">twice in a row</span>. Formally, if the hero has just moved from cave $i$ to cave $j$ via a tunnel, he can not head back to cave $i$ immediately after, but he can head to any other cave connected to cave $j$ with a tunnel.</p><p>It is known that at least two tunnels come out of every cave, thus, the hero will never find himself in a dead end even considering the above requirement.</p><p>To pass the level, the hero must beat the monsters in all the caves. When the hero enters a cave for the first time, he will have to fight the monster in it. The hero can beat the monster in cave $i$ if and only if the hero's power is strictly greater than $a_i$. In case of beating the monster, the hero's power increases by $b_i$. If the hero can't beat the monster he's fighting, the game ends and the player loses.</p><p>After the hero beats the monster in cave $i$, all subsequent visits to cave $i$ won't have any consequences: the cave won't have any monsters, and the hero's power won't change either.</p><p>Find the smallest possible power the hero must start the level with to be able to beat all the monsters and pass the level.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 100$). Description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $m$ ($3 \le n \le 1000$; $n \le m \le min(\frac{n(n-1)}{2}, 2000)$)&nbsp;— the number of caves and tunnels.</p><p>The second line contains $n-1$ integers $a_2, a_3, \ldots, a_n$ ($1 \le a_i \le 10^9$)&nbsp;— values the hero's power are compared to while fighting monsters in caves $2, 3, \ldots, n$.</p><p>The third line contains $n-1$ integers $b_2, b_3, \ldots, b_n$ ($1 \le b_i \le 10^9$)&nbsp;— increases applied to the hero's power for beating monsters in caves $2, 3, \ldots, n$.</p><p>Each of the next $m$ lines contains two integers $u_i$ and $v_i$ ($1 \le u_i, v_i \le n$; $u_i \ne v_i$)&nbsp;— the numbers of caves connected with a tunnel.</p><p>No two caves are connected with more than one tunnel. Any cave can be reached from any other cave by moving via tunnels. At least two tunnels come out of every cave.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $1000$, and the sum of $m$ over all test cases does not exceed $2000$.</p></div><div class="output-specification"><p>For each test case print a single integer&nbsp;— the smallest possible power the hero must start the level with to be able to beat all the monsters and pass the level.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 100$). Description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $m$ ($3 \le n \le 1000$; $n \le m \le min(\frac{n(n-1)}{2}, 2000)$)&nbsp;— the number of caves and tunnels.</p><p>The second line contains $n-1$ integers $a_2, a_3, \ldots, a_n$ ($1 \le a_i \le 10^9$)&nbsp;— values the hero's power are compared to while fighting monsters in caves $2, 3, \ldots, n$.</p><p>The third line contains $n-1$ integers $b_2, b_3, \ldots, b_n$ ($1 \le b_i \le 10^9$)&nbsp;— increases applied to the hero's power for beating monsters in caves $2, 3, \ldots, n$.</p><p>Each of the next $m$ lines contains two integers $u_i$ and $v_i$ ($1 \le u_i, v_i \le n$; $u_i \ne v_i$)&nbsp;— the numbers of caves connected with a tunnel.</p><p>No two caves are connected with more than one tunnel. Any cave can be reached from any other cave by moving via tunnels. At least two tunnels come out of every cave.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $1000$, and the sum of $m$ over all test cases does not exceed $2000$.</p>

## Output

<p>For each test case print a single integer&nbsp;— the smallest possible power the hero must start the level with to be able to beat all the monsters and pass the level.</p>





```input1
3
4 4
11 22 13
8 7 5
1 2
2 3
3 4
4 1
4 4
11 22 13
5 7 8
1 2
2 3
3 4
4 1
5 7
10 40 20 30
7 2 10 5
1 2
1 5
2 3
2 4
2 5
3 4
4 5
```




```output1
15
15
19
```



## Note

<p>In the first test case, the hero can pass the level with initial power $15$ as follows: </p><ul> <li> move from cave $1$ to cave $2$: since $15 &gt; 11$, the hero beats the monster, and his power increases to $15 + 8 = 23$; </li><li> move from cave $2$ to cave $3$: since $23 &gt; 22$, the hero beats the monster, and his power increases to $23 + 7 = 30$; </li><li> move from cave $3$ to cave $4$: since $30 &gt; 13$, the hero beats the monster, and his power increases to $30 + 5 = 35$. </li></ul><p>In the second test case, the situation is similar except that the power increases for beating monsters in caves $2$ and $4$ are exchanged. The hero can follow a different route, $1 \rightarrow 4 \rightarrow 3 \rightarrow 2$, and pass the level with initial power $15$.</p><p>In the third test case, the hero can pass the level with initial power $19$ as follows: </p><ul> <li> move from cave $1$ to cave $2$: since $19 &gt; 10$, the hero beats the monster, and his power increases to $19 + 7 = 26$; </li><li> move from cave $2$ to cave $4$: since $26 &gt; 20$, the hero beats the monster, and his power increases to $26 + 10 = 36$; </li><li> move from cave $4$ to cave $5$: since $36 &gt; 30$, the hero beats the monster, and his power increases to $36 + 5 = 41$; </li><li> move from cave $5$ to cave $2$: there is no monster in this cave anymore, nothing happens; </li><li> move from cave $2$ to cave $3$: since $41 &gt; 40$, the hero beats the monster, and his power increases to $41 + 2 = 43$. </li></ul>
