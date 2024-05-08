## Description

<div><p>Monocarp has a tree, consisting of $n$ vertices.</p><p>He is going to select some vertex $r$ and perform the following operations on each vertex $v$ from $1$ to $n$: </p><ul> <li> set $d_v$ equal to the distance from $v$ to $r$ (the number of edges on the shortest path); </li><li> color $v$ some color. </li></ul><p>A <span class="tex-font-style-it">nice</span> coloring satisfies two conditions: </p><ul> <li> for each pair of vertices of the same color $(v, u)$, there exists a path from $v$ to $u$ that only visits vertices of the same color; </li><li> for each pair of vertices of the same color $(v, u)$, $d_v \neq d_u$. </li></ul><p>Note that Monocarp can choose any amount of different colors he wants to use.</p><p>For each used color, he then counts the number of vertices of this color. The <span class="tex-font-style-it">cost</span> of the tree is the minimum of these numbers.</p><p>What can be the maximum cost of the tree?</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of testcases.</p><p>The first line of each testcase contains a single integer $n$ ($3 \le n \le 2 \cdot 10^5$)&nbsp;— the number of vertices in the tree.</p><p>Each of the next $n-1$ lines contains two integers $v$ and $u$ ($1 \le v, u \le n$)&nbsp;— the description of an edge.</p><p>The given edges form a tree. The sum of $n$ over all testcases doesn't exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each testcase print a single integer&nbsp;— the maximum possible cost of the tree.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of testcases.</p><p>The first line of each testcase contains a single integer $n$ ($3 \le n \le 2 \cdot 10^5$)&nbsp;— the number of vertices in the tree.</p><p>Each of the next $n-1$ lines contains two integers $v$ and $u$ ($1 \le v, u \le n$)&nbsp;— the description of an edge.</p><p>The given edges form a tree. The sum of $n$ over all testcases doesn't exceed $2 \cdot 10^5$.</p>

## Output

<p>For each testcase print a single integer&nbsp;— the maximum possible cost of the tree.</p>





```input1|2,3,4,5,11,12,13
4
4
1 2
2 3
3 4
5
1 2
1 3
1 4
1 5
3
1 3
3 2
7
3 2
2 5
7 5
3 1
1 6
1 4
```




```output1
4
1
3
3
```


