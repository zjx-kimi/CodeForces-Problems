## Description

<div><p>Doremy lives in a country consisting of $n$ cities numbered from $1$ to $n$, with $a_i$ people living in the $i$-th city. It can be modeled as an undirected graph with $n$ nodes.</p><p>Initially, there are no edges in the graph. Now Doremy wants to make the graph <span class="tex-font-style-it">connected</span>. </p><p>To do this, she can add an edge between $i$ and $j$ if </p><p>$$ \sum_{k \in S} a_k \ge i\cdot j \cdot c, $$</p><p>where $S$ is the set of all the nodes that are currently in the same connected component of either $i$ or $j$, and $c$ is a given constant.</p><p>Can Doremy make the graph connected?</p><p>Two nodes $(i, j)$ are in the same connected component if there exists a path from $i$ to $j$. A graph is connected if all its nodes are in the same connected component.</p></div><div class="input-specification"><p>The input consists of multiple test cases. The first line contains a single integer $t$ ($1\le t\le 10^4$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line contains two integers $n$, $c$ ($2\le n\le 2\cdot 10^5$, $1 \le c \le 10^6$)&nbsp;— the number of nodes and the constant.</p><p>The second line of each test case contains $ n $ integers $ a_1,a_2,\ldots,a_n $ ($0 \le a_i \le 10^{12}$)&nbsp;— the number of people living in the $i$-th city.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2\cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, print "<span class="tex-font-style-tt">YES</span>" (without quotes), if it is possible to make the graph connected, and "<span class="tex-font-style-tt">NO</span>" (without quotes) otherwise.</p><p>You can print letters in any case (upper or lower).</p></div>

## Input

<p>The input consists of multiple test cases. The first line contains a single integer $t$ ($1\le t\le 10^4$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line contains two integers $n$, $c$ ($2\le n\le 2\cdot 10^5$, $1 \le c \le 10^6$)&nbsp;— the number of nodes and the constant.</p><p>The second line of each test case contains $ n $ integers $ a_1,a_2,\ldots,a_n $ ($0 \le a_i \le 10^{12}$)&nbsp;— the number of people living in the $i$-th city.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2\cdot 10^5$.</p>

## Output

<p>For each test case, print "<span class="tex-font-style-tt">YES</span>" (without quotes), if it is possible to make the graph connected, and "<span class="tex-font-style-tt">NO</span>" (without quotes) otherwise.</p><p>You can print letters in any case (upper or lower).</p>





```input1|2,3,6,7,10,11,14,15
7
4 10
0 20 15 10
2 1
1 1
5 1
0 1 0 4 199
5 2
1 1 3 1 1
5 5
5 6 1 10 2
5 1000000
1000000000000 1000000000000 1000000000000 1000000000000 1000000000000
3 1
0 0 2
```




```output1
Yes
Yes
Yes
No
No
Yes
No
```



## Note

<p>In the first test case, Doremy can add edges in the following order:</p><ol> <li> Add $(1,2)$. This operation is valid because $a_1 + a_2 = 20 \ge i\cdot j \cdot c = 20$. </li><li> Add $(1,3)$. This operation is valid because $a_1 + a_2 + a_3 = 35 \ge i \cdot j \cdot c = 30$. </li><li> Add $(1,4)$. This operation is valid because $a_1 + a_2 + a_3 + a_4 = 45 \ge i \cdot j \cdot c = 40$. </li></ol><p>In the second test case, Doremy can add edge $(1,2)$ because $a_1 + a_2 =2 \ge 1 \cdot 2 \cdot 1$. After that, the graph is connected.</p><p>In the third test case, Doremy can add edges in the order $(5,4)$, $(5,3)$, $(5,2)$ and $(5,1)$.</p><p>In the fourth test case, Doremy cannot add any edge at all.</p>
