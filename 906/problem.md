## Description

<div><p>You are at your grandparents' house and you are playing an old video game on a strange console. Your controller has only two buttons and each button has a number written on it.</p><p>Initially, your score is $0$. The game is composed of $n$ rounds. For each $1\le i\le n$, the $i$-th round works as follows.</p><p>On the screen, a symbol $s_i$ appears, which is either $\texttt{+}$ (<span class="tex-font-style-it">plus</span>) or $\texttt{-}$ (<span class="tex-font-style-it">minus</span>). Then you must press one of the two buttons on the controller <span class="tex-font-style-bf">once</span>. Suppose you press a button with the number $x$ written on it: your score will increase by $x$ if the symbol was $\texttt{+}$ and will decrease by $x$ if the symbol was $\texttt{-}$. After you press the button, the round ends. </p><p>After you have played all $n$ rounds, you win if your score is $0$.</p><p>Over the years, your grandparents bought many different controllers, so you have $q$ of them. The two buttons on the $j$-th controller have the numbers $a_j$ and $b_j$ written on them. For each controller, you must compute whether you can win the game playing with that controller.</p></div><div class="input-specification"><p>The first line contains a single integer $n$ ($1 \le n \le 2\cdot 10^5$) — the number of rounds.</p><p>The second line contains a string $s$ of length $n$ — where $s_i$ is the symbol that will appear on the screen in the $i$-th round. It is guaranteed that $s$ contains only the characters $\texttt{+}$ and $\texttt{-}$.</p><p>The third line contains an integer $q$ ($1 \le q \le 10^5$) — the number of controllers.</p><p>The following $q$ lines contain two integers $a_j$ and $b_j$ each ($1 \le a_j, b_j \le 10^9$) — the numbers on the buttons of controller $j$. </p></div><div class="output-specification"><p>Output $q$ lines. On line $j$ print $\texttt{YES}$ if the game is winnable using controller $j$, otherwise print $\texttt{NO}$.</p></div>

## Input

<p>The first line contains a single integer $n$ ($1 \le n \le 2\cdot 10^5$) — the number of rounds.</p><p>The second line contains a string $s$ of length $n$ — where $s_i$ is the symbol that will appear on the screen in the $i$-th round. It is guaranteed that $s$ contains only the characters $\texttt{+}$ and $\texttt{-}$.</p><p>The third line contains an integer $q$ ($1 \le q \le 10^5$) — the number of controllers.</p><p>The following $q$ lines contain two integers $a_j$ and $b_j$ each ($1 \le a_j, b_j \le 10^9$) — the numbers on the buttons of controller $j$. </p>

## Output

<p>Output $q$ lines. On line $j$ print $\texttt{YES}$ if the game is winnable using controller $j$, otherwise print $\texttt{NO}$.</p>





```input1
8
+-+---+-
5
2 1
10 3
7 9
10 10
5 3
```




```input2
6
+-++--
2
9 7
1 1
```




```input3
20
+-----+--+--------+-
2
1000000000 99999997
250000000 1000000000
```




```output1
YES
NO
NO
NO
YES
```




```output2
YES
YES
```




```output3
NO
YES
```



## Note

<p>In the <span class="tex-font-style-bf">first sample</span>, one possible way to get score $0$ using the first controller is by pressing the button with numnber $1$ in rounds $1$, $2$, $4$, $5$, $6$ and $8$, and pressing the button with number $2$ in rounds $3$ and $7$. It is possible to show that there is no way to get a score of $0$ using the second controller.</p>
