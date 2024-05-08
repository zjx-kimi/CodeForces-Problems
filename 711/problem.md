## Description

<div><p>You are given an integer $n$ and an array $a$ of length $n-1$ whose elements are either $0$ or $1$.</p><p>Let us define the <span class="tex-font-style-it">value</span> of a permutation$^\dagger$ $p$ of length $m-1$ ($m \leq n$) by the following process.</p><p>Let $G$ be a graph of $m$ vertices labeled from $1$ to $m$ that does not contain any edges. For each $i$ from $1$ to $m-1$, perform the following operations: </p><ul> <li> define $u$ and $v$ as the (unique) vertices in the weakly connected components$^\ddagger$ containing vertices $p_i$ and $p_i+1$ respectively with only incoming edges$^{\dagger\dagger}$; </li><li> in graph $G$, add a directed edge from vertex $v$ to $u$ if $a_{p_i}=0$, otherwise add a directed edge from vertex $u$ to $v$ (if $a_{p_i}=1$). </li></ul> Note that after each step, it can be proven that each weakly connected component of $G$ has a unique vertex with only incoming edges.<p>Then, the value of $p$ is the number of incoming edges of vertex $1$ of $G$.</p><p>For each $k$ from $1$ to $n-1$, find the sum of values of all $k!$ permutations of length $k$. Since this value can be big, you are only required to compute this value under modulo $998\,244\,353$.</p><center> <img class="tex-graphics" src="file://Ivayr7X1.png" style="max-width: 100.0%;max-height: 100.0%;"> <span class="tex-font-size-small">Operations when $n=3$, $a=[0,1]$ and $p=[1,2]$</span> </center><p>$^\dagger$ A permutation of length $n$ is an array consisting of $n$ distinct integers from $1$ to $n$ in arbitrary order. For example, $[2,3,1,5,4]$ is a permutation, but $[1,2,2]$ is not a permutation ($2$ appears twice in the array), and $[1,3,4]$ is also not a permutation ($n=3$ but there is $4$ in the array).</p><p>$^\ddagger$ The weakly connected components of a directed graph is the same as the components of the undirected version of the graph. Formally, for directed graph $G$, define a graph $H$ where for all edges $a \to b$ in $G$, you add an undirected edge $a \leftrightarrow b$ in $H$. Then the weakly connected components of $G$ are the components of $H$.</p><p>$^{\dagger\dagger}$ Note that a vertex that has no edges is considered to have only incoming edges.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1\le t\le 10^4$)&nbsp;— the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2\le n\le 5 \cdot 10^5$).</p><p>The second line of each test case contains $n-1$ integers $a_1, a_2, \ldots, a_{n-1}$ ($a_i$ is $0$ or $1$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $5 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output $n-1$ integers in a line, the $i$-th integer should represent the answer when $k=i$, under modulo $998\,244\,353$.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1\le t\le 10^4$)&nbsp;— the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2\le n\le 5 \cdot 10^5$).</p><p>The second line of each test case contains $n-1$ integers $a_1, a_2, \ldots, a_{n-1}$ ($a_i$ is $0$ or $1$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $5 \cdot 10^5$.</p>

## Output

<p>For each test case, output $n-1$ integers in a line, the $i$-th integer should represent the answer when $k=i$, under modulo $998\,244\,353$.</p>





```input1|2,3
2
3
0 0
9
0 1 0 0 0 1 0 0
```




```output1
1 3 
1 2 7 31 167 1002 7314 60612
```



## Note

<p>Consider the first test case.</p><p>When $k=1$, there is only $1$ permutation $p$.</p><ul> <li> When $p=[1]$, we will add a single edge from vertex $2$ to $1$. Vertex $1$ will have $1$ incoming edge. So the value of $[1]$ is $1$. </li></ul><p>Therefore when $k=1$, the answer is $1$.</p><p>When $k=2$, there are $2$ permutations $p$.</p><ul> <li> When $p=[1,2]$, we will add an edge from vertex $2$ to $1$ and an edge from $3$ to $1$. Vertex $1$ will have $2$ incoming edges. So the value of $[1,2]$ is $2$. </li><li> When $p=[2,1]$, we will add an edge from vertex $3$ to $2$ and an edge from $2$ to $1$. Vertex $1$ will have $1$ incoming edge. So the value of $[2,1]$ is $1$. </li></ul><p>Therefore when $k=2$, the answer is $2+1=3$.</p>
