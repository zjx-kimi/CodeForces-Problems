## Description

<div><p>Pak Chanek comes up with an idea in the midst of boredom to play a game. The game is a rock tower game. There is a big rock that is used as a base. There are also $N$ small identical rocks that Pak Chanek will use to build a rock tower with a height of $N$ above the base rock.</p><p>Initially, there are no small rocks that are located above the base rock. In other words, the height of the tower above the base rock is initially $0$. In one move, Pak Chanek can place one small rock onto the top of the tower which makes the height of the tower above the base rock increase by $1$. Each time Pak Chanek place one small rock, the following will happen after the small rock is placed: </p><ul> <li> Let's say $x$ is the height of the tower above the base rock <span class="tex-font-style-bf">right after the small rock is placed</span>. </li><li> There is a probability of $P_x$ percent that the topmost rock falls. </li><li> If $x \geq 2$ and the topmost rock falls, then there is another probability of $P_x$ percent that the $2$-nd topmost rock also falls. </li><li> If $x \geq 3$ and the $2$-nd topmost rock falls, then there is another probability of $P_x$ percent that the $3$-rd topmost rock also falls. </li><li> If $x \geq 4$ and the $3$-rd topmost rock falls, then there is another probability of $P_x$ percent that the $4$-th topmost rock also falls. </li><li> And so on. </li></ul><p>If the tower successfully reaches a height of $N$ without any rocks falling after that, then the game is ended.</p><p>If given an integer array $[P_1, P_2, \ldots, P_N]$, what is the expected value of the number of moves that Pak Chanek needs to do to end the game? It can be proven that the expected value can be represented as an simple fraction $\frac{P}{Q}$ where $Q$ is coprime to $998\,244\,353$. Output the value of $P \times Q^{-1}$ modulo $998\,244\,353$.</p></div><div class="input-specification"><p>The first line contains a single integer $N$ ($1 \leq N \leq 2\cdot10^5$) — the required height of the rock tower.</p><p>The second line contains $N$ integers $P_1, P_2, P_3, \ldots, P_N$ ($0 \leq P_i \leq 99$).</p></div><div class="output-specification"><p>An integer representing the expected value of the number of moves that Pak Chanek needs to do to end the game, modulo $998\,244\,353$.</p></div>

## Input

<p>The first line contains a single integer $N$ ($1 \leq N \leq 2\cdot10^5$) — the required height of the rock tower.</p><p>The second line contains $N$ integers $P_1, P_2, P_3, \ldots, P_N$ ($0 \leq P_i \leq 99$).</p>

## Output

<p>An integer representing the expected value of the number of moves that Pak Chanek needs to do to end the game, modulo $998\,244\,353$.</p>





```input1
2
80 50
```




```input2
3
25 16 20
```




```output1
499122186
```




```output2
879786027
```



## Note

<p>In the first example, the expected value of the number of moves that Pak Chanek needs to do to end the game is $\frac{19}{2}$.</p>
