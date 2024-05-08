## Description

<div><p>There is an undirected graph with $n$ vertices and $m$ edges. Initially, for each vertex $i$, there is a monster with danger $a_{i}$ on that vertex. For a monster with danger $a_{i}$, you can defeat it if and only if you have defeated at least $a_{i}$ other monsters before.</p><p>Now you want to defeat all the monsters. First, you choose some vertex $s$ and defeat the monster on that vertex (since you haven't defeated any monsters before, $a_{s}$ has to be $0$). Then, you can move through the edges. If you want to move from vertex $u$ to vertex $v$, then the following must hold: either the monster on vertex $v$ has been defeated before, or you can defeat it now. For the second case, you defeat the monster on vertex $v$ and reach vertex $v$.</p><p>You can pass the vertices and the edges any number of times. Determine whether you can defeat all the monsters or not.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 10^4$) — the number of test cases. Their description follows.</p><p>The first line of each test case contains two integers $n$, $m$ ($1 \le n, m \le 2 \cdot 10^5$) — the number of vertices and edges in the graph respectively. </p><p>The second line of each test case contains $n$ integers $a_{1}, a_{2}, \ldots, a_{n}$ ($0 \le a_{i} \le n$) — the dangers of monsters on corresponding vertices.</p><p>For the following $m$ lines, each line contains two integers $u$, $v$ ($1 \le u, v \le n$), describing an edge connecting vertex $u$ and vertex $v$. It is guaranteed that there are no multi-edges or self-loops in the graph.</p><p>It is guaranteed that both the sum of $n$ and the sum of $m$ over all test cases do not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output "<span class="tex-font-style-tt">YES</span>" if you can defeat all the monsters, or "<span class="tex-font-style-tt">NO</span>" otherwise.</p><p>You can output the answer in any case (upper or lower). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as positive responses.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 10^4$) — the number of test cases. Their description follows.</p><p>The first line of each test case contains two integers $n$, $m$ ($1 \le n, m \le 2 \cdot 10^5$) — the number of vertices and edges in the graph respectively. </p><p>The second line of each test case contains $n$ integers $a_{1}, a_{2}, \ldots, a_{n}$ ($0 \le a_{i} \le n$) — the dangers of monsters on corresponding vertices.</p><p>For the following $m$ lines, each line contains two integers $u$, $v$ ($1 \le u, v \le n$), describing an edge connecting vertex $u$ and vertex $v$. It is guaranteed that there are no multi-edges or self-loops in the graph.</p><p>It is guaranteed that both the sum of $n$ and the sum of $m$ over all test cases do not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output "<span class="tex-font-style-tt">YES</span>" if you can defeat all the monsters, or "<span class="tex-font-style-tt">NO</span>" otherwise.</p><p>You can output the answer in any case (upper or lower). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as positive responses.</p>





```input1|2,3,4,5,6,15,16,17,18,19,28,29,30,31,32,33,34
5
4 3
2 1 0 3
1 2
2 3
3 4
6 6
0 1 2 3 0 1
1 2
2 3
3 4
4 5
4 6
5 6
4 3
0 1 2 0
1 2
2 3
1 3
4 6
1 1 1 0
1 2
3 2
4 3
2 4
4 1
1 3
5 5
0 1 3 2 0
1 2
2 3
3 4
4 5
3 5
```




```output1
YES
YES
NO
YES
NO
```



## Note

<p>In the first test case, you can start at vertex $3$ and defeat the monster on it, before you go to vertices $2$, $1$ in this order, defeating the monsters on them as well. Then you return to vertex $3$, and go to vertex $4$, defeating the monster on it.</p><p>In the third test case, there is no path to vertex $4$ if you start at vertex $1$. Also, there is no path to vertices $1$, $2$, and $3$ if you start at vertex $4$.</p>
