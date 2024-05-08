## Description

<div><p>You are given a tree with $n$ nodes. For each node, you either color it in $0$ or $1$.</p><p>The value of a path $(u,v)$ is equal to the MEX$^\dagger$ of the colors of the nodes from the shortest path between $u$ and $v$.</p><p>The value of a coloring is equal to the sum of values of all paths $(u,v)$ such that $1 \leq u \leq v \leq n$.</p><p>What is the maximum possible value of any coloring of the tree?</p><p>$^{\dagger}$ The MEX (minimum excluded) of an array is the smallest non-negative integer that does not belong to the array. For instance:</p><ul> <li> The MEX of $[2,2,1]$ is $0$, because $0$ does not belong to the array. </li><li> The MEX of $[3,1,0,1]$ is $2$, because $0$ and $1$ belong to the array, but $2$ does not. </li><li> The MEX of $[0,3,1,2]$ is $4$ because $0$, $1$, $2$, and $3$ belong to the array, but $4$ does not. </li></ul></div><div class="input-specification"><p>Each test contains multiple test cases. The first line of input contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$)&nbsp;— the number of nodes in the tree.</p><p>The following $n-1$ lines of each test case contains $2$ integers $a_i$ and $b_i$ ($1 \leq a_i, b_i \leq n, a_i \neq b_i$)&nbsp;— indicating an edge between vertices $a_i$ and $b_i$. It is guaranteed that the given edges form a tree.</p><p>It is guaranteed that the sum of $n$ across all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, print the maximum possible value of any coloring of the tree.</p></div>

## Input

<p>Each test contains multiple test cases. The first line of input contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$)&nbsp;— the number of nodes in the tree.</p><p>The following $n-1$ lines of each test case contains $2$ integers $a_i$ and $b_i$ ($1 \leq a_i, b_i \leq n, a_i \neq b_i$)&nbsp;— indicating an edge between vertices $a_i$ and $b_i$. It is guaranteed that the given edges form a tree.</p><p>It is guaranteed that the sum of $n$ across all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, print the maximum possible value of any coloring of the tree.</p>





```input1|2,3,4,9,10,11,12,13,14,15,16,17,18
4
3
1 2
2 3
4
1 2
1 3
1 4
10
1 2
1 3
3 4
3 5
1 6
5 7
2 8
6 9
6 10
1
```




```output1
8
15
96
1
```



## Note

<p>In the first sample, we will color vertex $2$ in $1$ and vertices $1,3$ in $0$. After this, we consider all paths: </p><ul> <li> $(1,1)$ with value $1$ </li><li> $(1,2)$ with value $2$ </li><li> $(1,3)$ with value $2$ </li><li> $(2,2)$ with value $0$ </li><li> $(2,3)$ with value $2$ </li><li> $(3,3)$ with value $1$ </li></ul><p>We notice the sum of values is $8$ which is the maximum possible.</p>
