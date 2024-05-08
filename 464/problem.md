## Description

<div><p>Mihai and Slavic were looking at a group of $n$ frogs, numbered from $1$ to $n$, all initially located at point $0$. Frog $i$ has a hop length of $a_i$. </p><p>Each second, frog $i$ hops $a_i$ units forward. Before any frogs start hopping, Slavic and Mihai can place <span class="tex-font-style-bf">exactly one</span> trap in a coordinate in order to catch all frogs that will ever pass through the corresponding coordinate.</p><p>However, the children can't go far away from their home so they can only place a trap in the first $n$ points (that is, in a point with a coordinate between $1$ and $n$) and the children can't place a trap in point $0$ since they are scared of frogs.</p><p>Can you help Slavic and Mihai find out what is the maximum number of frogs they can catch using a trap?</p></div><div class="input-specification"><p>The first line of the input contains a single integer $t$ ($1 \le t \le 100$) — the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \leq n \leq 2 \cdot 10^5$) — the number of frogs, which equals the distance Slavic and Mihai can travel to place a trap.</p><p>The second line of each test case contains $n$ integers $a_1, \ldots, a_n$ ($1 \leq a_i \leq 10^9$) — the lengths of the hops of the corresponding frogs.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case output a single integer&nbsp;— the maximum number of frogs Slavic and Mihai can catch using a trap.</p></div>

## Input

<p>The first line of the input contains a single integer $t$ ($1 \le t \le 100$) — the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \leq n \leq 2 \cdot 10^5$) — the number of frogs, which equals the distance Slavic and Mihai can travel to place a trap.</p><p>The second line of each test case contains $n$ integers $a_1, \ldots, a_n$ ($1 \leq a_i \leq 10^9$) — the lengths of the hops of the corresponding frogs.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case output a single integer&nbsp;— the maximum number of frogs Slavic and Mihai can catch using a trap.</p>





```input1|2,3,6,7,10,11,14,15
7
5
1 2 3 4 5
3
2 2 2
6
3 1 3 4 9 10
9
1 3 2 4 2 3 7 8 5
1
10
8
7 11 6 8 12 4 4 8
10
9 11 9 12 1 7 2 5 8 10
```




```output1
3
3
3
5
0
4
4
```



## Note

<p>In the first test case, the frogs will hop as follows: </p><ul> <li> Frog 1: $0 \to 1 \to 2 \to 3 \to \mathbf{\color{red}{4}} \to \cdots$ </li><li> Frog 2: $0 \to 2 \to \mathbf{\color{red}{4}} \to 6 \to 8 \to \cdots$ </li><li> Frog 3: $0 \to 3 \to 6 \to 9 \to 12 \to \cdots$ </li><li> Frog 4: $0 \to \mathbf{\color{red}{4}} \to 8 \to 12 \to 16 \to \cdots$ </li><li> Frog 5: $0 \to 5 \to 10 \to 15 \to 20 \to \cdots$ </li></ul> Therefore, if Slavic and Mihai put a trap at coordinate $4$, they can catch three frogs: frogs 1, 2, and 4. It can be proven that they can't catch any more frogs.<p>In the second test case, Slavic and Mihai can put a trap at coordinate $2$ and catch all three frogs instantly.</p>
