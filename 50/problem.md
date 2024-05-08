## Description

<div><p>In TreeWorld, there is a popular two-player game played on a tree with $n$ vertices labelled from $1$ to $n$. In this game, the tournament leaders first choose a vertex to be the root of the tree and choose another vertex (possibly the same vertex as the root) to place a coin on. Then, each player will take turns moving the coin to any child$^\dagger$ of the vertex that the coin is currently on. The first player who is unable to make a move loses.</p><p>Alice wants to be a tree LGM, so she spends a lot of time studying the game. She wrote down an $n$ by $n$ matrix $s$, where $s_{i,j} = \mathtt{1}$ if the first player can win with the root of the tree chosen to be vertex $i$, and the coin was initially placed on vertex $j$. Otherwise, $s_{i, j} = \mathtt{0}$. Alice is a perfectionist, so she assumes that both players play perfectly in the game.</p><p>However, she accidentally knocked her head on the way to the tournament and forgot what the tree looked like. Determine whether there exists a tree that satisfies the winning and losing states represented by matrix $s$, and if it exists, construct a valid tree.</p><p>$^\dagger$ A vertex $c$ is a child of vertex $u$ if there is an edge between $c$ and $u$, and $c$ does not lie on the unique simple path from the root to vertex $u$.</p></div><div class="input-specification"><p>The first line contains a single integer $n$ ($1 \le n \le 5000$)&nbsp;— the number of vertices in the tree.</p><p>Each of the next $n$ lines contains a string with $n$ characters, the $j$-th character of the $i$-th line representing $s_{i, j}$ ($s_{i, j} \in \{\mathtt{0}, \mathtt{1}\}$)&nbsp;— the winning and losing states of the tree.</p></div><div class="output-specification"><p>If there is no tree satisfying the winning and losing states represented by matrix $s$, print a single line containing "<span class="tex-font-style-tt">NO</span>".</p><p>Otherwise, if there exists a tree satisfying matrix $s$, print "<span class="tex-font-style-tt">YES</span>" on the first line, followed by $n - 1$ lines each containing two integers $u$ and $v$ ($1 \le u, v \le n$) representing that the tree has an edge between vertices $u$ and $v$.</p><p>You can output the answer in any case (upper or lower). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as positive responses.</p><p>If there are multiple trees satisfying the winning and losing states represented by matrix $s$, print any of them.</p></div>

## Input

<p>The first line contains a single integer $n$ ($1 \le n \le 5000$)&nbsp;— the number of vertices in the tree.</p><p>Each of the next $n$ lines contains a string with $n$ characters, the $j$-th character of the $i$-th line representing $s_{i, j}$ ($s_{i, j} \in \{\mathtt{0}, \mathtt{1}\}$)&nbsp;— the winning and losing states of the tree.</p>

## Output

<p>If there is no tree satisfying the winning and losing states represented by matrix $s$, print a single line containing "<span class="tex-font-style-tt">NO</span>".</p><p>Otherwise, if there exists a tree satisfying matrix $s$, print "<span class="tex-font-style-tt">YES</span>" on the first line, followed by $n - 1$ lines each containing two integers $u$ and $v$ ($1 \le u, v \le n$) representing that the tree has an edge between vertices $u$ and $v$.</p><p>You can output the answer in any case (upper or lower). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as positive responses.</p><p>If there are multiple trees satisfying the winning and losing states represented by matrix $s$, print any of them.</p>





```input1|
4
1100
0101
0011
0101
```




```input2|
3
001
010
100
```




```output1
YES
4 1
3 2
2 4
```




```output2
NO
```



## Note

<p>In the first test case, the line graph $1\!-\!4\!-\!2\!-\!3$ satisfies the winning and losing states represented by matrix $s$. For example, $s_{3,3} = 1$ as the first player can move the coin from $3\rightarrow 2$, then the second player moves the coin from $2\rightarrow 4$, and finally, the first player moves the coin from $4\rightarrow 1$. At this point, $1$ has no children, so the second player is unable to make a move and loses. On the other hand, $s_{1,3} = 0$ as if $1$ is the root, then $3$ has no children so the first player is unable to make the first move and loses.</p><p>In the second test case, it is possible to prove that no tree satisfies the winning and losing states represented by matrix $s$.</p>
