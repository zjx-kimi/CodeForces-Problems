## Description

<div><p>Adilbek has to water his garden. He is going to do it with the help of a complex watering system: he only has to deliver water to it, and the mechanisms will do all the remaining job.</p><p>The watering system consumes one liter of water per minute (if there is no water, it is not working). It can hold no more than $c$ liters. Adilbek has already poured $c_0$ liters of water into the system. He is going to start watering the garden right now and water it for $m$ minutes, and the watering system should contain at least one liter of water at the beginning of the $i$-th minute (for every $i$ from $0$ to $m - 1$).</p><p>Now Adilbek wonders what he will do if the watering system runs out of water. He called $n$ his friends and asked them if they are going to bring some water. The $i$-th friend answered that he can bring no more than $a_i$ liters of water; he will arrive at the beginning of the $t_i$-th minute and pour all the water he has into the system (if the system cannot hold such amount of water, the excess water is poured out); and then he will ask Adilbek to pay $b_i$ dollars for each liter of water he has brought. You may assume that if a friend arrives at the beginning of the $t_i$-th minute and the system runs out of water at the beginning of the same minute, the friend pours his water fast enough so that the system does not stop working.</p><p>Of course, Adilbek does not want to pay his friends, but he has to water the garden. So he has to tell his friends how much water should they bring. Formally, Adilbek wants to choose $n$ integers $k_1$, $k_2$, ..., $k_n$ in such a way that:</p><ul> <li> if each friend $i$ brings exactly $k_i$ liters of water, then the watering system works during the whole time required to water the garden; </li><li> the sum $\sum\limits_{i = 1}^{n} k_i b_i$ is minimum possible. </li></ul><p>Help Adilbek to determine the minimum amount he has to pay his friends or determine that Adilbek not able to water the garden for $m$ minutes.</p><p>You have to answer $q$ independent queries.</p></div><div class="input-specification"><p>The first line contains one integer $q$ ($1 \le q \le 5 \cdot 10^5$) – the number of queries.</p><p>The first line of each query contains four integers $n, m, c$ and $c_0$ ($0 \le n \le 5 \cdot 10^5, 2 \le m \le 10^9, 1 \le c_0 \le c \le 10^9$)&nbsp;— the number of friends, the number of minutes of watering, the capacity of the watering system and the number of liters poured by Adilbek.</p><p>Each of the next $n$ lines contains three integers $t_i, a_i, b_i$ ($ 0 &lt; t_i &lt; m, 1 \le a_i \le c, 1 \le b_i \le 10^9$) — the $i$-th friend's arrival time, the maximum amount of water $i$-th friend can bring and the cost of $1$ liter from $i$-th friend.</p><p>It is guaranteed that sum of all $n$ over all queries does not exceed $5 \cdot 10^5$.</p></div><div class="output-specification"><p>For each query print one integer&nbsp;— the minimum amount Adilbek has to pay his friends, or $-1$ if Adilbek is not able to water the garden for $m$ minutes.</p></div>

## Input

<p>The first line contains one integer $q$ ($1 \le q \le 5 \cdot 10^5$) – the number of queries.</p><p>The first line of each query contains four integers $n, m, c$ and $c_0$ ($0 \le n \le 5 \cdot 10^5, 2 \le m \le 10^9, 1 \le c_0 \le c \le 10^9$)&nbsp;— the number of friends, the number of minutes of watering, the capacity of the watering system and the number of liters poured by Adilbek.</p><p>Each of the next $n$ lines contains three integers $t_i, a_i, b_i$ ($ 0 &lt; t_i &lt; m, 1 \le a_i \le c, 1 \le b_i \le 10^9$) — the $i$-th friend's arrival time, the maximum amount of water $i$-th friend can bring and the cost of $1$ liter from $i$-th friend.</p><p>It is guaranteed that sum of all $n$ over all queries does not exceed $5 \cdot 10^5$.</p>

## Output

<p>For each query print one integer&nbsp;— the minimum amount Adilbek has to pay his friends, or $-1$ if Adilbek is not able to water the garden for $m$ minutes.</p>





```input1
4
1 5 4 2
2 4 2
0 4 5 4
2 5 3 1
1 2 4
3 1 3
2 3 5 1
2 1 1
1 4 3
```




```output1
6
0
-1
4
```


