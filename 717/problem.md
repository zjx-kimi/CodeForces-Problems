## Description

<div><p>You are given a tree (a connected graph without cycles). Each vertex of the tree contains an integer. Let's define the $\mathrm{MAD}$ (maximum double) parameter of the tree as the maximum integer that occurs in the vertices of the tree <span class="tex-font-style-bf">at least</span> $2$ times. If no number occurs in the tree more than once, then we assume $\mathrm{MAD}=0$.</p><p>Note that if you remove an edge from the tree, it splits into two trees. Let's compute the $\mathrm{MAD}$ parameters of the two trees and take the maximum of the two values. Let the result be the <span class="tex-font-style-it">value</span> of the deleted edge.</p><p>For each edge, find its value. Note that we don't actually delete any edges from the tree, the values are to be found independently.</p></div><div class="input-specification"><p>The first line contains one integer $n$ ($2 \le n \le 10^5$)&nbsp;— the number of vertices in the tree.</p><p>Each of the next $n - 1$ lines contains two integers $u$ and $v$ ($1 \le u, v \le n$)&nbsp;— the ends of an edge of the tree. It's guaranteed that the given edges form a valid tree.</p><p>The last line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le 10^9$)&nbsp;— the numbers in the vertices.</p></div><div class="output-specification"><p>For each edge in the input order, print one number&nbsp;— the maximum of the $\mathrm{MAD}$ parameters of the two trees obtained after removing the given edge from the initial tree.</p></div>

## Input

<p>The first line contains one integer $n$ ($2 \le n \le 10^5$)&nbsp;— the number of vertices in the tree.</p><p>Each of the next $n - 1$ lines contains two integers $u$ and $v$ ($1 \le u, v \le n$)&nbsp;— the ends of an edge of the tree. It's guaranteed that the given edges form a valid tree.</p><p>The last line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le 10^9$)&nbsp;— the numbers in the vertices.</p>

## Output

<p>For each edge in the input order, print one number&nbsp;— the maximum of the $\mathrm{MAD}$ parameters of the two trees obtained after removing the given edge from the initial tree.</p>





```input1
5
1 2
2 3
2 4
1 5
2 1 3 2 1
```




```input2
6
1 2
1 3
1 4
4 5
4 6
1 2 3 1 4 5
```




```output1
0
2
1
2
```




```output2
1
1
0
1
1
```



## Note

<center> <img class="tex-graphics" src="file://iojCcI0O.png" style="max-width: 100.0%;max-height: 100.0%;" width="302px"> </center><p>In the first example, after removing edge $(1, 2)$ no number repeats $2$ times in any of the resulting subtrees, so the answer is $\max(0, 0)=0$.</p><p>After removing edge $(2, 3)$, in the bigger subtree, $1$ is repeated twice, and $2$ is repeated twice, so the $\mathrm{MAD}$ of this tree is $2$.</p><p>After removing edge $(2, 4)$, in the bigger subtree, only the number $1$ is repeated, and in the second subtree, only one number appears, so the answer is $1$.</p><p>In the second example, if edge $1 \leftrightarrow 4$ is not removed, then one of the subtrees will have two $1$, so the answer&nbsp;— $1$. And if edge $1 \leftrightarrow 4$ is deleted, both subtrees have no repeating values, so the answer is $0$.</p>
