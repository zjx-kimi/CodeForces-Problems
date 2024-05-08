## Description

<div><p>You want to plant trees in a square lawn of size $n \times n$ whose corners have Cartesian coordinates $(0, 0)$, $(n, 0)$, $(0, n)$, and $(n, n)$. Trees can only be planted at locations with integer coordinates. Every tree will grow roots within a disk of radius $r$ centered at the location where the tree was planted; such disks must be fully contained in the lawn (possibly touching the boundary of the lawn) and can only intersect each other on their boundaries.</p><p>Find a configuration that maximizes the number of trees.</p></div><div class="input-specification"><p>The first and only line contains an integer $n$ ($1 \leq n \leq 20$) and a real number $r$ ($0 &lt; r \leq n/2$) — the length of the sides of the lawn, and the radius of the disks where each tree will grow roots. The real number $r$ is given in decimal notation with at least $1$ and at most $3$ digits after the decimal point.</p></div><div class="output-specification"><p>In the first line, print the maximum number $m$ of trees that can be planted.</p><p>In the next $m$ lines, print a configuration that maximizes the number of trees. Specifically, in the $(i+1)$-th line, print two integers $x$ and $y$ — the coordinates of the location where the $i$-th tree should be planted. You can print the trees in any order.</p><p>If there are multiple solutions, print any of them.</p></div>

## Input

<p>The first and only line contains an integer $n$ ($1 \leq n \leq 20$) and a real number $r$ ($0 &lt; r \leq n/2$) — the length of the sides of the lawn, and the radius of the disks where each tree will grow roots. The real number $r$ is given in decimal notation with at least $1$ and at most $3$ digits after the decimal point.</p>

## Output

<p>In the first line, print the maximum number $m$ of trees that can be planted.</p><p>In the next $m$ lines, print a configuration that maximizes the number of trees. Specifically, in the $(i+1)$-th line, print two integers $x$ and $y$ — the coordinates of the location where the $i$-th tree should be planted. You can print the trees in any order.</p><p>If there are multiple solutions, print any of them.</p>





```input1|
6 1.241
```




```input2|
9 2.0
```




```output1
2
4 2
2 4
```




```output2
4
2 2
7 2
2 6
6 6
```



## Note

<p>For the <span class="tex-font-style-bf">first sample</span>, the sample output is shown in the following figure. Note that this is not the only configuration that maximizes the number of trees. </p><center> <img class="tex-graphics" src="file://CDN4SVbR.png" style="max-width: 100.0%;max-height: 100.0%;" width="399px"> </center><p>For the <span class="tex-font-style-bf">second sample</span>, the sample output is shown in the following figure. Note that this is not the only configuration that maximizes the number of trees. </p><center> <img class="tex-graphics" src="file://BzMMa8XE.png" style="max-width: 100.0%;max-height: 100.0%;" width="399px"> </center>
