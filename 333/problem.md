## Description

<div><p>Jellyfish has $n$ green apples with values $a_1, a_2, \dots, a_n$ and Gellyfish has $m$ green apples with values $b_1,b_2,\ldots,b_m$.</p><p>They will play a game with $k$ rounds. For $i=1,2,\ldots,k$ in this order, they will perform the following actions: </p><ul> <li> If $i$ is odd, Jellyfish can choose to swap one of her apples with one of Gellyfish's apples or do nothing. </li><li> If $i$ is even, Gellyfish can choose to swap one of his apples with one of Jellyfish's apples or do nothing. </li></ul><p>Both players want to maximize the sum of the values of their apples.</p><p>Since you are one of the smartest people in the world, Jellyfish wants you to tell her the final sum of the value of her apples after all $k$ rounds of the game. Assume that both Jellyfish and Gellyfish play optimally to maximize the sum of values of their apples.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \leq t \leq 2000$). The description of the test cases follows.</p><p>The first line of each test case contains three integers, $n$, $m$ and $k$ ($1 \leq n, m \leq 50$, $1 \leq k \leq 10^9$)&nbsp;— the number of green apples Jellyfish has, the number of green apples Gellyfish has and the number of rounds of the game respectively.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \leq a_i \leq 10^9$)&nbsp;— the values of Jellyfish's green apples.</p><p>The third line of each test case contains $m$ integers $b_1, b_2, \dots, b_m$ ($1 \leq b_i \leq 10^9$)&nbsp;— the values of Gellyfish's green apples.</p><p>Do note that the sum of $n$ and $m$ over all test cases are both not bounded.</p></div><div class="output-specification"><p>For each test case, output a single integer&nbsp;— the final sum of the values of Jellyfish's apples.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \leq t \leq 2000$). The description of the test cases follows.</p><p>The first line of each test case contains three integers, $n$, $m$ and $k$ ($1 \leq n, m \leq 50$, $1 \leq k \leq 10^9$)&nbsp;— the number of green apples Jellyfish has, the number of green apples Gellyfish has and the number of rounds of the game respectively.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \leq a_i \leq 10^9$)&nbsp;— the values of Jellyfish's green apples.</p><p>The third line of each test case contains $m$ integers $b_1, b_2, \dots, b_m$ ($1 \leq b_i \leq 10^9$)&nbsp;— the values of Gellyfish's green apples.</p><p>Do note that the sum of $n$ and $m$ over all test cases are both not bounded.</p>

## Output

<p>For each test case, output a single integer&nbsp;— the final sum of the values of Jellyfish's apples.</p>





```input1|2,3,4,8,9,10
4
2 2 1
1 2
3 4
1 1 10000
1
2
4 5 11037
1 1 4 5
1 9 1 9 8
1 1 1
2
1
```




```output1
6
1
19
2
```



## Note

<p>In the first test case, Jellyfish will swap the apple of value $1$ and $4$.</p><p>In the second test case, both players will swap the two apples $10,000$ times.</p><p>In the fourth test case, Jellyfish will do nothing.</p>
