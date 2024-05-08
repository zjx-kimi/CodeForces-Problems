## Description

<div><p>Alice and Bob are going to celebrate Christmas by playing a game with a tree of presents. The tree has $n$ nodes (numbered $1$ to $n$, with some node $r$ as its root). There are $a_i$ presents are hanging from the $i$-th node.</p><p>Before beginning the game, a special integer $k$ is chosen. The game proceeds as follows:</p><ul><li> Alice begins the game, with moves alternating each turn;</li><li> in any move, the current player may choose some node (for example, $i$) which has depth at least $k$. Then, the player picks some positive number of presents hanging from that node, let's call it $m$ $(1 \le m \le a_i)$;</li><li> the player then places these $m$ presents on the $k$-th ancestor (let's call it $j$) of the $i$-th node (the $k$-th ancestor of vertex $i$ is a vertex $j$ such that $i$ is a descendant of $j$, and the difference between the depth of $j$ and the depth of $i$ is exactly $k$). Now, the number of presents of the $i$-th node $(a_i)$ is decreased by $m$, and, correspondingly, $a_j$ is increased by $m$;</li><li> Alice and Bob both play optimally. The player unable to make a move loses the game.</li></ul><p><span class="tex-font-style-bf">For each possible root</span> of the tree, find who among Alice or Bob wins the game.</p><p>Note: The depth of a node $i$ in a tree with root $r$ is defined as the number of edges on the simple path from node $r$ to node $i$. The depth of root $r$ itself is zero.</p></div><div class="input-specification"><p>The first line contains two space-separated integers $n$ and $k$ $(3 \le n \le 10^5, 1 \le k \le 20)$.</p><p>The next $n-1$ lines each contain two integers $x$ and $y$ $(1 \le x, y \le n, x \neq y)$, denoting an undirected edge between the two nodes $x$ and $y$. These edges form a tree of $n$ nodes.</p><p>The next line contains $n$ space-separated integers denoting the array $a$ $(0 \le a_i \le 10^9)$.</p></div><div class="output-specification"><p>Output $n$ integers, where the $i$-th integer is $1$ if Alice wins the game when the tree is rooted at node $i$, or $0$ otherwise.</p></div>

## Input

<p>The first line contains two space-separated integers $n$ and $k$ $(3 \le n \le 10^5, 1 \le k \le 20)$.</p><p>The next $n-1$ lines each contain two integers $x$ and $y$ $(1 \le x, y \le n, x \neq y)$, denoting an undirected edge between the two nodes $x$ and $y$. These edges form a tree of $n$ nodes.</p><p>The next line contains $n$ space-separated integers denoting the array $a$ $(0 \le a_i \le 10^9)$.</p>

## Output

<p>Output $n$ integers, where the $i$-th integer is $1$ if Alice wins the game when the tree is rooted at node $i$, or $0$ otherwise.</p>





```input1
5 1
1 2
1 3
5 2
4 3
0 3 2 4 4
```




```output1
1 0 0 1 1
```



## Note

<p>Let us calculate the answer for sample input with root node as 1 and as 2.</p><p><span class="tex-font-style-bf">Root node 1</span></p><p>Alice always wins in this case. One possible gameplay between Alice and Bob is:</p><ul> <li> Alice moves one present from node 4 to node 3. </li><li> Bob moves four presents from node 5 to node 2. </li><li> Alice moves four presents from node 2 to node 1. </li><li> Bob moves three presents from node 2 to node 1. </li><li> Alice moves three presents from node 3 to node 1. </li><li> Bob moves three presents from node 4 to node 3. </li><li> Alice moves three presents from node 3 to node 1. </li></ul><p>Bob is now unable to make a move and hence loses.</p><p><span class="tex-font-style-bf">Root node 2</span></p><p>Bob always wins in this case. One such gameplay is:</p><ul> <li> Alice moves four presents from node 4 to node 3. </li><li> Bob moves four presents from node 5 to node 2. </li><li> Alice moves six presents from node 3 to node 1. </li><li> Bob moves six presents from node 1 to node 2. </li></ul><p>Alice is now unable to make a move and hence loses.</p>
