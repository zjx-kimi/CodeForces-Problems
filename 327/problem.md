## Description

<div><p>Jellyfish loves playing a game called "Inscryption" which is played on a directed acyclic graph with $n$ vertices and $m$ edges. All edges $a \to b$ satisfy $a &lt; b$.</p><p>You need to move from vertex $1$ to vertex $n$ along the directed edges, and then fight with the final boss.</p><p>You will collect <span class="tex-font-style-bf">cards</span> and <span class="tex-font-style-bf">props</span> in the process.</p><p>Each <span class="tex-font-style-bf">card</span> has two attributes: HP and damage. If a <span class="tex-font-style-bf">card's</span> HP is $a$ and its damage is $b$, then the power of the <span class="tex-font-style-bf">card</span> is $a \times b$.</p><p>Each <span class="tex-font-style-bf">prop</span> has only one attribute: power.</p><p>In addition to vertex $1$ and vertex $n$, there are some vertices that trigger special events. The special events are:</p><ol> <li> You will get a <span class="tex-font-style-bf">card</span> with $a$ HP, and $b$ damage. </li><li> If you have at least one <span class="tex-font-style-bf">card</span>, choose one of your <span class="tex-font-style-bf">cards</span> and increase its HP by $x$. </li><li> If you have at least one <span class="tex-font-style-bf">card</span>, choose one of your <span class="tex-font-style-bf">cards</span> and increase its damage by $y$. </li><li> You will get a <span class="tex-font-style-bf">prop</span> with $w$ power. </li></ol><p>When you get to vertex $n$, you can choose <span class="tex-font-style-bf">at most one</span> of your <span class="tex-font-style-bf">cards</span> and multiply its damage by $10^9$.</p><p>The final boss is very strong, so you want to maximize the sum of the power of all your <span class="tex-font-style-bf">cards</span> and <span class="tex-font-style-bf">props</span>. Find the maximum possible sum of power of all your <span class="tex-font-style-bf">cards</span> and <span class="tex-font-style-bf">props</span> if you play the game optimally.</p></div><div class="input-specification"><p>The first line contains two integers $n$ and $m$ ($2 \leq n \leq 200$, $n - 1\leq m \leq \min(\frac{n(n-1)}2, 2000)$)&nbsp;— the number of the vertices and the number of the edges.</p><p>In the following $n$ lines, the $i$-th $(1 \leq i \leq n)$ line describes the special event that will trigger on vertex $i$:</p><ul> <li> <span class="tex-font-style-tt">0</span>&nbsp;— no special events. </li><li> <span class="tex-font-style-tt">1 a b</span> ($1 \leq a, b \leq 200$)&nbsp;— you will get a card with $a$ HP, and $b$ damage. </li><li> <span class="tex-font-style-tt">2 x</span> ($1 \leq x \leq 200$)&nbsp;— if you have at least one card, choose one of your cards and increase its HP by $x$. </li><li> <span class="tex-font-style-tt">3 y</span> ($1 \leq y \leq 200$)&nbsp;— if you have at least one card, choose one of your cards and increase its damage by $y$. </li><li> <span class="tex-font-style-tt">4 w</span> ($1 \leq w \leq 10^6$)&nbsp;— you will get a prop with $w$ power. </li></ul><p>In the following $m$ lines, each line contains two integers $u$ and $v$ ($1 \leq u &lt; v \leq n$) representing a directed edge from vertex $u$ to vertex $v$.</p><p>It is guaranteed that every edge $(u,v)$ appears at most once.</p><p>It is guaranteed that there are no special events on vertex $1$ and vertex $n$.</p><p>It is guaranteed that for all $i$, there exists a path from vertex $1$ to vertex $n$ that passes through vertex $i$.</p></div><div class="output-specification"><p>Output a single integer&nbsp;— the maximum sum of the power of all your cards and props.</p></div>

## Input

<p>The first line contains two integers $n$ and $m$ ($2 \leq n \leq 200$, $n - 1\leq m \leq \min(\frac{n(n-1)}2, 2000)$)&nbsp;— the number of the vertices and the number of the edges.</p><p>In the following $n$ lines, the $i$-th $(1 \leq i \leq n)$ line describes the special event that will trigger on vertex $i$:</p><ul> <li> <span class="tex-font-style-tt">0</span>&nbsp;— no special events. </li><li> <span class="tex-font-style-tt">1 a b</span> ($1 \leq a, b \leq 200$)&nbsp;— you will get a card with $a$ HP, and $b$ damage. </li><li> <span class="tex-font-style-tt">2 x</span> ($1 \leq x \leq 200$)&nbsp;— if you have at least one card, choose one of your cards and increase its HP by $x$. </li><li> <span class="tex-font-style-tt">3 y</span> ($1 \leq y \leq 200$)&nbsp;— if you have at least one card, choose one of your cards and increase its damage by $y$. </li><li> <span class="tex-font-style-tt">4 w</span> ($1 \leq w \leq 10^6$)&nbsp;— you will get a prop with $w$ power. </li></ul><p>In the following $m$ lines, each line contains two integers $u$ and $v$ ($1 \leq u &lt; v \leq n$) representing a directed edge from vertex $u$ to vertex $v$.</p><p>It is guaranteed that every edge $(u,v)$ appears at most once.</p><p>It is guaranteed that there are no special events on vertex $1$ and vertex $n$.</p><p>It is guaranteed that for all $i$, there exists a path from vertex $1$ to vertex $n$ that passes through vertex $i$.</p>

## Output

<p>Output a single integer&nbsp;— the maximum sum of the power of all your cards and props.</p>





```input1
6 8
0
1 2 10
1 6 6
2 8
3 10
0
1 2
1 3
2 4
2 5
3 4
3 5
4 6
5 6
```




```input2
4 3
0
4 1000000
4 1000000
0
1 2
2 3
3 4
```




```input3
16 15
0
1 1 10
1 10 1
2 4
3 4
1 20 20
2 30
3 20
1 1 100
2 9
1 1 200
2 9
3 10
1 190 100
2 10
0
1 2
2 3
3 4
4 5
5 6
6 7
7 8
8 9
9 10
10 11
11 12
12 13
13 14
14 15
15 16
```




```input4
9 9
0
1 1 200
3 200
3 200
3 200
3 200
1 200 200
3 200
0
1 2
2 3
3 4
4 5
5 6
6 7
7 8
8 9
1 9
```




```input5
9 8
0
1 20 200
3 200
3 200
2 5
1 100 200
3 200
3 200
0
1 2
2 3
3 4
4 5
5 6
6 7
7 8
8 9
```




```input6
16 34
0
0
0
2 6
3 1
4 27
4 40
3 9
0
2 6
1 8 1
0
2 2
1 10 7
2 9
0
2 4
3 10
2 11
2 7
13 15
3 15
2 3
6 14
4 12
10 12
9 10
7 8
4 13
11 12
4 6
11 16
14 15
2 5
5 15
9 13
8 14
1 3
2 15
12 16
7 10
4 5
1 2
4 11
4 9
4 16
3 6
6 8
7 11
15 16
```




```output1
100000000000
```




```output2
2000000
```




```output3
20000000005600
```




```output4
80000000001000
```




```output5
60000000015000
```




```output6
133000000040
```



## Note

<p>In the first example, we will play the game in the following order:</p><ul> <li> move from vertex $1$ to vertex $2$, get a card with $2$ HP, and $10$ damage. </li><li> move from vertex $2$ to vertex $4$, choose the card we get from vertex $2$ and increase its HP by $8$. </li><li> move from vertex $4$ to vertex $6$, choose the card we get from vertex $2$ and multiply its damage by $10^9$. </li></ul><p>In the end, we will have a card with $(2+8)=10$ HP and $10 \times 10^9=10^{10}$ damage, It's power is $10 \times 10^{10}=10^{11}$. Because we only have the card we get from vertex $2$, so the sum of power of all your cards and props is $10^{11}$.</p>
