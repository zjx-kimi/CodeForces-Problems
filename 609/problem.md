## Description

<div><p>LuoTianyi is watching the anime <span class="tex-font-style-it">Made in Abyss</span>. She finds that making a Cartridge is interesting. To describe the process of making a Cartridge more clearly, she abstracts the original problem and gives you the following problem.</p><p>You are given a tree $T$ consisting of $n$ vertices. Each vertex has values $a_i$ and $b_i$ and each edge has values $c_j$ and $d_j$.</p><p>Now you are aim to build a <span class="tex-font-style-bf">tree</span> $T'$ as follows:</p><ul> <li> First, select $p$ vertices from $T$ ($p$ is a number chosen by yourself) as the vertex set $S'$ of $T'$. </li><li> Next, select $p-1$ edges from $T$ one by one (you cannot select one edge more than once). </li><li> May you have chosen the $j$-th edge connects vertices $x_j$ and $y_j$ with values $(c_j,d_j)$, then you can choose two vertices $u$ and $v$ in $S'$ that satisfy the edge $(x_j,y_j)$ is contained in the simple path from $u$ to $v$ in $T$, and link $u$ and $v$ in $T'$ by the edge with values $(c_j,d_j)$ ($u$ and $v$ shouldn't be contained in one connected component before in $T'$). </li></ul><center> <img class="tex-graphics" src="file://n4IMOEW2.png" style="max-width: 100.0%;max-height: 100.0%;">   <span class="tex-font-size-small">A tree with three vertices, $\min(A,C)=1,B+D=7$, the cost is $7$.</span> </center><center> <img class="tex-graphics" src="file://4jXJmma3.png" style="max-width: 100.0%;max-height: 100.0%;">   <span class="tex-font-size-small">Selected vertices $2$ and $3$ as $S'$, used the edge $(1,2)$ with $c_j = 2$ and $d_j = 1$ to link this vertices, now $\min(A,C)=2,B+D=4$, the cost is $8$.</span> </center><p>Let $A$ be the minimum of values $a_i$ in $T'$ and $C$ be the minimum of values $c_i$ in $T'$. Let $B$ be the sum of $b_i$ in $T'$ and $D$ be the sum of values $d_i$ in $T'$. Let $\min(A, C) \cdot (B + D)$ be the <span class="tex-font-style-it">cost</span> of $T'$. You need to find the maximum possible cost of $T'$.</p></div><div class="input-specification"><p>The first line contains one integer $n$ ($3\le n \le 2\cdot 10^5$) — the number of vertices in the tree $T$.</p><p>The second line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1\le a_i\le 2\cdot 10^5$), where the $i$-th integer represents the $a_i$ value of the $i$-th vertex.</p><p>The third line contains $n$ integers $b_1, b_2, \ldots, b_n$ ($1\le b_i\le 2\cdot 10^5$), where the $i$-th integer represents the $b_i$ value of the $i$-th vertex.</p><p>Then $n-1$ lines follow, the $j$-th of them contains four integers $x_j,y_j,c_j,d_j$ ($1\le x_j,y_j\le n,1\le c_j,d_j\le 2\cdot 10^5$) representing the edge $(x_j,y_j)$ and its values $c_j$ and $d_j$ respectively. It's guaranteed that edges form a tree.</p></div><div class="output-specification"><p>Print a single integer — the maximum possible cost of $T'$.</p></div>

## Input

<p>The first line contains one integer $n$ ($3\le n \le 2\cdot 10^5$) — the number of vertices in the tree $T$.</p><p>The second line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1\le a_i\le 2\cdot 10^5$), where the $i$-th integer represents the $a_i$ value of the $i$-th vertex.</p><p>The third line contains $n$ integers $b_1, b_2, \ldots, b_n$ ($1\le b_i\le 2\cdot 10^5$), where the $i$-th integer represents the $b_i$ value of the $i$-th vertex.</p><p>Then $n-1$ lines follow, the $j$-th of them contains four integers $x_j,y_j,c_j,d_j$ ($1\le x_j,y_j\le n,1\le c_j,d_j\le 2\cdot 10^5$) representing the edge $(x_j,y_j)$ and its values $c_j$ and $d_j$ respectively. It's guaranteed that edges form a tree.</p>

## Output

<p>Print a single integer — the maximum possible cost of $T'$.</p>





```input1
3
1 2 2
1 1 2
1 2 2 1
1 3 1 2
```




```input2
5
2 4 2 1 1
2 4 4 4 4
2 5 3 3
3 5 2 4
4 2 5 5
5 1 1 5
```




```input3
6
5 7 10 7 9 4
6 9 7 9 8 5
2 1 5 1
3 2 2 4
4 3 6 3
5 1 7 4
6 5 6 8
```




```input4
5
1000 1000 1 1000 1000
1000 1000 1 1000 1000
1 2 1 1
2 3 1000 1000
3 4 1000 1000
3 5 1000 1000
```




```output1
8
```




```output2
35
```




```output3
216
```




```output4
7000000
```



## Note

<p>The tree from the first example is shown in the statement.</p><p>The tree from the second example is shown below:</p><center> <img class="tex-graphics" src="file://r7rTsCtM.png" style="max-width: 100.0%;max-height: 100.0%;"> </center><p>$A = 1, B = 18, C = 1, D = 17$, so the cost is $\min(1,1) \cdot (18 + 17) = 35$.</p>
