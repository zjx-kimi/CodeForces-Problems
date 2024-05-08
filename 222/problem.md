## Description

<div><p>You are given an undirected connected graph in which any two distinct simple cycles <span class="tex-font-style-bf">do not have</span> common vertices. Since the graph can be very large, it is given to you in a compressed form: for each edge, you are also given a number $d$, which indicates that there are $d$ additional vertices on this edge.</p><p>You need to assign a weight to each vertex and each edge of the graph&nbsp;— an integer from $1$ to $3$.</p><p>An edge of the graph is called <span class="tex-font-style-it">good</span> if the <a href="https://en.wikipedia.org/wiki/Exclusive_or">bitwise XOR</a> of the weights of its adjacent vertices is <span class="tex-font-style-bf">not equal to</span> $0$ and <span class="tex-font-style-bf">not equal to</span> the weight of that edge.</p><p>Similarly, a vertex of the graph is called <span class="tex-font-style-it">good</span> if the <a href="https://en.wikipedia.org/wiki/Exclusive_or">bitwise XOR</a> of the weights of its adjacent edges is <span class="tex-font-style-bf">not equal to</span> $0$ and <span class="tex-font-style-bf">not equal to</span> the weight of that vertex.</p><p>You need to determine how many ways there are to assign weights to the vertices and edges of the graph so that all vertices and edges are <span class="tex-font-style-it">good</span>. Since the answer can be quite large, you need to calculate the remainder of the answer divided by $998\,244\,353$.</p></div><div class="input-specification"><p>The first line contains two integers $n$ and $m$&nbsp;— the number of vertices and the number of edges in the graph ($2 \le n \le 5 \cdot 10^5$, $n - 1 \le m \le 10^6$).</p><p>Each of the next $m$ lines contains three integers $a_i, b_i$, and $d_i$ ($1 \le a_i, b_i \le n$, $a_i \ne b_i$, $0 \le d_i \le 10^9$), indicating that there is an edge in the graph connecting vertices $a_i$ and $b_i$. Additionally, on this edge, there are $d_i$ additional vertices. It is guaranteed that the given graph is connected, there are no multiple edges, loops, and any two distinct simple cycles of the graph <span class="tex-font-style-bf">do not have</span> common vertices.</p></div><div class="output-specification"><p>Output a single integer&nbsp;— the answer to the problem modulo $998\,244\,353$.</p></div>

## Input

<p>The first line contains two integers $n$ and $m$&nbsp;— the number of vertices and the number of edges in the graph ($2 \le n \le 5 \cdot 10^5$, $n - 1 \le m \le 10^6$).</p><p>Each of the next $m$ lines contains three integers $a_i, b_i$, and $d_i$ ($1 \le a_i, b_i \le n$, $a_i \ne b_i$, $0 \le d_i \le 10^9$), indicating that there is an edge in the graph connecting vertices $a_i$ and $b_i$. Additionally, on this edge, there are $d_i$ additional vertices. It is guaranteed that the given graph is connected, there are no multiple edges, loops, and any two distinct simple cycles of the graph <span class="tex-font-style-bf">do not have</span> common vertices.</p>

## Output

<p>Output a single integer&nbsp;— the answer to the problem modulo $998\,244\,353$.</p>





```input1
3 3
1 2 0
2 3 0
3 1 0
```




```input2
6 7
1 2 0
2 3 0
3 1 0
4 5 0
5 6 0
6 4 0
4 3 0
```




```input3
2 1
2 1 777
```




```input4
3 3
1 2 0
2 3 110850709
3 1 1000000000
```




```output1
12
```




```output2
0
```




```output3
0
```




```output4
179179178
```



## Note

<p>In the first test, the graph is a simple cycle of $3$ vertices. It can be shown, that there are exactly $12$ ways to assign weights, to make all vertexes and edges <span class="tex-font-style-it">good</span>.</p><p>In the second test, the graph has the form of two simple cycles of $3$ vertices connected by an edge. It can be shown that for such a graph there are no ways to arrange weights so that all vertices and edges are <span class="tex-font-style-it">good</span>.</p>
