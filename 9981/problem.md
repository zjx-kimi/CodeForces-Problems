## Description

<div><p>Define a function $f$ such that for an array $b$, $f(b)$ returns the array of prefix maxima of $b$. In other words, $f(b)$ is an array containing only those elements $b_i$, for which $b_i=\max(b_1,b_2,\ldots,b_i)$, without changing their order. For example, $f([3,10,4,10,15,1])=[3,10,10,15]$.</p><p>You are given a tree consisting of $n$ nodes rooted at $1$.</p><p>A permutation$^\dagger$ $p$ of is considered a <span class="tex-font-style-it">pre-order</span> of the tree if for all $i$ the following condition holds: </p><ul> <li> Let $k$ be the number of proper descendants$^\ddagger$ of node $p_i$. </li><li> For all $x$ such that $i &lt; x \leq i+k$, $p_x$ is a proper descendant of node $p_i$. </li></ul><p>Find the number of distinct values of $f(a)$ over all possible pre-orders $a$. Since this value might be large, you only need to find it modulo $998\,244\,353$.</p><p>$^\dagger$ A permutation of length $n$ is an array consisting of $n$ distinct integers from $1$ to $n$ in arbitrary order. For example, $[2,3,1,5,4]$ is a permutation, but $[1,2,2]$ is not a permutation ($2$ appears twice in the array), and $[1,3,4]$ is also not a permutation ($n=3$ but there is $4$ in the array).</p><p>$^\ddagger$ Node $t$ is a proper descendant of node $s$ if $s \neq t$ and $s$ is on the unique simple path from $t$ to $1$.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 10^5$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \leq n \leq 10^6$)&nbsp;— the number of vertices.</p><p>The following next $n-1$ lines contain two integers $u$ and $v$ ($1 \leq u, v \leq n$, $u \neq v$)&nbsp;— denoting an edge between nodes $u$ and $v$. It is guaranteed that the given edges form a tree.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^6$.</p></div><div class="output-specification"><p>For each test case, output the number of distinct values of $f(a)$ modulo $998\,244\,353$ that you can get.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 10^5$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \leq n \leq 10^6$)&nbsp;— the number of vertices.</p><p>The following next $n-1$ lines contain two integers $u$ and $v$ ($1 \leq u, v \leq n$, $u \neq v$)&nbsp;— denoting an edge between nodes $u$ and $v$. It is guaranteed that the given edges form a tree.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^6$.</p>

## Output

<p>For each test case, output the number of distinct values of $f(a)$ modulo $998\,244\,353$ that you can get.</p>





```input1|2,5,6,7,11,12,13,14,15
6
1
2
1 2
3
1 2
1 3
3
1 2
2 3
5
1 2
1 3
1 4
1 5
10
1 2
2 3
1 4
2 5
2 6
4 7
5 8
4 9
9 10
```




```output1
1
1
2
1
8
6
```



## Note

<p>In the first test case, the only valid pre-order is $a=[1]$. So the only possible value of $f(a)$ is $[1]$.</p><p>In the second test case, the only valid pre-order is $a=[1,2]$. So the only possible value $f(a)$ is $[1,2]$.</p><p>In the third test case, the two valid pre-orders are $a=[1,2,3]$ and $a=[1,3,2]$. So the possible values of $f(a)$ are $[1,2,3]$ and $[1,3]$.</p><p>In the fifth test case, the possible values of $f(a)$ are: </p><ul> <li> $[1,5]$; </li><li> $[1,2,5]$; </li><li> $[1,3,5]$; </li><li> $[1,4,5]$; </li><li> $[1,2,3,5]$; </li><li> $[1,2,4,5]$; </li><li> $[1,3,4,5]$; </li><li> $[1,2,3,4,5]$. </li></ul>
