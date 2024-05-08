## Description

<div><p>You are given a tree with $n$ vertices numbered $1, 2, \ldots, n$. Initially, all vertices are colored white.</p><p>You can perform the following two-step operation: </p><ol> <li> Choose a vertex $v$ ($1 \leq v \leq n$) and a distance $d$ ($0 \leq d \leq n-1$). </li><li> For all vertices $u$ ($1 \leq u \leq n$) such that $\text{dist}^\dagger(u,v)=d$, color $u$ black. </li></ol><p>Construct a sequence of operations to color all the nodes in the tree black using the minimum possible number of operations. It can be proven that it is always possible to do so using at most $n$ operations.</p><p>$^\dagger$ $\text{dist}(x, y)$ denotes the number of edges on the (unique) simple path between vertices $x$ and $y$ on the tree.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 200$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 2 \cdot 10^3$)&nbsp;— the number of vertices of the tree.</p><p>The following $n - 1$ lines of each test case describe the edges of the tree. The $i$-th of these lines contains two integers $u_i$ and $v_i$ ($1 \le u_i, v_i \le n$, $u_i \neq v_i$), the indices of the vertices connected by the $i$-th edge.</p><p>It is guaranteed that the given edges form a tree.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^3$.</p></div><div class="output-specification"><p>For each test case, first output a single integer $op$&nbsp;$(1 \le op \le n)$, the minimum number of operations needed to color all vertices of the tree black.</p><p>Then, output $op$ lines, each containing $2$ integers. The $i$-th line should contain the values of $v$ and $d$ chosen for the $i$-th operation ($1 \le v \le n$, $0 \le d \le n - 1$)</p><p>You must guarantee that at the end of $op$ operations, all vertices are colored black.</p><p>If there are multiple solutions, you may output any one of them.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 200$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 2 \cdot 10^3$)&nbsp;— the number of vertices of the tree.</p><p>The following $n - 1$ lines of each test case describe the edges of the tree. The $i$-th of these lines contains two integers $u_i$ and $v_i$ ($1 \le u_i, v_i \le n$, $u_i \neq v_i$), the indices of the vertices connected by the $i$-th edge.</p><p>It is guaranteed that the given edges form a tree.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^3$.</p>

## Output

<p>For each test case, first output a single integer $op$&nbsp;$(1 \le op \le n)$, the minimum number of operations needed to color all vertices of the tree black.</p><p>Then, output $op$ lines, each containing $2$ integers. The $i$-th line should contain the values of $v$ and $d$ chosen for the $i$-th operation ($1 \le v \le n$, $0 \le d \le n - 1$)</p><p>You must guarantee that at the end of $op$ operations, all vertices are colored black.</p><p>If there are multiple solutions, you may output any one of them.</p>





```input1|2,5,6,7,8
4
1
2
1 2
4
1 2
1 3
1 4
7
2 7
3 2
6 4
5 7
1 6
6 7
```




```output1
1
1 0
2
1 1
2 1
2
1 1
2 1
3
6 1
7 1
2 1
```



## Note

<p>In the first test case, there is only one possible operation, and performing it gives us a valid answer.</p><p>In the second test case, the first operation colors vertex $2$ black, and the second operation colors vertex $1$ black. It can be shown that it is impossible to color both vertices black in one operation, so the minimum number of operations needed is $2$. Another possible solution is to use the $2$ operations: $(u, r) = (1, 0)$ and $(u, r) = (2, 0)$.</p><p>In the third test case, the first operation colors vertices $2$, $3$ and $4$ black, and the second operation colors vertex $1$ black. Again, it can be shown that it is impossible to color all vertices black in $1$ operation, so the minimum number of operations needed is $2$.</p><p>In the fourth test case, the first operation colors vertices $4$, $1$ and $7$ black, the second operation colors vertices $2$, $5$ and $6$ black while the third operation colors vertices $3$ and $7$ black. Notice that it is allowed to color vertex $7$ black twice.</p><p>Thus, each node was marked at least once, with node $7$ marked twice. It can be shown that it is impossible to color all vertices black in fewer than $3$ moves.</p>
