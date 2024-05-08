## Description

<div><p>A boy called Smilo is playing a new game! In the game, there are $n$ hordes of monsters, and the $i$-th horde contains $a_i$ monsters. The goal of the game is to destroy all the monsters. To do this, you have two types of attacks and a combo counter $x$, initially set to $0$:</p><ul> <li> The first type: you choose a number $i$ from $1$ to $n$, such that there is at least one monster left in the horde with the number $i$. Then, you kill one monster from horde number $i$, and the combo counter $x$ increases by $1$. </li><li> The second type: you choose a number $i$ from $1$ to $n$, such that there are at least $x$ monsters left in the horde with number $i$. Then, you use an ultimate attack and kill $x$ monsters from the horde with number $i$. After that, $x$ is reset to zero.</li></ul><p>Your task is to destroy all of the monsters, meaning that there should be no monsters left in any of the hordes. Smilo wants to win as quickly as possible, so he wants to the minimum number of attacks required to win the game. </p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \leq t \leq 10^4$) — the number of test cases. The descriptions of the test cases follow.</p><p>The first line of each input data set contains a single integer $n$ ($1 \leq n \leq 2 \cdot 10^5$) — the number of hordes of monsters.</p><p>The second line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \leq a_i \leq 10^9$) — the number of monsters in each horde.</p><p>It is guaranteed that the sum of $n$ across all test cases does not exceed $2 \cdot {10^5}$.</p></div><div class="output-specification"><p>For each test case, out put the minimum number of attacks required to kill all monsters.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \leq t \leq 10^4$) — the number of test cases. The descriptions of the test cases follow.</p><p>The first line of each input data set contains a single integer $n$ ($1 \leq n \leq 2 \cdot 10^5$) — the number of hordes of monsters.</p><p>The second line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \leq a_i \leq 10^9$) — the number of monsters in each horde.</p><p>It is guaranteed that the sum of $n$ across all test cases does not exceed $2 \cdot {10^5}$.</p>

## Output

<p>For each test case, out put the minimum number of attacks required to kill all monsters.</p>





```input1|2,3,6,7
4
4
1 3 1 1
4
1 2 1 1
6
3 2 1 5 2 4
2
1 6
```




```output1
4
4
11
5
```



## Note

<p>In the first test case, we can use an attack of the first type on the $1$-st, $3$-rd and $4$-th hordes, and then use an attack of the second type to finish off the $2$-nd horde. We need $4$ attacks in total.</p><p>In the second test case, we can use an attack of the first type on the $1$-st and $3$-rd hordes, then use an attack of the second type to finish off the $2$-nd horde, and then use an attack of the first type on the $4$-th horde. We need $4$ attacks in total.</p><p>In the fourth test case, we can use an attack of the first type once on the $1$-st horde, twice on the $2$-nd horde, and then use an attack of the second type on the $2$-nd horde, and finally use an attack of the first type to finish off the $2$-nd horde. We need $5$ attacks in total.</p>
