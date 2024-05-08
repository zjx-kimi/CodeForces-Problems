## Description

<div><p>Christmas was knocking on the door, and our protagonist, Bob, was preparing a spectacular present for his long-time second best friend Charlie. As chocolate boxes are lame, he decided to decorate a tree instead. Bob's tree can be represented as an undirected connected graph with $n$ nodes (numbered $1$ to $n$) and $n-1$ edges. Initially, Bob placed a decoration with label $i$ on node $i$, for each $1 \le i \le n$. However, as such a simple arrangement is lame, he decided to shuffle the decorations a bit. Formally, Bob did the following steps:</p><ul><li> First, he listed the $n-1$ edges in some order.</li><li> Then, he considered the edges one by one in that order. For each edge $(u, v)$, he swapped the decorations of node $u$ with the one of node $v$.</li></ul><p>After finishing, Bob seemed satisfied with the arrangement, so he went to sleep.</p><p>The next morning, Bob wakes up only to find out that his beautiful arrangement has been ruined! Last night, Bob's younger brother Bobo dropped some of the decorations on the floor while he was playing with the tree. Fortunately, no decorations were lost, so Bob can repair the tree in no time. However, he completely forgets how the tree looked like yesterday. Therefore, given the labels of the decorations still on the tree, Bob wants to know the number of possible configurations of the tree. As the result can be quite large, Bob will be happy if you can output the result modulo $1000000007$ ($10^9+7$). Note that, it is possible that there exists no possible configurations.</p></div><div class="input-specification"><p>The first line contains a single integer $n$ ($2 \leq n \leq 500\,000$)&nbsp;— the number of nodes.</p><p>Each of the next $n - 1$ lines contains two integers $u$ and $v$ ($1 \leq u, v \leq n$), denoting that there is an edge connecting two nodes $u$ and $v$. It is guaranteed that the given edges form a tree.</p><p>The last line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($0 \le a_i \le n$). For each $i$, $a_i = 0$ means that the decoration of node $i$ has been dropped on the floor. Otherwise, $a_i$ is the label of the decoration of node $i$. It is guaranteed that no label appears more than once.</p></div><div class="output-specification"><p>Output the number of possible configurations modulo $1000000007$ ($10^9+7$).</p></div>

## Input

<p>The first line contains a single integer $n$ ($2 \leq n \leq 500\,000$)&nbsp;— the number of nodes.</p><p>Each of the next $n - 1$ lines contains two integers $u$ and $v$ ($1 \leq u, v \leq n$), denoting that there is an edge connecting two nodes $u$ and $v$. It is guaranteed that the given edges form a tree.</p><p>The last line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($0 \le a_i \le n$). For each $i$, $a_i = 0$ means that the decoration of node $i$ has been dropped on the floor. Otherwise, $a_i$ is the label of the decoration of node $i$. It is guaranteed that no label appears more than once.</p>

## Output

<p>Output the number of possible configurations modulo $1000000007$ ($10^9+7$).</p>





```input1
4
3 4
2 4
4 1
0 4 0 0
```




```input2
5
1 2
2 4
3 4
5 4
0 0 0 0 0
```




```input3
3
1 2
1 3
1 0 0
```




```output1
2
```




```output2
12
```




```output3
0
```



## Note

<p>In the first example, the possible configurations of the tree are $[2, 4, 1, 3]$ and $[3, 4, 2, 1]$.</p><p>In the second example, note that while there are $4! = 24$ possible permutations of the edges, each of them results in a possible configuration, there are only $12$ different configurations.</p><p>In the third example, it is easy to see that the decoration $1$ cannot stay at node $1$ after the swaps.</p>
