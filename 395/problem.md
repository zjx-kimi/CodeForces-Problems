## Description

<div><p>You are given a tree with $n$ vertices labeled $1, 2, \ldots, n$. The length of a simple path in the tree is the number of vertices in it.</p><p>You are to select a set of simple paths of length at least $2$ each, but you cannot simultaneously select two distinct paths contained one in another. Find the largest possible size of such a set.</p><p>Formally, a set $S$ of vertices is called a <span class="tex-font-style-it">route</span> if it contains <span class="tex-font-style-bf">at least two vertices</span> and coincides with the set of vertices of a simple path in the tree. A collection of distinct routes is called a <span class="tex-font-style-it">timetable</span>. A route $S$ in a timetable $T$ is called <span class="tex-font-style-it">redundant</span> if there is a different route $S' \in T$ such that $S \subset S'$. A timetable is called <span class="tex-font-style-it">efficient</span> if it contains no redundant routes. Find the largest possible number of routes in an efficient timetable.</p></div><div class="input-specification"><p>The first line contains a single integer $n$ ($2 \le n \le 3000$).</p><p>The $i$-th of the following $n - 1$ lines contains two integers $u_i$ and $v_i$ ($1 \le u_i, v_i \le n$, $u_i \neq v_i$)&nbsp;— the numbers of vertices connected by the $i$-th edge.</p><p>It is guaranteed that the given edges form a tree.</p></div><div class="output-specification"><p>Print a single integer&nbsp;— the answer to the problem.</p></div>

## Input

<p>The first line contains a single integer $n$ ($2 \le n \le 3000$).</p><p>The $i$-th of the following $n - 1$ lines contains two integers $u_i$ and $v_i$ ($1 \le u_i, v_i \le n$, $u_i \neq v_i$)&nbsp;— the numbers of vertices connected by the $i$-th edge.</p><p>It is guaranteed that the given edges form a tree.</p>

## Output

<p>Print a single integer&nbsp;— the answer to the problem.</p>





```input1
4
1 2
1 3
1 4
```




```input2
7
2 1
3 2
4 3
5 3
6 4
7 4
```




```output1
3
```




```output2
7
```



## Note

<p>In the first example, possible efficient timetables are $\{\{1, 2\}, \{1, 3\}, \{1, 4\}\}$ and $\{\{1, 2, 3\}, \{1, 2, 4\}, \{1, 3, 4\}\}$.</p><p>In the second example, we can choose $\{ \{1, 2, 3\}, \{2, 3, 4\}, \{3, 4, 6\}, \{2, 3, 5\}, \{3, 4, 5\}, \{3, 4, 7\}, \{4, 6, 7\}\}$.</p>
