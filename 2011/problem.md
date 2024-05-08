## Description

<div><p>There are $n$ villages lying equidistant on a circle in the middle of a thick, impassable forest. From ancient times, it was impossible to move from one village to another, but technical progress has changed a lot. Now, there is a technology to build passable trails in the forest. </p><p>The building process consists of $m$ events. Each event is either building a trail or querying if two villages are connected. Trails are built as straight lines connecting two villages. After a trail is built, anybody can walk along the trail from one village to another. </p><p>Moreover, if two trails cross, anybody can turn at the intersection, and if other trails leave a village you have just reached, they can also be used to walk along. So, for example, if villages are numbered $1$ to $6$ in the order around the circle, and there are trails $1$ to $3$, $2$ to $4$, and $4$ to $6$, then all villages, except the $5$-th, are reachable from the $1$-st village.</p><p>Given a list of $m$ events, for each query, find if two given villages are reachable from each other at that moment.</p></div><div class="input-specification"><p>The first line contains two integers $n$ ($2 \le n \le 2\cdot 10^5$) and $m$ ($1 \le m \le 3\cdot 10^5$)&nbsp;— the number of villages and the number of events respectively. </p><p>Next $m$ lines contain events. Each event description consists of three integers $e$ ($e$ is $1$ or $2$), $v$ ($1 \le v \le n$), and $u$ ($1 \le u \le n$, $u \ne v$). If $e = 1$, then the event is building a trail between villages $v$ and $u$. If $e = 2$, then the event is a query if the villages $v$ and $u$ are connected. It is guaranteed that each trail is built at most once. </p><p>Villages are numbered $1$ to $n$ in clockwise order around the circle. </p></div><div class="output-specification"><p>For each query print one character '<span class="tex-font-style-tt">0</span>' if villages are not reachable, and '<span class="tex-font-style-tt">1</span>' if villages are reachable from each other. Print answers for all queries as a single string in one line.</p></div>

## Input

<p>The first line contains two integers $n$ ($2 \le n \le 2\cdot 10^5$) and $m$ ($1 \le m \le 3\cdot 10^5$)&nbsp;— the number of villages and the number of events respectively. </p><p>Next $m$ lines contain events. Each event description consists of three integers $e$ ($e$ is $1$ or $2$), $v$ ($1 \le v \le n$), and $u$ ($1 \le u \le n$, $u \ne v$). If $e = 1$, then the event is building a trail between villages $v$ and $u$. If $e = 2$, then the event is a query if the villages $v$ and $u$ are connected. It is guaranteed that each trail is built at most once. </p><p>Villages are numbered $1$ to $n$ in clockwise order around the circle. </p>

## Output

<p>For each query print one character '<span class="tex-font-style-tt">0</span>' if villages are not reachable, and '<span class="tex-font-style-tt">1</span>' if villages are reachable from each other. Print answers for all queries as a single string in one line.</p>





```input1
6 9
1 1 3
1 4 6
2 3 4
1 2 4
2 1 2
2 1 3
2 1 4
2 6 1
2 5 3
```




```input2
2 5
2 1 2
2 2 1
1 1 2
2 1 2
2 2 1
```




```output1
011110
```




```output2
0011
```


