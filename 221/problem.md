## Description

<div><p>Let's consider a game in which two players, A and B, participate. This game is characterized by two positive integers, $X$ and $Y$.</p><p>The game consists of <span class="tex-font-style-it">sets</span>, and each <span class="tex-font-style-it">set</span> consists of <span class="tex-font-style-it">plays</span>. In each <span class="tex-font-style-it">play</span>, <span class="tex-font-style-bf">exactly one</span> of the players, either A or B, wins. A <span class="tex-font-style-it">set</span> ends <span class="tex-font-style-bf">exactly</span> when one of the players reaches $X$ wins in the <span class="tex-font-style-it">plays</span> of that <span class="tex-font-style-it">set</span>. This player is declared the winner of the <span class="tex-font-style-it">set</span>. The players play <span class="tex-font-style-it">sets</span> until one of them reaches $Y$ wins in the <span class="tex-font-style-it">sets</span>. After that, the game ends, and this player is declared the winner of the entire game.</p><p>You have just watched a game but didn't notice who was declared the winner. You remember that during the game, $n$ <span class="tex-font-style-it">plays</span> were played, and you know which player won each <span class="tex-font-style-it">play</span>. However, you <span class="tex-font-style-bf">do not know</span> the values of $X$ and $Y$. Based on the available information, determine who won the entire game&nbsp;— A or B. If there is not enough information to determine the winner, you should also report it.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains a single integer $t$ $(1 \leq t \leq 10^4)$ - the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains an integer $n$ $(1 \leq n \leq 20)$ - the number of <span class="tex-font-style-it">plays</span> played during the game.</p><p>The second line of each test case contains a string $s$ of length $n$, consisting of characters $\texttt{A}$ and $\texttt{B}$. If $s_i = \texttt{A}$, it means that player A won the $i$-th <span class="tex-font-style-it">play</span>. If $s_i = \texttt{B}$, it means that player B won the $i$-th <span class="tex-font-style-it">play</span>.</p><p><span class="tex-font-style-bf">It is guaranteed that the given sequence of <span class="tex-font-style-it">plays</span> corresponds to at least one valid game scenario, for some values of $X$ and $Y$</span>.</p></div><div class="output-specification"><p>For each test case, output:</p><ul><li> $\texttt{A}$&nbsp;— if player A is guaranteed to be the winner of the game.</li><li> $\texttt{B}$&nbsp;— if player B is guaranteed to be the winner of the game.</li><li> $\texttt{?}$&nbsp;— if it is <span class="tex-font-style-bf">impossible</span> to determine the winner of the game.</li></ul></div>

## Input

<p>Each test contains multiple test cases. The first line contains a single integer $t$ $(1 \leq t \leq 10^4)$ - the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains an integer $n$ $(1 \leq n \leq 20)$ - the number of <span class="tex-font-style-it">plays</span> played during the game.</p><p>The second line of each test case contains a string $s$ of length $n$, consisting of characters $\texttt{A}$ and $\texttt{B}$. If $s_i = \texttt{A}$, it means that player A won the $i$-th <span class="tex-font-style-it">play</span>. If $s_i = \texttt{B}$, it means that player B won the $i$-th <span class="tex-font-style-it">play</span>.</p><p><span class="tex-font-style-bf">It is guaranteed that the given sequence of <span class="tex-font-style-it">plays</span> corresponds to at least one valid game scenario, for some values of $X$ and $Y$</span>.</p>

## Output

<p>For each test case, output:</p><ul><li> $\texttt{A}$&nbsp;— if player A is guaranteed to be the winner of the game.</li><li> $\texttt{B}$&nbsp;— if player B is guaranteed to be the winner of the game.</li><li> $\texttt{?}$&nbsp;— if it is <span class="tex-font-style-bf">impossible</span> to determine the winner of the game.</li></ul>





```input1|2,3,6,7,10,11,14,15
7
5
ABBAA
3
BBB
7
BBAAABA
20
AAAAAAAABBBAABBBBBAB
1
A
13
AAAABABBABBAB
7
BBBAAAA
```




```output1
A
B
A
B
A
B
A
```



## Note

<p>In the first test case, the game could have been played with parameters $X = 3$, $Y = 1$. The game consisted of $1$ set, in which player A won, as they won the first $3$ plays. In this scenario, player A is the winner. The game could also have been played with parameters $X = 1$, $Y = 3$. It can be shown that there are no such $X$ and $Y$ values for which player B would be the winner.</p><p>In the second test case, player B won all the plays. It can be easily shown that in this case, player B is guaranteed to be the winner of the game.</p><p>In the fourth test case, the game could have been played with parameters $X = 3$, $Y = 3$:</p><ul><li> In the first set, $3$ plays were played: <span class="tex-font-style-bf"><span class="tex-font-style-tt">AAA</span></span>. Player A is declared the winner of the set.</li><li> In the second set, $3$ plays were played: <span class="tex-font-style-bf"><span class="tex-font-style-tt">AAA</span></span>. Player A is declared the winner of the set.</li><li> In the third set, $5$ plays were played: <span class="tex-font-style-bf"><span class="tex-font-style-tt">AABBB</span></span>. Player B is declared the winner of the set.</li><li> In the fourth set, $5$ plays were played: <span class="tex-font-style-bf"><span class="tex-font-style-tt">AABBB</span></span>. Player B is declared the winner of the set.</li><li> In the fifth set, $4$ plays were played: <span class="tex-font-style-bf"><span class="tex-font-style-tt">BBAB</span></span>. Player B is declared the winner of the set.</li></ul><p>In total, player B was the first player to win $3$ sets. They are declared the winner of the game.</p>
