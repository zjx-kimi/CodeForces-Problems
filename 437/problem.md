## Description

<div><p><span class="tex-font-style-bf">This is the easy version of the problem. The differences between the two versions are the constraint on $n$ and the time limit. You can make hacks only if both versions of the problem are solved.</span></p><p>You are given a tree with $n$ vertices rooted at vertex $1$.</p><p>For some permutation$^\dagger$ $a$ of length $n$, let $f(a)$ be the number of pairs of vertices $(u, v)$ such that $a_u &lt; a_{\operatorname{lca}(u, v)} &lt; a_v$. Here, $\operatorname{lca}(u,v)$ denotes the <a href="https://en.wikipedia.org/wiki/Lowest_common_ancestor">lowest common ancestor</a> of vertices $u$ and $v$.</p><p>Find the maximum possible value of $f(a)$ over all permutations $a$ of length $n$.</p><p>$^\dagger$ A permutation of length $n$ is an array consisting of $n$ distinct integers from $1$ to $n$ in arbitrary order. For example, $[2,3,1,5,4]$ is a permutation, but $[1,2,2]$ is not a permutation ($2$ appears twice in the array), and $[1,3,4]$ is also not a permutation ($n=3$ but there is $4$ in the array).</p></div><div class="input-specification"><p>The first line contains a single integer $n$ ($2 \le n \le 5000$).</p><p>The second line contains $n - 1$ integers $p_2,p_3,\ldots,p_n$ ($1 \le p_i &lt; i$) indicating that there is an edge between vertices $i$ and $p_i$.</p></div><div class="output-specification"><p>Output the maximum value of $f(a)$.</p></div>

## Input

<p>The first line contains a single integer $n$ ($2 \le n \le 5000$).</p><p>The second line contains $n - 1$ integers $p_2,p_3,\ldots,p_n$ ($1 \le p_i &lt; i$) indicating that there is an edge between vertices $i$ and $p_i$.</p>

## Output

<p>Output the maximum value of $f(a)$.</p>





```input1
5
1 1 3 3
```




```input2
2
1
```




```input3
6
1 2 2 1 5
```




```input4
4
1 1 1
```




```output1
4
```




```output2
0
```




```output3
7
```




```output4
2
```



## Note

<p>The tree in the first test: </p><center> <img class="tex-graphics" src="file://1Vp6oQLV.png" style="max-width: 100.0%;max-height: 100.0%;"> </center><p>One possible optimal permutation $a$ is $[2, 1, 4, 5, 3]$ with $4$ suitable pairs of vertices: </p><ul> <li> $(2, 3)$, since $\operatorname{lca}(2, 3) = 1$ and $1 &lt; 2 &lt; 4$, </li><li> $(2, 4)$, since $\operatorname{lca}(2, 4) = 1$ and $1 &lt; 2 &lt; 5$, </li><li> $(2, 5)$, since $\operatorname{lca}(2, 5) = 1$ and $1 &lt; 2 &lt; 3$, </li><li> $(5, 4)$, since $\operatorname{lca}(5, 4) = 3$ and $3 &lt; 4 &lt; 5$. </li></ul><p>The tree in the third test: </p><center> <img class="tex-graphics" src="file://2VSyeLVt.png" style="max-width: 100.0%;max-height: 100.0%;"> </center><p>The tree in the fourth test: </p><center> <img class="tex-graphics" src="file://XpmA2mye.png" style="max-width: 100.0%;max-height: 100.0%;"> </center>
