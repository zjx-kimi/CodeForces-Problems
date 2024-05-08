## Description

<div><p>There is a complete rooted binary tree, that is, a rooted tree in which each vertex has either $0$ or $2$ children. The root of the tree is vertex $1$. A node without children is called a <span class="tex-font-style-it">leaf</span>. Each leaf has a <span class="tex-font-style-it">hunger value</span>, we denote the hunger value of leaf $v$ by $h_v$.</p><p>Each inner vertex of the tree has a selector pointing to one of the children of the vertex.</p><p>This tree accepts cookies. Before launching the process you can choose the initial state of each selector individually. The process is as follows:</p><ul> <li> Initially there are no cookies in vertices. </li><li> You insert cookies into the root one by one. </li><li> As long as the cookie is not in a leaf, it falls to the child defined by the selector in the current vertex. This selector then changes its state to the opposite one, i.&nbsp;e. it starts pointing to the other child of the vertex. </li><li> You stop inserting cookies when each leaf $v$ has at least $h_v$ cookies in it. In this case, we say that the tree is filled up. </li></ul><p>You have $q$ queries. Each query changes the value of $h_v$ for some leaf $v$. You need to print $q + 1$ numbers, the $i$-th of them being the minimum number of cookies required to fill up the machine after $(i - 1)$ updates if you can pick any initial state for every selector. Since these numbers may be very large, print the answers modulo $998\,244\,353$.</p><p>Please note that you can choose the initial state of all selectors independently between queries. However, the queries themselves are not independent: when answering the $i$-th query, you should also consider the effect of queries $1, 2, \ldots, i - 1$.</p></div><div class="input-specification"><p>The first line contains a single integer $n$ ($1\le n &lt; 200\,000$)&nbsp;— the number of vertices in the tree.</p><p>The second line contains $n - 1$ integers $p_2, p_3, \ldots, p_n$ ($1\le p_i &lt; i$), meaning that the parent of vertex $i$ is $p_i$.</p><p>The third line contains $n$ integers $h_1, h_2, \ldots, h_n$ ($0\le h_i\le 10^9$)&nbsp;— the hunger values of vertices. If vertex $i$ is not a leaf, then $h_i = 0$ and this value is irrelevant. However, $h_i = 0$ may also hold if $i$ is a leaf.</p><p>The fourth line contains a single integer $q$ ($0\le q\le 200\,000$)&nbsp;— the number of queries.</p><p>Each of the next $q$ lines contains two integers $v$ and $x$ ($1\le v\le n$, $0\le x\le 10^9$), meaning that the hunger value of vertex $v$ is set to $x$.</p><p>It is guaranteed that the tree in the input is a full binary tree rooted at vertex $1$. It is also guaranteed that in each query $v$ is a leaf.</p></div><div class="output-specification"><p>Output $q + 1$ integers, $i$-th of them being the minimum number of cookies needed to fill up the machine after $(i - 1)$ updates, modulo $998\,244\,353$.</p></div>

## Input

<p>The first line contains a single integer $n$ ($1\le n &lt; 200\,000$)&nbsp;— the number of vertices in the tree.</p><p>The second line contains $n - 1$ integers $p_2, p_3, \ldots, p_n$ ($1\le p_i &lt; i$), meaning that the parent of vertex $i$ is $p_i$.</p><p>The third line contains $n$ integers $h_1, h_2, \ldots, h_n$ ($0\le h_i\le 10^9$)&nbsp;— the hunger values of vertices. If vertex $i$ is not a leaf, then $h_i = 0$ and this value is irrelevant. However, $h_i = 0$ may also hold if $i$ is a leaf.</p><p>The fourth line contains a single integer $q$ ($0\le q\le 200\,000$)&nbsp;— the number of queries.</p><p>Each of the next $q$ lines contains two integers $v$ and $x$ ($1\le v\le n$, $0\le x\le 10^9$), meaning that the hunger value of vertex $v$ is set to $x$.</p><p>It is guaranteed that the tree in the input is a full binary tree rooted at vertex $1$. It is also guaranteed that in each query $v$ is a leaf.</p>

## Output

<p>Output $q + 1$ integers, $i$-th of them being the minimum number of cookies needed to fill up the machine after $(i - 1)$ updates, modulo $998\,244\,353$.</p>





```input1
5
1 1 2 2
0 0 0 0 0
5
3 1
4 1
5 1
3 4
4 1000000000
```




```output1
0
1
2
3
7
7022585
```



## Note

<p>Consider the example. Before any queries are made, no cookies need to be inserted, since all hunger values of zero are trivially satisfied.</p><p>After the first query, we can choose the selector in vertex $1$ pointing to vertex $3$. Then one cookie will immediately descend to $3$.</p><p>After the second query, we choose the selector in vertex $1$ pointing to vertex $3$ and the selector in vertex $2$ pointing to vertex $4$. The first cookie will drop down to $3$ and change the state of the selector in vertex $1$: now it is pointing to $2$. The second cookie will go via the path $1 \to 2 \to 4$.</p><p>After the third query, we choose the selector in vertex $1$ pointing to vertex $2$ and the selector in vertex $2$ pointing to vertex $4$. Then the three cookies will descend via the paths $1 \to 2 \to 4$, $1 \to 3$, $1 \to 2 \to 5$.</p><p>After the fourth query, we choose the selector in vertex $1$ pointing to vertex $3$. Regardless of the initial state of the selector in vertex $2$, after seven cookies are inserted, four of them will be in leaf $3$, and one or two cookies will be in each of the leaves $4$ and $5$ (note that exceeding the hunger value is allowed).</p><p>The answer after the fifth query is $3\,999\,999\,997$. Do not forget to print the answer modulo $998\,244\,353$.</p>
