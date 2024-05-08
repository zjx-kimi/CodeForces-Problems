## Description

<div><p>$n$ players are playing a game. </p><p>There are two different maps in the game. For each player, we know his strength on each map. When two players fight on a specific map, the player with higher strength on that map always wins. No two players have the same strength on the same map. </p><p>You are the game master and want to organize a tournament. There will be a total of $n-1$ battles. While there is more than one player in the tournament, choose any map and any two remaining players to fight on it. The player who loses will be eliminated from the tournament. </p><p>In the end, exactly one player will remain, and he is declared the winner of the tournament. For each player determine if he can win the tournament.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 100$) — the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \leq n \leq 10^5$) — the number of players.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \leq a_i \leq 10^9$, $a_i \neq a_j$ for $i \neq j$), where $a_i$ is the strength of the $i$-th player on the first map. </p><p>The third line of each test case contains $n$ integers $b_1, b_2, \dots, b_n$ ($1 \leq b_i \leq 10^9$, $b_i \neq b_j$ for $i \neq j$), where $b_i$ is the strength of the $i$-th player on the second map. </p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p></div><div class="output-specification"><p>For each test case print a string of length $n$. $i$-th character should be "<span class="tex-font-style-tt">1</span>" if the $i$-th player can win the tournament, or "<span class="tex-font-style-tt">0</span>" otherwise.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 100$) — the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \leq n \leq 10^5$) — the number of players.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \leq a_i \leq 10^9$, $a_i \neq a_j$ for $i \neq j$), where $a_i$ is the strength of the $i$-th player on the first map. </p><p>The third line of each test case contains $n$ integers $b_1, b_2, \dots, b_n$ ($1 \leq b_i \leq 10^9$, $b_i \neq b_j$ for $i \neq j$), where $b_i$ is the strength of the $i$-th player on the second map. </p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p>

## Output

<p>For each test case print a string of length $n$. $i$-th character should be "<span class="tex-font-style-tt">1</span>" if the $i$-th player can win the tournament, or "<span class="tex-font-style-tt">0</span>" otherwise.</p>





```input1
3
4
1 2 3 4
1 2 3 4
4
11 12 20 21
44 22 11 30
1
1000000000
1000000000
```




```output1
0001
1111
1
```



## Note

<p>In the first test case, the $4$-th player will beat any other player on any game, so he will definitely win the tournament.</p><p>In the second test case, everyone can be a winner. </p><p>In the third test case, there is only one player. Clearly, he will win the tournament.</p>
