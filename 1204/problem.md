## Description

<div><p>One day, you are accepted as being Dr. Chanek's assistant. The first task given by Dr. Chanek to you is to take care and store his magical stones.</p><p>Dr. Chanek has $N$ magical stones with $N$ being an even number. Those magical stones are numbered from $1$ to $N$. Magical stone $i$ has a strength of $A_i$. A magical stone can be painted with two colours, namely the colour black or the colour white. You are tasked to paint the magical stones with the colour black or white and store the magical stones into a magic box with a magic coefficient $Z$ ($0 \leq Z \leq 2$). The painting of the magical stones must be done in a way such that there are $\frac{N}{2}$ black magical stones and $\frac{N}{2}$ white magical stones.</p><p>Define $\text{concat}(x, y)$ for two integers $x$ and $y$ as the result of concatenating the digits of $x$ to the left of $y$ in their decimal representation without changing the order. As an example, $\text{concat}(10, 24)$ will result in $1024$.</p><p>For a magic box with a magic coefficient $Z$, magical stone $i$ will react with magical stone $j$ if the colours of both stones are different and $\text{concat}(A_i, A_j) \times \text{concat}(A_j, A_i) + A_i \times A_j \equiv Z \mod 3$. A magical stone that is reacting will be very hot and dangerous. Because of that, you must colour the magical stones and determine the magic coefficient $Z$ of the magic box in a way such that there is no magical stone that reacts, or report if it is impossible.</p></div><div class="input-specification"><p>The first line contains a single <span class="tex-font-style-bf">even</span> integer $N$ ($2 \le N \le 10^5$) — the number of magical stones Dr. Chanek has.</p><p>The second line contains $N$ integer $A_1, A_2, \ldots, A_N$ ($1 \leq A_i \leq 10^9$) — the strengths of all magical stones.</p></div><div class="output-specification"><p>If it is not possible to satisfy the condition of the problem, output $-1$.</p><p>Otherwise, output two lines. The first line contains an integer $Z$ denoting the magic coefficient of the magic box. The second line contains a string $S$ of length $N$. $S_i$ is $0$ if magical stone $i$ is coloured black or $1$ if magical stone $i$ is coloured white. If there are more than one possibilities of colouring and choosing the magic coefficient $Z$, output any of them.</p></div>

## Input

<p>The first line contains a single <span class="tex-font-style-bf">even</span> integer $N$ ($2 \le N \le 10^5$) — the number of magical stones Dr. Chanek has.</p><p>The second line contains $N$ integer $A_1, A_2, \ldots, A_N$ ($1 \leq A_i \leq 10^9$) — the strengths of all magical stones.</p>

## Output

<p>If it is not possible to satisfy the condition of the problem, output $-1$.</p><p>Otherwise, output two lines. The first line contains an integer $Z$ denoting the magic coefficient of the magic box. The second line contains a string $S$ of length $N$. $S_i$ is $0$ if magical stone $i$ is coloured black or $1$ if magical stone $i$ is coloured white. If there are more than one possibilities of colouring and choosing the magic coefficient $Z$, output any of them.</p>





```input1
4
4 10 9 14
```




```output1
0
1001
```



## Note

<p>By giving the above colouring, it can be seen that: </p><ul> <li> $i=1, j=2 \longrightarrow \text{concat}(4, 10) \times \text{concat}(10, 4) + 10 \times 4 = 410 \times 104 + 40 = 42680 \equiv 2 \mod 3$ </li><li> $i=1, j=3 \longrightarrow \text{concat}(4, 9) \times \text{concat}(9, 4) + 4 \times 9 = 49 \times 94 + 36 = 4642 \equiv 1 \mod 3$ </li><li> $i=4, j=2 \longrightarrow \text{concat}(14, 10) \times \text{concat}(10, 14) + 10 \times 14 = 1410 \times 1014 + 140 = 1429880 \equiv 2 \mod 3$ </li><li> $i=4, j=3 \longrightarrow \text{concat}(14, 9) \times \text{concat}(9, 14) + 14 \times 9 = 149 \times 914 + 126 = 136312 \equiv 1 \mod 3$ </li></ul><p>Because of that, by choosing $Z = 0$, it can be guaranteed that there is no magical stone that reacts.</p>
