## Description

<div><p><span class="tex-font-style-bf">This is the easy version of this problem. The difference between easy and hard versions is the constraint on $k$ and the time limit. Also, in this version of the problem, you only need to calculate the answer when $n=k$. You can make hacks only if both versions of the problem are solved.</span></p><p>Cirno is playing a war simulator game with $n$ towers (numbered from $1$ to $n$) and $n$ bots (numbered from $1$ to $n$). The $i$-th tower is initially occupied by the $i$-th bot for $1 \le i \le n$.</p><p>Before the game, Cirno first chooses a permutation $p = [p_1, p_2, \ldots, p_n]$ of length $n$ (A permutation of length $n$ is an array of length $n$ where each integer between $1$ and $n$ appears exactly once). After that, she can choose a sequence $a = [a_1, a_2, \ldots, a_n]$ ($1 \le a_i \le n$ and $a_i \ne i$ for all $1 \le i \le n$).</p><p>The game has $n$ rounds of attacks. In the $i$-th round, if the $p_i$-th bot is still in the game, it will begin its attack, and as the result the $a_{p_i}$-th tower becomes occupied by the $p_i$-th bot; the bot that previously occupied the $a_{p_i}$-th tower will no longer occupy it. If the $p_i$-th bot is not in the game, nothing will happen in this round.</p><p>After each round, if a bot doesn't occupy any towers, it will be eliminated and leave the game. Please note that no tower can be occupied by more than one bot, but one bot can occupy more than one tower during the game.</p><p>At the end of the game, Cirno will record the result as a sequence $b = [b_1, b_2, \ldots, b_n]$, where $b_i$ is the number of the bot that occupies the $i$-th tower at the end of the game.</p><p>However, as a mathematics master, she wants you to solve the following counting problem instead of playing games:</p><p>Count the number of different pairs of sequences $a$ and $b$ that we can get from all possible choices of sequence $a$ and permutation $p$.</p><p>Since this number may be large, output it modulo $M$.</p></div><div class="input-specification"><p>The only line contains two positive integers $k$ and $M$ ($1\le k\le 5000$, $2\le M\le 10^9$ ). It is guaranteed that $2^{18}$ is a divisor of $M-1$ and $M$ is a prime number.</p><p>You need to calculate the answer for $n=k$.</p></div><div class="output-specification"><p>Output a single integer — the number of different pairs of sequences for $n=k$ modulo $M$.</p></div>

## Input

<p>The only line contains two positive integers $k$ and $M$ ($1\le k\le 5000$, $2\le M\le 10^9$ ). It is guaranteed that $2^{18}$ is a divisor of $M-1$ and $M$ is a prime number.</p><p>You need to calculate the answer for $n=k$.</p>

## Output

<p>Output a single integer — the number of different pairs of sequences for $n=k$ modulo $M$.</p>





```input1
1 998244353
```




```input2
2 998244353
```




```input3
3 998244353
```




```input4
8 998244353
```




```output1
0
```




```output2
2
```




```output3
24
```




```output4
123391016
```



## Note

<p>For $n=1$, no valid sequence $a$ exists. We regard the answer as $0$.</p><p>For $n=2$, there is only one possible array $a$: $[2, 1]$. </p><ul> <li> For array $a$ is $[2, 1]$ and permutation $p$ is $[1, 2]$, the sequence $b$ will be $[1, 1]$ after all rounds have finished. The details for each rounds: <ul> <li> In the first round, the first bot will begin its attack and successfully capture the tower $2$. After this round, the second bot will be eliminated and leave the game as all of its towers are occupied by other bots. </li><li> In the second round, the second bot is not in the game. </li></ul> </li><li> For array $a$ is $[2, 1]$ and permutation $p$ is $[2, 1]$, the sequence $b$ will be $[2, 2]$ after all rounds have finished. The details for each rounds: <ul> <li> In the first round, the second bot will begin its attack and successfully capture the tower $1$. After this round, the first bot will be eliminated and leave the game as all of its towers are occupied by other bots. </li><li> In the second round, the first bot is not in the game. </li></ul> </li></ul><p>So the number of different pairs of sequences $(a,b)$ is $2$ ($[2, 1]$, $[1, 1]$ and $[2, 1]$, $[2, 2]$) for $n=2$.</p>
