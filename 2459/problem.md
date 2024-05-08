## Description

<div><p>Let $F_k$ denote the $k$-th term of Fibonacci sequence, defined as below:</p><ul><li> $F_0 = F_1 = 1$</li><li> for any integer $n \geq 0$, $F_{n+2} = F_{n+1} + F_n$</li></ul><p>You are given a tree with $n$ vertices. Recall that a tree is a connected undirected graph without cycles.</p><p>We call a tree a <span class="tex-font-style-bf">Fib-tree</span>, if its number of vertices equals $F_k$ for some $k$, and at least one of the following conditions holds:</p><ul><li> The tree consists of only $1$ vertex;</li><li> You can divide it into two Fib-trees by removing some edge of the tree. </li></ul><p>Determine whether the given tree is a Fib-tree or not.</p></div><div class="input-specification"><p>The first line of the input contains a single integer $n$ ($1 \leq n \leq 2 \cdot 10^5$) — the number of vertices in the tree.</p><p>Then $n-1$ lines follow, each of which contains two integers $u$ and $v$ ($1\leq u,v \leq n$, $u \neq v$), representing an edge between vertices $u$ and $v$. It's guaranteed that given edges form a tree.</p></div><div class="output-specification"><p>Print <span class="tex-font-style-tt">"YES"</span> if the given tree is a Fib-tree, or <span class="tex-font-style-tt">"NO"</span> otherwise.</p><p>You can print your answer in any case. For example, if the answer is "<span class="tex-font-style-tt">YES</span>", then the output "<span class="tex-font-style-tt">Yes</span>" or "<span class="tex-font-style-tt">yeS</span>" will also be considered as correct answer.</p></div>

## Input

<p>The first line of the input contains a single integer $n$ ($1 \leq n \leq 2 \cdot 10^5$) — the number of vertices in the tree.</p><p>Then $n-1$ lines follow, each of which contains two integers $u$ and $v$ ($1\leq u,v \leq n$, $u \neq v$), representing an edge between vertices $u$ and $v$. It's guaranteed that given edges form a tree.</p>

## Output

<p>Print <span class="tex-font-style-tt">"YES"</span> if the given tree is a Fib-tree, or <span class="tex-font-style-tt">"NO"</span> otherwise.</p><p>You can print your answer in any case. For example, if the answer is "<span class="tex-font-style-tt">YES</span>", then the output "<span class="tex-font-style-tt">Yes</span>" or "<span class="tex-font-style-tt">yeS</span>" will also be considered as correct answer.</p>





```input1
3
1 2
2 3
```




```input2
5
1 2
1 3
1 4
1 5
```




```input3
5
1 3
1 2
4 5
3 4
```




```output1
YES
```




```output2
NO
```




```output3
YES
```



## Note

<p>In the first sample, we can cut the edge $(1, 2)$, and the tree will be split into $2$ trees of sizes $1$ and $2$ correspondently. Any tree of size $2$ is a Fib-tree, as it can be split into $2$ trees of size $1$.</p><p>In the second sample, no matter what edge we cut, the tree will be split into $2$ trees of sizes $1$ and $4$. As $4$ isn't $F_k$ for any $k$, it's not Fib-tree.</p><p>In the third sample, here is one possible order of cutting the edges so that all the trees in the process are Fib-trees: $(1, 3), (1, 2), (4, 5), (3, 4)$. </p>
