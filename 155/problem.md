## Description

<div><p>In this sad world full of imperfections, ugly segment trees exist.</p><p>A segment tree is a tree where each node represents a segment and has its number. A segment tree for an array of $n$ elements can be built in a recursive manner. Let's say function $\operatorname{build}(v,l,r)$ builds the segment tree rooted in the node with number $v$ and it corresponds to the segment $[l,r]$.</p><p>Now let's define $\operatorname{build}(v,l,r)$: </p><ul> <li> If $l=r$, this node $v$ is a leaf so we stop adding more edges </li><li> Else, we add the edges $(v, 2v)$ and $(v, 2v+1)$. Let $m=\lfloor \frac{l+r}{2} \rfloor$. Then we call $\operatorname{build}(2v,l,m)$ and $\operatorname{build}(2v+1,m+1,r)$. </li></ul><p>So, the whole tree is built by calling $\operatorname{build}(1,1,n)$.</p><p>Now Ibti will construct a segment tree for an array with $n$ elements. He wants to find the sum of $\operatorname{lca}^\dagger(S)$, where $S$ is a non-empty subset of <span class="tex-font-style-bf">leaves</span>. Notice that there are exactly $2^n - 1$ possible subsets. Since this sum can be very large, output it modulo $998\,244\,353$.</p><p>$^\dagger\operatorname{lca}(S)$ is the number of the least common ancestor for the nodes that are in $S$.</p></div><div class="input-specification"><p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 10^3$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2 \le n \le 10^{18}$)&nbsp;— the length of the array for which the segment tree is built.</p></div><div class="output-specification"><p>For each test case, output a single integer — the required sum modulo $998\,244\,353$.</p></div>

## Input

<p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 10^3$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2 \le n \le 10^{18}$)&nbsp;— the length of the array for which the segment tree is built.</p>

## Output

<p>For each test case, output a single integer — the required sum modulo $998\,244\,353$.</p>





```input1|2,4,6
5
2
3
4
5
53278
```




```output1
6
17
36
69
593324855
```



## Note

<center> <img class="tex-graphics" src="file://5SSJXAb5.png" style="max-width: 100.0%;max-height: 100.0%;"> </center><p>In the first test case:</p><p>Let's look at all subsets of leaves.</p><ul> <li> $\operatorname{lca}(\{2\})=2$; </li><li> $\operatorname{lca}(\{3\})=3$; </li><li> $\operatorname{lca}(\{2,3\})=1$. </li></ul><p>Thus, the answer is $2+3+1=6$.</p><p>In the second test case:</p><p>Let's look at all subsets of leaves.</p><ul> <li> $\operatorname{lca}(\{4\})=4$; </li><li> $\operatorname{lca}(\{5\})=5$; </li><li> $\operatorname{lca}(\{3\})=3$; </li><li> $\operatorname{lca}(\{4,5\})=2$; </li><li> $\operatorname{lca}(\{4,3\})=1$; </li><li> $\operatorname{lca}(\{5,3\})=1$; </li><li> $\operatorname{lca}(\{4,5,3\})=1$; </li></ul><p>Thus, the answer is $4+5+3+2+1+1+1=17$.</p>
