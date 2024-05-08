## Description

<div><p>Lunchbox has a tree of size $n$ rooted at node $1$. Each node is then assigned a value. Lunchbox considers the tree to be beautiful if each value is distinct and ranges from $1$ to $n$. In addition, a beautiful tree must also satisfy $m$ requirements of $2$ types:</p><ul> <li> "<span class="tex-font-style-tt">1 a b c</span>"&nbsp;— The node with the smallest value on the path between nodes $a$ and $b$ must be located at $c$. </li><li> "<span class="tex-font-style-tt">2 a b c</span>"&nbsp;— The node with the largest value on the path between nodes $a$ and $b$ must be located at $c$. </li></ul><p>Now, you must assign values to each node such that the resulting tree is beautiful. If it is impossible to do so, output $-1$.</p></div><div class="input-specification"><p>The first line contains two integers $n$ and $m$ ($2 \le n, m \le 2 \cdot 10^5$).</p><p>The next $n - 1$ lines contain two integers $u$ and $v$ ($1 \le u, v \le n, u \ne v$)&nbsp;— denoting an edge between nodes $u$ and $v$. It is guaranteed that the given edges form a tree.</p><p>The next $m$ lines each contain four integers $t$, $a$, $b$, and $c$ ($t \in \{1,2\}$, $1 \le a, b, c \le n$). It is guaranteed that node $c$ is on the path between nodes $a$ and $b$.</p></div><div class="output-specification"><p>If it is impossible to assign values such that the tree is beautiful, output $-1$. Otherwise, output $n$ integers, the $i$-th of which denotes the value of node $i$.</p></div>

## Input

<p>The first line contains two integers $n$ and $m$ ($2 \le n, m \le 2 \cdot 10^5$).</p><p>The next $n - 1$ lines contain two integers $u$ and $v$ ($1 \le u, v \le n, u \ne v$)&nbsp;— denoting an edge between nodes $u$ and $v$. It is guaranteed that the given edges form a tree.</p><p>The next $m$ lines each contain four integers $t$, $a$, $b$, and $c$ ($t \in \{1,2\}$, $1 \le a, b, c \le n$). It is guaranteed that node $c$ is on the path between nodes $a$ and $b$.</p>

## Output

<p>If it is impossible to assign values such that the tree is beautiful, output $-1$. Otherwise, output $n$ integers, the $i$-th of which denotes the value of node $i$.</p>





```input1
7 5
1 2
1 3
1 4
3 5
4 6
3 7
1 6 5 1
2 6 7 3
1 2 7 1
1 7 5 7
2 4 2 2
```




```input2
2 2
1 2
1 1 2 1
1 1 2 2
```




```output1
1 6 7 5 3 4 2
```




```output2
-1
```


