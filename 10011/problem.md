## Description

<div><p>You are given a tree, consisting of $n$ vertices, numbered from $1$ to $n$. Every vertex is colored in some color, denoted by an integer from $1$ to $n$.</p><p>A simple path of the tree is called <span class="tex-font-style-it">beautiful</span> if: </p><ul> <li> it consists of at least $2$ vertices; </li><li> the first and the last vertices of the path have the same color; </li><li> no other vertex on the path has the same color as the first vertex. </li></ul><p>Count the number of the <span class="tex-font-style-it">beautiful</span> simple paths of the tree. Note that paths are considered undirected (i. e. the path from $x$ to $y$ is the same as the path from $y$ to $x$).</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of testcases.</p><p>The first line of each testcase contains a single integer $n$ ($2 \le n \le 2 \cdot 10^5$)&nbsp;— the number of vertices in the tree.</p><p>The second line contains $n$ integers $c_1, c_2, \dots, c_n$ ($1 \le c_i \le n$)&nbsp;— the color of each vertex.</p><p>The $i$-th of the next $n - 1$ lines contains two integers $v_i$ and $u_i$ ($1 \le v_i, u_i \le n$; $v_i \neq u_i$)&nbsp;— the $i$-th edge of the tree.</p><p>The given edges form a valid tree. The sum of $n$ over all testcases doesn't exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each testcase, print a single integer&nbsp;— the number of the <span class="tex-font-style-it">beautiful</span> simple paths of the tree.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of testcases.</p><p>The first line of each testcase contains a single integer $n$ ($2 \le n \le 2 \cdot 10^5$)&nbsp;— the number of vertices in the tree.</p><p>The second line contains $n$ integers $c_1, c_2, \dots, c_n$ ($1 \le c_i \le n$)&nbsp;— the color of each vertex.</p><p>The $i$-th of the next $n - 1$ lines contains two integers $v_i$ and $u_i$ ($1 \le v_i, u_i \le n$; $v_i \neq u_i$)&nbsp;— the $i$-th edge of the tree.</p><p>The given edges form a valid tree. The sum of $n$ over all testcases doesn't exceed $2 \cdot 10^5$.</p>

## Output

<p>For each testcase, print a single integer&nbsp;— the number of the <span class="tex-font-style-it">beautiful</span> simple paths of the tree.</p>





```input1|2,3,4,5,12,13,14,15,16,17
4
3
1 2 1
1 2
2 3
5
2 1 2 1 2
1 2
1 3
3 4
4 5
5
1 2 3 4 5
1 2
1 3
3 4
4 5
4
2 2 2 2
3 1
3 2
3 4
```




```output1
1
3
0
3
```


