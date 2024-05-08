## Description

<div><p>$n$ people indexed with integers from $1$ to $n$ came to take part in a lottery. Each received a ticket with an integer from $0$ to $m$.</p><p>In a lottery, one integer called <span class="tex-font-style-it">target</span> is drawn uniformly from $0$ to $m$. $k$ tickets (or less, if there are not enough participants) with the closest numbers to the target are declared the winners. In case of a draw, a ticket belonging to the person with a smaller index is declared a winner.</p><p>Bytek decided to take part in the lottery. He knows the values on the tickets of all previous participants. He can pick whatever value he wants on his ticket, but unfortunately, as he is the last one to receive it, he is indexed with an integer $n + 1$. </p><p>Bytek wants to win the lottery. Thus, he wants to know what he should pick to maximize the chance of winning. He wants to know the smallest integer in case there are many such integers. Your task is to find it and calculate his chance of winning.</p></div><div class="input-specification"><p>In the first line of the input, there are the integers $n$, $m$, and $k$ ($1 \leq n \leq 10^6$, $0 \leq m \leq 10^{18}$, $1 \leq k \leq 10^6$).</p><p>In the following line, there are $n$ integers separated by a single space, denoting the numbers on tickets received by people participating in a lottery. These numbers are integers in the range from $0$ to $m$.</p></div><div class="output-specification"><p>You should output two integers separated by a single space on the standard output. The first should be equal to the number of target values (from $0$ to $m$), upon drawing which Baytek wins, given that he chooses his ticket optimally. The second should be equal to the integer Bytek should pick to maximize his chance of winning the lottery.</p></div>

## Input

<p>In the first line of the input, there are the integers $n$, $m$, and $k$ ($1 \leq n \leq 10^6$, $0 \leq m \leq 10^{18}$, $1 \leq k \leq 10^6$).</p><p>In the following line, there are $n$ integers separated by a single space, denoting the numbers on tickets received by people participating in a lottery. These numbers are integers in the range from $0$ to $m$.</p>

## Output

<p>You should output two integers separated by a single space on the standard output. The first should be equal to the number of target values (from $0$ to $m$), upon drawing which Baytek wins, given that he chooses his ticket optimally. The second should be equal to the integer Bytek should pick to maximize his chance of winning the lottery.</p>





```input1
3 6 2
1 4 5
```




```input2
7 7 1
2 4 7 3 0 1 6
```




```output1
4 2
```




```output2
1 5
```



## Note

<p>In the first example, Bytek wins for $4$ target values (namely $0, 1, 2, 3$) if he chooses integer $2$, which is the lowest optimal value. If he chooses $3$, he also wins in four cases, but it is not the lowest value.</p>
