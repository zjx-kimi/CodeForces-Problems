## Description

<div><p>Alice and Bob are playing a game. They have two strings $S$ and $T$ of the same length $n$ consisting of lowercase latin letters. Players take turns alternately, with Alice going first.</p><p>On her turn, Alice chooses an integer $i$ from $1$ to $n$, one of the strings $S$ or $T$, and any lowercase latin letter $c$, and replaces the $i$-th symbol in the chosen string with the character $c$.</p><p>On his turn, Bob chooses one of the strings $S$ or $T$, and reverses it. More formally, Bob makes the replacement $S := \operatorname{rev}(S)$ or $T := \operatorname{rev}(T)$, where $\operatorname{rev}(P) = P_n P_{n-1} \ldots P_1$.</p><p>The game lasts until the strings $S$ and $T$ are equal. As soon as the strings become equal, the game <span class="tex-font-style-bf">ends instantly</span>.</p><p>Define <span class="tex-font-style-it">the duration of the game</span> as the total number of moves made by both players during the game. For example, if Alice made $2$ moves in total, and Bob made $1$ move, then the duration of this game is $3$.</p><p>Alice's goal is to minimize the duration of the game, and Bob's goal is to maximize the duration of the game.</p><p>What will be the duration of the game, if both players play optimally? It can be shown that the game will end in a finite number of turns.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^4$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 10^5$)&nbsp;— the length of the strings $S$ and $T$.</p><p>The second line of each test case contains a string $S$ of length $n$ consisting of lowercase latin letters.</p><p>The third line of each test case contains a string $T$ of length $n$ consisting of lowercase latin letters.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p></div><div class="output-specification"><p>For each test case, output a single number on a separate line&nbsp;— the duration of the described game, if both players play optimally.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^4$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 10^5$)&nbsp;— the length of the strings $S$ and $T$.</p><p>The second line of each test case contains a string $S$ of length $n$ consisting of lowercase latin letters.</p><p>The third line of each test case contains a string $T$ of length $n$ consisting of lowercase latin letters.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p>

## Output

<p>For each test case, output a single number on a separate line&nbsp;— the duration of the described game, if both players play optimally.</p>





```input1|2,3,4,8,9,10,14,15,16,20,21,22
7
5
abcde
abxde
5
hello
olleo
2
ab
cd
7
aaaaaaa
abbbbba
1
q
q
6
yoyoyo
oyoyoy
8
abcdefgh
hguedfbh
```




```output1
1
2
3
9
0
2
6
```



## Note

<p>In the first test case, in her turn, Alice can replace the third symbol of the string $S$ with <span class="tex-font-style-tt">x</span>. After that, both strings will become equal to "<span class="tex-font-style-tt">abxde</span>" and the game will end after one move. Since Alice's goal is to finish the game in as few moves as possible, this move will be one of her optimal first moves, and the final answer will be $1$.</p><p>In the second test case, in her turn, Alice can replace the fifth symbol of the string $T$ with <span class="tex-font-style-tt">h</span>. After this move, $S =$ "<span class="tex-font-style-tt">hello</span>", $T =$ "<span class="tex-font-style-tt">olleh</span>". Then Bob makes his turn. In his turn, he must reverse one of the strings. If Bob chooses the string $S$, then after his turn both strings will be equal to "<span class="tex-font-style-tt">olleh</span>", and if he chooses the string $T$, then after his turn both strings will be equal to "<span class="tex-font-style-tt">hello</span>". Thus, after the presented first move of Alice, the game will definitely end in $2$ moves. It can be shown that there is no strategy for Alice to finish the game in less than $2$ moves, with both players playing optimally. The final answer is $2$.</p><p>In the third test case, in her first move, Alice can replace the second symbol of the string $S$ with <span class="tex-font-style-tt">c</span>. After this move, $S =$ "<span class="tex-font-style-tt">ac</span>", $T =$ "<span class="tex-font-style-tt">cd</span>". Then Bob makes his turn. If Bob reverses the string $S$, then after his turn $S =$ "<span class="tex-font-style-tt">ca</span>", $T =$ "<span class="tex-font-style-tt">cd</span>". Then it is easy to see that in this case Alice can definitely finish the game on the $3$-rd move, by replacing the second symbol of the string $T$ with <span class="tex-font-style-tt">a</span>, after which both strings will become equal to "<span class="tex-font-style-tt">ca</span>". If Bob reverses the string $T$, then after his turn $S =$ "<span class="tex-font-style-tt">ac</span>", $T =$ "<span class="tex-font-style-tt">dc</span>". In this case, Alice can also definitely finish the game on the $3$rd move, by replacing the first symbol of the string $S$ with <span class="tex-font-style-tt">d</span>, after which both strings will become equal to "<span class="tex-font-style-tt">dc</span>". Thus, Alice can definitely finish the game in $3$ moves regardless of Bob's moves. It can be shown that the game cannot end in less than $3$ moves, with both players playing optimally.</p><p>In the fifth test case, the strings $S$ and $T$ are equal, so the game will end without starting, in $0$ moves.</p>
