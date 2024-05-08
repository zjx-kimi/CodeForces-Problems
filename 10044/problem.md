## Description

<div><p>You are at a dueling arena. You also possess $n$ Pokémons. Initially, only the $1$-st Pokémon is standing in the arena.</p><p>Each Pokémon has $m$ attributes. The $j$-th attribute of the $i$-th Pokémon is $a_{i,j}$. Each Pokémon also has a cost to be hired: the $i$-th Pokémon's cost is $c_i$.</p><p>You want to have the $n$-th Pokémon stand in the arena. To do that, you can perform the following two types of operations any number of times in any order: </p><ul> <li> Choose three integers $i$, $j$, $k$ ($1 \le i \le n$, $1 \le j \le m$, $k &gt; 0$), increase $a_{i,j}$ by $k$ permanently. The cost of this operation is $k$. </li><li> Choose two integers $i$, $j$ ($1 \le i \le n$, $1 \le j \le m$) and hire the $i$-th Pokémon to duel with the current Pokémon in the arena based on the $j$-th attribute. The $i$-th Pokémon will win if $a_{i,j}$ is <span class="tex-font-style-bf">greater than or equal to</span> the $j$-th attribute of the current Pokémon in the arena (otherwise, it will lose). After the duel, only the winner will stand in the arena. The cost of this operation is $c_i$. </li></ul><p>Find the minimum cost you need to pay to have the $n$-th Pokémon stand in the arena.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^5$). The description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $m$ ($2 \le n \le 4 \cdot 10^5$, $1 \le m \le 2 \cdot 10^5$, $2 \leq n \cdot m \leq 4 \cdot 10^5$).</p><p>The second line of each test case contains $n$ integers $c_1, c_2, \ldots, c_n$ ($1 \le c_i \le 10^9$).</p><p>The $i$-th of the following $n$ lines contains $m$ integers $a_{i,1}, a_{i,2}, \ldots, a_{i,m}$ ($1 \le a_{i,j} \le 10^9$).</p><p>It is guaranteed that the sum of $n \cdot m$ over all test cases does not exceed $4 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output the minimum cost to make the $n$-th Pokémon stand in the arena.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^5$). The description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $m$ ($2 \le n \le 4 \cdot 10^5$, $1 \le m \le 2 \cdot 10^5$, $2 \leq n \cdot m \leq 4 \cdot 10^5$).</p><p>The second line of each test case contains $n$ integers $c_1, c_2, \ldots, c_n$ ($1 \le c_i \le 10^9$).</p><p>The $i$-th of the following $n$ lines contains $m$ integers $a_{i,1}, a_{i,2}, \ldots, a_{i,m}$ ($1 \le a_{i,j} \le 10^9$).</p><p>It is guaranteed that the sum of $n \cdot m$ over all test cases does not exceed $4 \cdot 10^5$.</p>

## Output

<p>For each test case, output the minimum cost to make the $n$-th Pokémon stand in the arena.</p>





```input1|2,3,4,5,6,12,13,14,15,16,17
4
3 3
2 3 1
2 9 9
6 1 7
1 2 1
3 3
2 3 1
9 9 9
6 1 7
1 2 1
4 2
2 8 3 5
18 24
17 10
1 10
1 1
6 3
21412674 3212925 172015806 250849370 306960171 333018900
950000001 950000001 950000001
821757276 783362401 760000001
570000001 700246226 600757652
380000001 423513575 474035234
315201473 300580025 287023445
1 1 1
```




```output1
2
6
17
1224474550
```



## Note

<p>In the first test case, the attribute array of the $1$-st Pokémon (which is standing in the arena initially) is $[2,9,9]$.</p><p>In the first operation, you can choose $i=3$, $j=1$, $k=1$, and increase $a_{3,1}$ by $1$ permanently. Now the attribute array of the $3$-rd Pokémon is $[2,2,1]$. The cost of this operation is $k = 1$.</p><p>In the second operation, you can choose $i=3$, $j=1$, and hire the $3$-rd Pokémon to duel with the current Pokémon in the arena based on the $1$-st attribute. Since $a_{i,j}=a_{3,1}=2 \ge 2=a_{1,1}$, the $3$-rd Pokémon will win. The cost of this operation is $c_3 = 1$.</p><p>Thus, we have made the $3$-rd Pokémon stand in the arena within the cost of $2$. It can be proven that $2$ is minimum possible.</p><p>In the second test case, the attribute array of the $1$-st Pokémon in the arena is $[9,9,9]$.</p><p>In the first operation, you can choose $i=2$, $j=3$, $k=2$, and increase $a_{2,3}$ by $2$ permanently. Now the attribute array of the $2$-nd Pokémon is $[6,1,9]$. The cost of this operation is $k = 2$.</p><p>In the second operation, you can choose $i=2$, $j=3$, and hire the $2$-nd Pokémon to duel with the current Pokémon in the arena based on the $3$-rd attribute. Since $a_{i,j}=a_{2,3}=9 \ge 9=a_{1,3}$, the $2$-nd Pokémon will win. The cost of this operation is $c_2 = 3$.</p><p>In the third operation, you can choose $i=3$, $j=2$, and hire the $3$-rd Pokémon to duel with the current Pokémon in the arena based on the $2$-nd attribute. Since $a_{i,j}=a_{1,2}=2 \ge 1=a_{2,2}$, the $3$-rd Pokémon can win. The cost of this operation is $c_3 = 1$.</p><p>Thus, we have made the $3$-rd Pokémon stand in the arena within the cost of $6$. It can be proven that $6$ is minimum possible.</p>
