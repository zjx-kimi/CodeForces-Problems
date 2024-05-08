## Description

<div><p>Let us call an edge-weighted tree with $n$ vertices numbered from $1$ to $n$ <span class="tex-font-style-it">good</span> if the weight of each edge is either $1$ or $-1$ and for each vertex $i$, the product of the edge weights of all edges having $i$ as one endpoint is $-1$.</p><p>You are given a positive integer $n$. There are $n^{n-2} \cdot 2^{n-1}$ distinct$^\dagger$ edge-weighted trees with $n$ vertices numbered from $1$ to $n$ such that each edge is either $1$ or $-1$. Your task is to find the sum of $d(1,n)^\ddagger$ of all such trees that are good. Since the answer can be quite large, you only need to find it modulo $998\,244\,353$.</p><p>$^\dagger$ Two trees are considered to be distinct if either: </p><ul> <li> there exists two vertices such that there is an edge between them in one of the trees, and not in the other. </li><li> there exists two vertices such that there is an edge between them in both trees but the weight of the edge between them in one tree is different from the one in the other tree. </li></ul><p>Note that by <a href="https://rb.gy/hho7vu">Cayley's formula</a>, the number of trees on $n$ labeled vertices is $n^{n-2}$. Since we have $n-1$ edges, there are $2^{n-1}$ possible assignment of weights(weight can either be $1$ or $-1$). That is why total number of distinct edge-weighted tree is $n^{n-2} \cdot 2^{n-1}$.</p><p>$^\ddagger$ $d(u,v)$ denotes the sum of the weight of all edges on the unique simple path from $u$ to $v$.</p></div><div class="input-specification"><p>The first and only line of input contains a single integer $n$ ($1 \leq n \leq 5 \cdot 10^5$).</p></div><div class="output-specification"><p>The only line of output should contain a single integer, the required answer, modulo $998\,244\,353$.</p></div>

## Input

<p>The first and only line of input contains a single integer $n$ ($1 \leq n \leq 5 \cdot 10^5$).</p>

## Output

<p>The only line of output should contain a single integer, the required answer, modulo $998\,244\,353$.</p>





```input1
2
```




```input2
1
```




```input3
4
```




```input4
10
```




```input5
43434
```




```output1
998244352
```




```output2
0
```




```output3
998244343
```




```output4
948359297
```




```output5
86232114
```



## Note

<p>In the first test case, there is only $1$ distinct <span class="tex-font-style-it">good</span> tree. The value of $d(1,2)$ for that tree is $-1$, which is $998\,244\,352$ under modulo $998\,244\,353$.</p><p>In the second test case, the value of $d(1,1)$ for any tree is $0$, so the answer is $0$.</p><p>In the third test case, there are $16$ distinct <span class="tex-font-style-it">good</span> trees. The value of $d(1,4)$ is: </p><ul> <li> $-2$ for $2$ trees; </li><li> $-1$ for $8$ trees; </li><li> $0$ for $4$ trees; </li><li> $1$ for $2$ trees. </li></ul><p>The sum of $d(1,4)$ over all trees is $2 \cdot (-2) + 8 \cdot (-1) + 4 \cdot (0) + 2 \cdot (1) = -10$, which is $998\,244\,343$ under modulo $998\,244\,353$.</p>
