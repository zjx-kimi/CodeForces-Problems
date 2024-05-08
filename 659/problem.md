## Description

<div><p>You are given an undirected graph consisting of $n$ vertices and $n-1$ edges. The $i$-th edge has weight $a_i$; it connects the vertices $i$ and $i+1$.</p><p>Initially, each vertex contains a chip. Each chip has an integer written on it; the integer written on the chip in the $i$-th vertex is $i$.</p><p>In one operation, you can choose a chip (if there are multiple chips in a single vertex, you may choose any one of them) and move it along one of the edges of the graph. The cost of this operation is equal to the weight of the edge.</p><p>The <span class="tex-font-style-it">cost</span> of the graph is the minimum cost of a sequence of such operations that meets the following condition:</p><ul> <li> after all operations are performed, each vertex contains exactly one chip, and the integer on each chip is <span class="tex-font-style-bf">not equal</span> to the index of the vertex where that chip is located. </li></ul><p>You are given $q$ queries of the form:</p><ul> <li> $k$ $x$ — change the weight of the $k$-th edge (the one which connects the vertices $k$ and $k+1$) to $x$. </li></ul><p>After each query, print the <span class="tex-font-style-it">cost</span> of the graph. Note that you don't actually move any chips; when you compute the cost, the chips are on their initial positions.</p></div><div class="input-specification"><p>The first line contains one integer $n$ ($2 \le n \le 2 \cdot 10^5$).</p><p>The second line contains $n-1$ integers $a_1, a_2, \dots, a_{n-1}$ ($1 \le a_i \le 10^9$).</p><p>The third line contains one integer $q$ ($1 \le q \le 2 \cdot 10^5$).</p><p>Then $q$ lines follow. The $i$-th of them contains two integers $k$ and $x$ ($1 \le k \le n-1$; $1 \le x \le 10^9$) for the $i$-th query.</p></div><div class="output-specification"><p>For each query, print one integer — the <span class="tex-font-style-it">cost</span> of the graph after the query is performed.</p></div>

## Input

<p>The first line contains one integer $n$ ($2 \le n \le 2 \cdot 10^5$).</p><p>The second line contains $n-1$ integers $a_1, a_2, \dots, a_{n-1}$ ($1 \le a_i \le 10^9$).</p><p>The third line contains one integer $q$ ($1 \le q \le 2 \cdot 10^5$).</p><p>Then $q$ lines follow. The $i$-th of them contains two integers $k$ and $x$ ($1 \le k \le n-1$; $1 \le x \le 10^9$) for the $i$-th query.</p>

## Output

<p>For each query, print one integer — the <span class="tex-font-style-it">cost</span> of the graph after the query is performed.</p>





```input1
10
12 6 12 15 20 8 17 12 15
8
4 10
7 3
6 14
9 9
2 10
3 5
4 11
7 11
```




```output1
126
108
120
108
112
98
98
114
```


