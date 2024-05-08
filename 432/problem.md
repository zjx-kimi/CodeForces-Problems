## Description

<div><p>Given two arrays $a$ and $b$, both of length $n$. Elements of both arrays indexed from $1$ to $n$. You are constructing a directed graph, where edge from $u$ to $v$ ($u\neq v$) exists if $a_u-a_v \ge b_u-b_v$.</p><p>A vertex $V$ is called strong if there exists a path from $V$ to all other vertices.</p><p>A path in a directed graph is a chain of several vertices, connected by edges, such that moving from the vertex $u$, along the directions of the edges, the vertex $v$ can be reached.</p><p>Your task is to find all strong vertices.</p><p>For example, if $a=[3,1,2,4]$ and $b=[4,3,2,1]$, the graph will look like this: </p><center> <img class="tex-graphics" src="file://sij6NFxT.png" style="max-width: 100.0%;max-height: 100.0%;">   <span class="tex-font-size-small">The graph has only one strong vertex with number $4$</span> </center></div><div class="input-specification"><p>The first line contains an integer $t$ ($1\le t\le 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains an integer $n$ ($2 \le n \le 2\cdot 10^5$)&nbsp;— the length of $a$ and $b$.</p><p>The second line of each test case contains $n$ integers $a_1,a_2 \dots a_n$ ($-10^9 \le a_i \le 10^9$)&nbsp;— the array $a$.</p><p>The third line of each test case contains $n$ integers $b_1,b_2 \dots b_n$ ($-10^9 \le b_i \le 10^9$)&nbsp;— the array $b$.</p><p>It is guaranteed that the sum of $n$ for all test cases does not exceed $2\cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output two lines: in the first line, output the number of strong vertices, and in the second line, output all strong vertices <span class="tex-font-style-bf">in ascending order</span>.</p></div>

## Input

<p>The first line contains an integer $t$ ($1\le t\le 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains an integer $n$ ($2 \le n \le 2\cdot 10^5$)&nbsp;— the length of $a$ and $b$.</p><p>The second line of each test case contains $n$ integers $a_1,a_2 \dots a_n$ ($-10^9 \le a_i \le 10^9$)&nbsp;— the array $a$.</p><p>The third line of each test case contains $n$ integers $b_1,b_2 \dots b_n$ ($-10^9 \le b_i \le 10^9$)&nbsp;— the array $b$.</p><p>It is guaranteed that the sum of $n$ for all test cases does not exceed $2\cdot 10^5$.</p>

## Output

<p>For each test case, output two lines: in the first line, output the number of strong vertices, and in the second line, output all strong vertices <span class="tex-font-style-bf">in ascending order</span>.</p>





```input1|2,3,4,8,9,10,14,15,16
5
4
3 1 2 4
4 3 2 1
5
1 2 4 1 2
5 2 3 3 1
2
1 2
2 1
3
0 2 1
1 3 2
3
5 7 4
-2 -3 -6
```




```output1
1
4 
2
3 5 
1
2 
3
1 2 3 
2
2 3
```



## Note

<p>The first sample is covered in the problem statement.</p><p>For the second sample, the graph looks like this: </p><center> <img class="tex-graphics" src="file://k0Dp4DOI.png" style="max-width: 100.0%;max-height: 100.0%;">   <span class="tex-font-size-small">The graph has two strong vertices with numbers $3$ and $5$. Note that there is a bidirectional edge between vertices $3$ and $5$.</span> </center><p>In the third sample, the vertices are connected by a single directed edge from vertex $2$ to vertex $1$, so the only strong vertex is $2$.</p><p>In the fourth sample, all vertices are connected to each other by bidirectional edges, so there is a path from every vertex to any other vertex.</p>
