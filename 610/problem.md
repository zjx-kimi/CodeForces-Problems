## Description

<div><p>LuoTianyi gives you an array $a$ of $n$ integers and the index begins from $1$.</p><p>Define $g(i,j)$ as follows:</p><ul> <li> $g(i,j)$ is the largest integer $x$ that satisfies $\{a_p:i\le p\le j\}\subseteq\{a_q:x\le q\le j\}$ while $i \le j$; </li><li> and $g(i,j)=0$ while $i&gt;j$. </li></ul><p>There are $q$ queries. For each query you are given four integers $l,r,x,y$, you need to calculate $\sum\limits_{i=l}^{r}\sum\limits_{j=x}^{y}g(i,j)$.</p></div><div class="input-specification"><p>The first line contains two integers $n$ and $q$ ($1\le n,q\le 10^6$) — the length of the array $a$ and the number of queries.</p><p>The second line contains $n$ integers $a_1,a_2,\ldots,a_n$ ($1\le a_i\le n$) — the elements of the array $a$.</p><p>Next $q$ lines describe a query. The $i$-th line contains four integers $l,r,x,y$ ($1\le l\le r\le n, 1\le x\le y\le n$) — the integers in the $i$-th query.</p></div><div class="output-specification"><p>Print $q$ lines where $i$-th line contains one integer — the answer for the $i$-th query.</p></div>

## Input

<p>The first line contains two integers $n$ and $q$ ($1\le n,q\le 10^6$) — the length of the array $a$ and the number of queries.</p><p>The second line contains $n$ integers $a_1,a_2,\ldots,a_n$ ($1\le a_i\le n$) — the elements of the array $a$.</p><p>Next $q$ lines describe a query. The $i$-th line contains four integers $l,r,x,y$ ($1\le l\le r\le n, 1\le x\le y\le n$) — the integers in the $i$-th query.</p>

## Output

<p>Print $q$ lines where $i$-th line contains one integer — the answer for the $i$-th query.</p>





```input1
6 4
1 2 2 1 3 4
1 1 4 5
2 3 3 3
3 6 1 2
6 6 6 6
```




```input2
10 5
10 2 8 10 9 8 2 1 1 8
1 1 10 10
2 2 3 3
6 6 6 6
1 1 4 5
4 8 4 8
```




```output1
6
6
0
6
```




```output2
4
2
6
4
80
```



## Note

<p>In the first example:</p><p>In the first query, the answer is $g(1,4)+g(1,5)=3+3=6$.</p><p>$x=1,2,3$ can satisfies $\{a_p:1\le p\le 4\}\subseteq\{a_q:x\le q\le 4\}$, $3$ is the largest integer so $g(1,4)=3$.</p><p>In the second query, the answer is $g(2,3)+g(3,3)=3+3=6$.</p><p>In the third query, the answer is $0$, because all $i &gt; j$ and $g(i,j)=0$.</p><p>In the fourth query, the answer is $g(6,6)=6$.</p><p>In the second example:</p><p>In the second query, the answer is $g(2,3)=2$.</p><p>In the fourth query, the answer is $g(1,4)+g(1,5)=2+2=4$.</p>
