## Description

<div><p>There are $n$ players, numbered from $1$ to $n$ sitting around a round table. The $(i+1)$-th player sits to the right of the $i$-th player for $1 \le i &lt; n$, and the $1$-st player sits to the right of the $n$-th player.</p><p>There are $n^2$ cards, each of which has an integer between $1$ and $n$ written on it. For each integer from $1$ to $n$, there are exactly $n$ cards having this number.</p><p>Initially, all these cards are distributed among all the players, in such a way that each of them has exactly $n$ cards. In one operation, each player chooses one of his cards and passes it to the player to his right. All these actions are performed <span class="tex-font-style-bf">simultaneously</span>. </p><p>Player $i$ is called <span class="tex-font-style-it">solid</span> if all his cards have the integer $i$ written on them. Their objective is to reach a configuration in which everyone is solid. Find a way to do it using at most $(n^2-n)$ operations. You do <span class="tex-font-style-bf">not</span> need to minimize the number of operations.</p></div><div class="input-specification"><p>The first line contains a single integer $n$ ($2\le n\le 100$).</p><p>Then $n$ lines follow. The $i$-th of them contains $n$ integers $c_1, c_2, \ldots, c_n$ ($1\le c_j\le n$)&nbsp;— the initial cards of the $i$-th player.</p><p>It is guaranteed that for each integer $i$ from $1$ to $n$, there are exactly $n$ cards having the number $i$.</p></div><div class="output-specification"><p>In the first line print an integer $k$ ($0\le k\le (n^2-n)$)&nbsp;— the numbers of operations you want to make.</p><p>Then $k$ lines should follow. In the $i$-th of them print $n$ integers $d_1, d_2, \ldots, d_n$ ($1\le d_j\le n$) where $d_j$ is the number written on the card which $j$-th player passes to the player to his right in the $i$-th operation.</p><p>We can show that an answer always exists under the given constraints. If there are multiple answers, print any.</p></div>

## Input

<p>The first line contains a single integer $n$ ($2\le n\le 100$).</p><p>Then $n$ lines follow. The $i$-th of them contains $n$ integers $c_1, c_2, \ldots, c_n$ ($1\le c_j\le n$)&nbsp;— the initial cards of the $i$-th player.</p><p>It is guaranteed that for each integer $i$ from $1$ to $n$, there are exactly $n$ cards having the number $i$.</p>

## Output

<p>In the first line print an integer $k$ ($0\le k\le (n^2-n)$)&nbsp;— the numbers of operations you want to make.</p><p>Then $k$ lines should follow. In the $i$-th of them print $n$ integers $d_1, d_2, \ldots, d_n$ ($1\le d_j\le n$) where $d_j$ is the number written on the card which $j$-th player passes to the player to his right in the $i$-th operation.</p><p>We can show that an answer always exists under the given constraints. If there are multiple answers, print any.</p>





```input1
2
2 1
1 2
```




```input2
3
1 1 1
2 2 2
3 3 3
```




```output1
1
2 1
```




```output2
6
1 2 3
3 1 2
2 3 1
1 2 3
3 1 2
2 3 1
```



## Note

<p>In the first test case, if the first player passes a card with number $2$ and the second player passes a card with number $1$, then the first player has two cards with number $1$ and the second player has two cards with number $2$. Then, after making this operation, both players are solid.</p><p>In the second test case, $0$ operations would be enough too. Note that you do not need to minimize the number of operations. </p>
