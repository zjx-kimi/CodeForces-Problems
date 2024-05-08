## Description

<div><p>The King wants to marry off his daughter, and he wants her husband to have the greatest innate luckiness possible. To find such a person he decided to hold a heads-or-tails tournament. </p><p>If person $A$ with <span class="tex-font-style-underline">luckiness</span> $x$ and person $B$ with <span class="tex-font-style-underline">luckiness</span> $y$ play heads-or-tails against each other, person $A$ wins with probability $x/(x+y)$. </p><p>The tournament has several rounds. Each round some participants are split into pairs. Each pair plays against each other, and the loser leaves the tournament. </p><p>The participants are numbered from $1$ to $n$. During the first round, a number $k$ ($1 \le k \le n$) is selected such that $n-k/2$ is a power of $2$ (such $k$ always exists and is unique). Only participants numbered from $1$ to $k$ take part in the first round. It ensures that in all other rounds the number of participants is the power of $2$. </p><p>During other rounds, all the participants who still have not left the tournament take part. If during some round, participants numbered $p_1 &lt; \ldots &lt; p_{2m}$ take part, then they are split into pairs in the following manner: participant $p_{2i-1}$ plays against participant $p_{2i}$ for each $i$ from $1$ to $m$. </p><p>The rounds are held until only one participant is left. He is declared the winner of the tournament and he will marry the King's daughter. The princess can't wait to find out who is her future husband. She asked every participant to tell her his luckiness. Assuming they did not lie, she wants to know the probability of each participant winning the tournament. As you are the best friend of the princess, she asks you to help her.</p></div><div class="input-specification"><p>The first line of the input contains the number of participants, $n$ ($2 \le n \le 3 \cdot 10^5$). The second line of the input contains $n$ integer numbers, $a_1, \ldots, a_{n}$ ($1 \le a_i \le 10^9$). The luckiness of the $i$-th participant equals to $a_i$.</p></div><div class="output-specification"><p>Print $n$ numbers $p_i$. The $i$-th number should be the probability of the $i$-th participant winning the tournament. The absolute error of your answer must not exceed $10^{-9}$.</p></div>

## Input

<p>The first line of the input contains the number of participants, $n$ ($2 \le n \le 3 \cdot 10^5$). The second line of the input contains $n$ integer numbers, $a_1, \ldots, a_{n}$ ($1 \le a_i \le 10^9$). The luckiness of the $i$-th participant equals to $a_i$.</p>

## Output

<p>Print $n$ numbers $p_i$. The $i$-th number should be the probability of the $i$-th participant winning the tournament. The absolute error of your answer must not exceed $10^{-9}$.</p>





```input1
5
1 4 1 1 4
```




```output1
0.026 0.3584 0.0676 0.0616 0.4864
```



## Note

<p>Here is an example of a tournament bracket, showing the winning probability in each pair.</p><center> <img class="tex-graphics" src="file://MjYx7E6c.png" style="max-width: 100.0%;max-height: 100.0%;"> </center>
