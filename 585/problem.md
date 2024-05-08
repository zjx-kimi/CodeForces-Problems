## Description

<div><p>Copil Copac is given a list of $n-1$ edges describing a tree of $n$ vertices. He decides to draw it using the following algorithm:</p><ul> <li> Step $0$: Draws the first vertex (vertex $1$). Go to step $1$. </li><li> Step $1$: For every edge in the input, in order: if the edge connects an already drawn vertex $u$ to an undrawn vertex $v$, he will draw the undrawn vertex $v$ and the edge. After checking every edge, go to step $2$. </li><li> Step $2$: If all the vertices are drawn, terminate the algorithm. Else, go to step $1$. </li></ul><p>The number of readings is defined as the number of times Copil Copac performs step $1$.</p><p>Find the number of readings needed by Copil Copac to draw the tree.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line of input contains a single integer $t$ ($1 \leq t \leq 10^4$)&nbsp;— the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2 \le n \le 2 \cdot 10^5$)&nbsp;— the number of vertices of the tree.</p><p>The following $n - 1$ lines of each test case contain two integers $u_i$ and $v_i$ ($1 \le u_i, v_i \le n$, $u_i \neq v_i$)&nbsp;— indicating that $(u_i,v_i)$ is the $i$-th edge in the list. It is guaranteed that the given edges form a tree.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output the number of readings Copil Copac needs to draw the tree.</p></div>

## Input

<p>Each test contains multiple test cases. The first line of input contains a single integer $t$ ($1 \leq t \leq 10^4$)&nbsp;— the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2 \le n \le 2 \cdot 10^5$)&nbsp;— the number of vertices of the tree.</p><p>The following $n - 1$ lines of each test case contain two integers $u_i$ and $v_i$ ($1 \le u_i, v_i \le n$, $u_i \neq v_i$)&nbsp;— indicating that $(u_i,v_i)$ is the $i$-th edge in the list. It is guaranteed that the given edges form a tree.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output the number of readings Copil Copac needs to draw the tree.</p>





```input1|2,3,4,5,6,7
2
6
4 5
1 3
1 2
3 4
1 6
7
5 6
2 4
2 7
1 3
1 2
4 5
```




```output1
2
3
```



## Note

<p>In the first test case:</p><p>After the first reading, the tree will look like this:</p><center> <img class="tex-graphics" src="file://dWPgjdlN.png" style="max-width: 100.0%;max-height: 100.0%;"> </center><p>After the second reading:</p><center> <img class="tex-graphics" src="file://0InKz45y.png" style="max-width: 100.0%;max-height: 100.0%;"> </center><p>Therefore, Copil Copac needs $2$ readings to draw the tree.</p>
