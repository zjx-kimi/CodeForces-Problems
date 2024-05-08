## Description

<div><p>Vlad found a flowerbed with graphs in his yard and decided to take one for himself. Later he found out that in addition to the usual graphs, $k$-flowers also grew on that flowerbed. A graph is called a $k$-flower if it consists of a simple cycle of length $k$, through each vertex of which passes its own simple cycle of length $k$ and these cycles do not intersect at the vertices. For example, $3$-flower looks like this:</p><center> <img class="tex-graphics" src="file://FRqCpg5b.png" style="max-width: 100.0%;max-height: 100.0%;" width="454px"> </center><p>Note that $1$-flower and $2$-flower do not exist, since at least $3$ vertices are needed to form a cycle.</p><p>Vlad really liked the structure of the $k$-flowers and now he wants to find out if he was lucky to take one of them from the flowerbed.</p></div><div class="input-specification"><p>The first line of input contains the single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases in the test.</p><p>The descriptions of the cases follow. An empty string is written before each case.</p><p>The first line of each case contains two integers $n$ and $m$ ($2 \le n \le 2 \cdot 10^5$, $1 \le m \le \min(2 \cdot 10^5, \frac{n \cdot (n-1)}{2})$) — the number of vertices and edges in the graph, respectively.</p><p>The next $m$ lines contain two integers each $u$ and $v$ ($1 \le u, v \le n$, $u \ne v$) — numbers of vertices connected by an edge. It is guaranteed that the graph does not contain multiple edges and self-loops.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$. It is also guaranteed for the sum of $m$ over all test cases.</p></div><div class="output-specification"><p>Output $t$ lines, each of which is the answer to the corresponding test case. As an answer, output "<span class="tex-font-style-tt">YES</span>" if Vlad's graph is a $k$-flower for some $k$, and "<span class="tex-font-style-tt">NO</span>" otherwise.</p><p>You can output the answer in any case (for example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>" and "<span class="tex-font-style-tt">YES</span>" will be recognized as a positive answer).</p></div>

## Input

<p>The first line of input contains the single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases in the test.</p><p>The descriptions of the cases follow. An empty string is written before each case.</p><p>The first line of each case contains two integers $n$ and $m$ ($2 \le n \le 2 \cdot 10^5$, $1 \le m \le \min(2 \cdot 10^5, \frac{n \cdot (n-1)}{2})$) — the number of vertices and edges in the graph, respectively.</p><p>The next $m$ lines contain two integers each $u$ and $v$ ($1 \le u, v \le n$, $u \ne v$) — numbers of vertices connected by an edge. It is guaranteed that the graph does not contain multiple edges and self-loops.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$. It is also guaranteed for the sum of $m$ over all test cases.</p>

## Output

<p>Output $t$ lines, each of which is the answer to the corresponding test case. As an answer, output "<span class="tex-font-style-tt">YES</span>" if Vlad's graph is a $k$-flower for some $k$, and "<span class="tex-font-style-tt">NO</span>" otherwise.</p><p>You can output the answer in any case (for example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>" and "<span class="tex-font-style-tt">YES</span>" will be recognized as a positive answer).</p>





```input1|2,3,4,5,6,7,8,9,10,11,12,13,14,15,30,31,32,33,34,45,46,47,48,49,50,51,52,53
5
<br>
9 12
1 2
3 1
2 3
1 6
4 1
6 4
3 8
3 5
5 8
9 7
2 9
7 2
<br>
8 12
1 2
3 1
2 3
1 6
4 1
6 4
3 8
3 5
5 8
8 7
2 8
7 2
<br>
4 3
1 2
4 2
3 1
<br>
6 8
6 3
6 4
5 3
5 2
3 2
3 1
2 1
2 4
<br>
5 7
2 4
2 5
3 4
3 5
4 1
4 5
1 5
```




```input2|2,3,4,16,17,18,19,20,21,22,23,24,25,26,27,28,29
4
<br>
2 1
1 2
<br>
8 9
1 2
8 4
8 2
6 4
6 5
4 7
3 2
3 7
2 5
<br>
9 12
2 9
2 8
6 9
6 8
6 5
6 1
9 8
9 3
9 1
8 3
8 7
5 7
<br>
3 3
1 2
1 3
2 3
```




```output1
YES
NO
NO
NO
NO
```




```output2
NO
NO
NO
NO
```


