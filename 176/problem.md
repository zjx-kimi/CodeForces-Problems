## Description

<div><p>There is an infinite $2$-dimensional grid. Initially, a robot stands in the point $(0, 0)$. The robot can execute four commands:</p><ul> <li> <span class="tex-font-style-tt">U</span>&nbsp;— move from point $(x, y)$ to $(x, y + 1)$; </li><li> <span class="tex-font-style-tt">D</span>&nbsp;— move from point $(x, y)$ to $(x, y - 1)$; </li><li> <span class="tex-font-style-tt">L</span>&nbsp;— move from point $(x, y)$ to $(x - 1, y)$; </li><li> <span class="tex-font-style-tt">R</span>&nbsp;— move from point $(x, y)$ to $(x + 1, y)$. </li></ul><p>You are given a sequence of commands $s$ of length $n$. Your task is to answer $q$ <span class="tex-font-style-bf">independent</span> queries: given four integers $x$, $y$, $l$ and $r$; determine whether the robot visits the point $(x, y)$, while executing a sequence $s$, but the substring from $l$ to $r$ is reversed (i. e. the robot performs commands in order $s_1 s_2 s_3 \dots s_{l-1} s_r s_{r-1} s_{r-2} \dots s_l s_{r+1} s_{r+2} \dots s_n$).</p></div><div class="input-specification"><p>The first line contains two integers $n$ and $q$ ($1 \le n, q \le 2 \cdot 10^5$)&nbsp;— the length of the command sequence and the number of queries, respectively.</p><p>The second line contains a string $s$ of length $n$, consisting of characters <span class="tex-font-style-tt">U</span>, <span class="tex-font-style-tt">D</span>, <span class="tex-font-style-tt">L</span> and/or <span class="tex-font-style-tt">R</span>.</p><p>Then $q$ lines follow, the $i$-th of them contains four integers $x_i$, $y_i$, $l_i$ and $r_i$ ($-n \le x_i, y_i \le n$; $1 \le l \le r \le n$) describing the $i$-th query.</p></div><div class="output-specification"><p>For each query, print <span class="tex-font-style-tt">YES</span> if the robot visits the point $(x, y)$, while executing a sequence $s$, but the substring from $l$ to $r$ is reversed; otherwise print <span class="tex-font-style-tt">NO</span>.</p></div>

## Input

<p>The first line contains two integers $n$ and $q$ ($1 \le n, q \le 2 \cdot 10^5$)&nbsp;— the length of the command sequence and the number of queries, respectively.</p><p>The second line contains a string $s$ of length $n$, consisting of characters <span class="tex-font-style-tt">U</span>, <span class="tex-font-style-tt">D</span>, <span class="tex-font-style-tt">L</span> and/or <span class="tex-font-style-tt">R</span>.</p><p>Then $q$ lines follow, the $i$-th of them contains four integers $x_i$, $y_i$, $l_i$ and $r_i$ ($-n \le x_i, y_i \le n$; $1 \le l \le r \le n$) describing the $i$-th query.</p>

## Output

<p>For each query, print <span class="tex-font-style-tt">YES</span> if the robot visits the point $(x, y)$, while executing a sequence $s$, but the substring from $l$ to $r$ is reversed; otherwise print <span class="tex-font-style-tt">NO</span>.</p>





```input1|
8 3
RDLLUURU
-1 2 1 7
0 0 3 4
0 1 7 8
```




```input2|
4 2
RLDU
0 0 2 2
-1 -1 2 3
```




```input3|
10 6
DLUDLRULLD
-1 0 1 10
-1 -2 2 5
-4 -2 6 10
-1 0 3 9
0 1 4 7
-3 -1 5 8
```




```output1
YES
YES
NO
```




```output2
YES
NO
```




```output3
YES
YES
YES
NO
YES
YES
```



## Note

<p>In the first query of the first sample, the path of the robot looks as follows: </p><center> <img class="tex-graphics" src="file://1r1GNp5r.png" style="max-width: 100.0%;max-height: 100.0%;"> </center><p>In the second query of the first sample, the path of the robot looks as follows: </p><center> <img class="tex-graphics" src="file://MRqGqgel.png" style="max-width: 100.0%;max-height: 100.0%;"> </center><p>In the third query of the first sample, the path of the robot looks as follows: </p><center> <img class="tex-graphics" src="file://xAb12ruM.png" style="max-width: 100.0%;max-height: 100.0%;"> </center>
