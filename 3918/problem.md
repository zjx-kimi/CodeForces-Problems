## Description

<div><p>We have a magic tree: a rooted tree on $n$ vertices. The vertices are numbered $1$ through $n$. Vertex $1$ is the root.</p><p>The magic tree gives us magic fruit. The fruit only grows in vertices of the tree other than the root. Each vertex contains at most one piece of fruit.</p><p>It is now day 0 and no fruit is ripe yet. Each fruit will only be ripe for a single day. For each fruit, we are given the vertex $v_j$ where it grows, the day $d_j$ on which it will be ripe, and the amount $w_j$ of magic juice we can extract from it if we harvest it when it is ripe.</p><p>The fruits have to be harvested by cutting some branches of the tree. On each day, you may cut as many branches of the tree as you like. The parts of the tree you cut off will fall to the ground and you can collect all the ripe fruits they contain. All fruits that fall to the ground when they are not ripe are discarded and no magic juice is collected from them.</p><p>Formally, on each day, you may erase some edges of the tree. Whenever you do so, the tree will split into multiple connected components. You then erase all components that do not contain the root and you harvest all ripe fruits those components contained.</p><p>Given is a description of the tree together with the locations, ripening days and juiciness of all $m$ fruits. Calculate the maximum total amount of magic juice we can harvest from the tree.</p></div><div class="input-specification"><p>The first line contains three space-separated integers $n$ ($2 \le n \le 100,000$), $m$ ($1 \le m \le n-1$) and $k$ ($1 \le k \le 100,000$) – the number of vertices, the number of fruits, and the maximum day on which a fruit may become ripe.</p><p>The following $n-1$ lines contain the integers $p_2, \dots, p_n$, one per line. For each $i$ (from $2$ to $n$, inclusive), vertex $p_i$ ($1 \leq p_i \le i-1$) is the parent of vertex $i$.</p><p>Each of the last $m$ lines describes one fruit. The $j$-th of these lines has the form "$v_j\ d_j\ w_j$" ($2 \le v_j \le n$, $1 \le d_j \le k$, $1 \le w_j \le 10^9$).</p><p>It is guaranteed that no vertex contains more than one fruit (i.e., the values $v_j$ are distinct).</p></div><div class="output-specification"><p>Output a single line with a single integer, the maximum amount of magic juice we can harvest from the tree.</p></div><div><h2>Scoring</h2><p>Subtask 1 (6 points): $n, k \leq 20$, and $w_j = 1$ for all $j$</p><p>Subtask 2 (3 points): fruits only grow in the leaves of the tree</p><p>Subtask 3 (11 points): $p_i = i-1$ for each $i$, and $w_j = 1$ for all $j$</p><p>Subtask 4 (12 points): $k \leq 2$</p><p>Subtask 5 (16 points): $k \leq 20$, and $w_j = 1$ for all $j$</p><p>Subtask 6 (13 points): $m \leq 1,000$</p><p>Subtask 7 (22 points): $w_j = 1$ for all $j$</p><p>Subtask 8 (17 points): no additional constraints</p></div>

## Input

<p>The first line contains three space-separated integers $n$ ($2 \le n \le 100,000$), $m$ ($1 \le m \le n-1$) and $k$ ($1 \le k \le 100,000$) – the number of vertices, the number of fruits, and the maximum day on which a fruit may become ripe.</p><p>The following $n-1$ lines contain the integers $p_2, \dots, p_n$, one per line. For each $i$ (from $2$ to $n$, inclusive), vertex $p_i$ ($1 \leq p_i \le i-1$) is the parent of vertex $i$.</p><p>Each of the last $m$ lines describes one fruit. The $j$-th of these lines has the form "$v_j\ d_j\ w_j$" ($2 \le v_j \le n$, $1 \le d_j \le k$, $1 \le w_j \le 10^9$).</p><p>It is guaranteed that no vertex contains more than one fruit (i.e., the values $v_j$ are distinct).</p>

## Output

<p>Output a single line with a single integer, the maximum amount of magic juice we can harvest from the tree.</p>





```input1
6 4 10
1
2
1
4
4
3 4 5
4 7 2
5 4 1
6 9 3
```




```output1
9
```



## Note

<p>In the example input, one optimal solution looks as follows: </p><ul> <li> On day 4, cut the edge between vertices 4 and 5 and harvest a ripe fruit with 1 unit of magic juice. On the same day, cut the edge between vertices 1 and 2 and harvest 5 units of magic juice from the ripe fruit in vertex 3. </li><li> On day 7, do nothing. (We could harvest the fruit in vertex 4 that just became ripe, but doing so is not optimal.) </li><li> On day 9, cut the edge between vertices 1 and 4. Discard the fruit in vertex 4 that is no longer ripe, and harvest 3 units of magic juice from the ripe fruit in vertex 6. (Alternately, we could achieve the same effect by cutting the edge between vertices 4 and 6.) </li></ul>
