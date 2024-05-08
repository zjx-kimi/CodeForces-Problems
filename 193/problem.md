## Description

<div><p><span class="tex-font-style-it">Tree</span> is a connected graph without cycles. It can be shown that any tree of $n$ vertices has exactly $n - 1$ edges.</p><p><span class="tex-font-style-it">Leaf</span> is a vertex in the tree with exactly one edge connected to it.</p><p><span class="tex-font-style-it">Distance</span> between two vertices $u$ and $v$ in a tree is the minimum number of edges that must be passed to come from vertex $u$ to vertex $v$.</p><p>Alex's birthday is coming up, and Timofey would like to gift him a tree of $n$ vertices. However, Alex is a very moody boy. Every day for $q$ days, he will choose an integer, denoted by the integer chosen on the $i$-th day by $d_i$. If on the $i$-th day there are not two leaves in the tree at a distance <span class="tex-font-style-bf">exactly</span> $d_i$, Alex will be <span class="tex-font-style-it">disappointed</span>.</p><p>Timofey decides to gift Alex a designer so that he can change his tree as he wants. Timofey knows that Alex is also lazy (a disaster, not a human being), so at the beginning of every day, he can perform <span class="tex-font-style-bf">no more</span> than one operation of the following kind:</p><ul><li> Choose vertices $u$, $v_1$, and $v_2$ such that there is an edge between $u$ and $v_1$ and no edge between $u$ and $v_2$. Then remove the edge between $u$ and $v_1$ and add an edge between $u$ and $v_2$. This operation <span class="tex-font-style-bf">cannot</span> be performed if the graph is no longer a tree after it.</li></ul><p>Somehow Timofey managed to find out all the $d_i$. After that, he had another brilliant idea&nbsp;— just in case, make an instruction manual for the set, one that Alex wouldn't be <span class="tex-font-style-it">disappointed</span>.</p><p>Timofey is not as lazy as Alex, but when he saw the integer $n$, he quickly lost the desire to develop the instruction and the original tree, so he assigned this task to you. It can be shown that a tree and a sequence of operations satisfying the described conditions always exist.</p><p><img class="tex-graphics" src="file://Rsj4qwSK.png" style="max-width: 100.0%;max-height: 100.0%;"></p><p>Here is an example of an operation where vertices were selected: $u$&nbsp;— $6$, $v_1$&nbsp;— $1$, $v_2$&nbsp;— $4$.</p></div><div class="input-specification"><p>The first line contains the integer $t$ ($1 \leq t \leq 100$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains two integers $n$ ($3 \leq n \leq 500$) and $q$ ($1 \leq q \leq 500$)&nbsp;— the number of nodes in the tree and the number of days, respectively.</p><p>The $i$th of the following $q$ lines contains the integer $d_i$ ($2 \leq d_i \leq n - 1$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $500$. The same is guaranteed for $q$.</p><p>It can be shown that a tree and a sequence of operations satisfying the described conditions always exist.</p></div><div class="output-specification"><p>For each test case, first print an $n - 1$ string describing the edges of the tree. If you want the tree to have an edge between nodes $u$ and $v$, there must be a string $v$ $u$ or $u$ $v$ among these $n - 1$ lines.</p><p>In the next $q$ lines, print three integers each $u$ $v_1$ $v_2$&nbsp;— a description of the operations. If Alex doesn't need to perform an operation the following day, print $-1$ $-1$ $-1$.</p></div>

## Input

<p>The first line contains the integer $t$ ($1 \leq t \leq 100$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains two integers $n$ ($3 \leq n \leq 500$) and $q$ ($1 \leq q \leq 500$)&nbsp;— the number of nodes in the tree and the number of days, respectively.</p><p>The $i$th of the following $q$ lines contains the integer $d_i$ ($2 \leq d_i \leq n - 1$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $500$. The same is guaranteed for $q$.</p><p>It can be shown that a tree and a sequence of operations satisfying the described conditions always exist.</p>

## Output

<p>For each test case, first print an $n - 1$ string describing the edges of the tree. If you want the tree to have an edge between nodes $u$ and $v$, there must be a string $v$ $u$ or $u$ $v$ among these $n - 1$ lines.</p><p>In the next $q$ lines, print three integers each $u$ $v_1$ $v_2$&nbsp;— a description of the operations. If Alex doesn't need to perform an operation the following day, print $-1$ $-1$ $-1$.</p>





```input1|2,3,4,5,13,14,15,16,17,18,19,20,21,22
3
3 3
2
2
2
5 6
4
2
3
4
3
2
4 9
2
3
3
2
2
2
3
2
2
```




```output1
1 2
2 3
-1 -1 -1
-1 -1 -1
-1 -1 -1
1 2
2 3
3 4
4 5
-1 -1 -1
4 3 2
5 4 3
4 2 5
4 5 2
5 3 4
1 2
2 3
3 4
4 3 2
4 2 3
-1 -1 -1
4 3 2
-1 -1 -1
-1 -1 -1
4 2 3
4 3 2
-1 -1 -1
```


