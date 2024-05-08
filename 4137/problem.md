## Description

<div><p>There are $n$ shovels in the nearby shop. The $i$-th shovel costs $a_i$ bourles.</p><p>Misha has to buy <span class="tex-font-style-bf">exactly</span> $k$ shovels. Each shovel can be bought <span class="tex-font-style-bf">no more than once</span>.</p><p>Misha can buy shovels by several purchases. During one purchase he can choose any subset of remaining (non-bought) shovels and buy this subset.</p><p>There are also $m$ special offers in the shop. The $j$-th of them is given as a pair $(x_j, y_j)$, and it means that if Misha buys <span class="tex-font-style-bf">exactly</span> $x_j$ shovels <span class="tex-font-style-bf">during one purchase</span> then $y_j$ <span class="tex-font-style-bf">most cheapest</span> of them are for free (i.e. he will not pay for $y_j$ most cheapest shovels during the current purchase).</p><p>Misha can use any offer any (possibly, zero) number of times, but he cannot use <span class="tex-font-style-bf">more than one</span> offer during <span class="tex-font-style-bf">one purchase</span> (but he can buy shovels without using any offers).</p><p>Your task is to calculate the minimum cost of buying $k$ shovels, if Misha buys them optimally.</p></div><div class="input-specification"><p>The first line of the input contains three integers $n, m$ and $k$ ($1 \le n, m \le 2 \cdot 10^5, 1 \le k \le min(n, 2000)$) — the number of shovels in the shop, the number of special offers and the number of shovels Misha has to buy, correspondingly.</p><p>The second line of the input contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le 2 \cdot 10^5$), where $a_i$ is the cost of the $i$-th shovel.</p><p>The next $m$ lines contain special offers. The $j$-th of them is given as a pair of integers $(x_i, y_i)$ ($1 \le y_i \le x_i \le n$) and means that if Misha buys exactly $x_i$ shovels during some purchase, then he can take $y_i$ most cheapest of them for free.</p></div><div class="output-specification"><p>Print one integer — the minimum cost of buying $k$ shovels if Misha buys them optimally.</p></div>

## Input

<p>The first line of the input contains three integers $n, m$ and $k$ ($1 \le n, m \le 2 \cdot 10^5, 1 \le k \le min(n, 2000)$) — the number of shovels in the shop, the number of special offers and the number of shovels Misha has to buy, correspondingly.</p><p>The second line of the input contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le 2 \cdot 10^5$), where $a_i$ is the cost of the $i$-th shovel.</p><p>The next $m$ lines contain special offers. The $j$-th of them is given as a pair of integers $(x_i, y_i)$ ($1 \le y_i \le x_i \le n$) and means that if Misha buys exactly $x_i$ shovels during some purchase, then he can take $y_i$ most cheapest of them for free.</p>

## Output

<p>Print one integer — the minimum cost of buying $k$ shovels if Misha buys them optimally.</p>





```input1
7 4 5
2 5 4 2 6 3 1
2 1
6 5
2 1
3 1
```




```input2
9 4 8
6 8 5 1 8 1 1 2 1
9 2
8 4
5 3
9 7
```




```input3
5 1 4
2 5 7 4 6
5 4
```




```output1
7
```




```output2
17
```




```output3
17
```



## Note

<p>In the first example Misha can buy shovels on positions $1$ and $4$ (both with costs $2$) during the first purchase and get one of them for free using the first or the third special offer. And then he can buy shovels on positions $3$ and $6$ (with costs $4$ and $3$) during the second purchase and get the second one for free using the first or the third special offer. Then he can buy the shovel on a position $7$ with cost $1$. So the total cost is $4 + 2 + 1 = 7$.</p><p>In the second example Misha can buy shovels on positions $1$, $2$, $3$, $4$ and $8$ (costs are $6$, $8$, $5$, $1$ and $2$) and get three cheapest (with costs $5$, $1$ and $2$) for free. And then he can buy shovels on positions $6$, $7$ and $9$ (all with costs $1$) without using any special offers. So the total cost is $6 + 8 + 1 + 1 + 1 = 17$.</p><p>In the third example Misha can buy four cheapest shovels without using any special offers and get the total cost $17$.</p>
