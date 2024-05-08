## Description

<div><p>A compass points directly toward the morning star. It can only point in one of eight directions: the four cardinal directions (N, S, E, W) or some combination (NW, NE, SW, SE). Otherwise, it will break.</p><center> <img class="tex-graphics" src="file://le7iNWCZ.png" style="max-width: 100.0%;max-height: 100.0%;"> <span class="tex-font-size-small">The directions the compass can point.</span> </center><p>There are $n$ distinct points with integer coordinates on a plane. How many ways can you put a compass at one point and the morning star at another so that the compass does not break?</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^4$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2 \leq n \leq 2 \cdot 10^5$)&nbsp;— the number of points.</p><p>Then $n$ lines follow, each line containing two integers $x_i$, $y_i$ ($-10^9 \leq x_i, y_i \leq 10^9$)&nbsp;— the coordinates of each point, all points have distinct coordinates.</p><p>It is guaranteed that the sum of $n$ over all test cases doesn't exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output a single integer&nbsp;— the number of pairs of points that don't break the compass.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^4$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2 \leq n \leq 2 \cdot 10^5$)&nbsp;— the number of points.</p><p>Then $n$ lines follow, each line containing two integers $x_i$, $y_i$ ($-10^9 \leq x_i, y_i \leq 10^9$)&nbsp;— the coordinates of each point, all points have distinct coordinates.</p><p>It is guaranteed that the sum of $n$ over all test cases doesn't exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output a single integer&nbsp;— the number of pairs of points that don't break the compass.</p>





```input1|2,3,4,5,11,12,13,14,21,22,23,24
5
3
0 0
-1 -1
1 1
4
4 5
5 7
6 9
10 13
3
-1000000000 1000000000
0 0
1000000000 -1000000000
5
0 0
2 2
-1 5
-1 10
2 11
3
0 0
-1 2
1 -2
```




```output1
6
2
6
8
0
```



## Note

<p>In the first test case, any pair of points won't break the compass: </p><ul> <li> The compass is at $(0,0)$, the morning star is at $(-1,-1)$: the compass will point $\text{SW}$. </li><li> The compass is at $(0,0)$, the morning star is at $(1,1)$: the compass will point $\text{NE}$. </li><li> The compass is at $(-1,-1)$, the morning star is at $(0,0)$: the compass will point $\text{NE}$. </li><li> The compass is at $(-1,-1)$, the morning star is at $(1,1)$: the compass will point $\text{NE}$. </li><li> The compass is at $(1,1)$, the morning star is at $(0,0)$: the compass will point $\text{SW}$. </li><li> The compass is at $(1,1)$, the morning star is at $(-1,-1)$: the compass will point $\text{SW}$. </li></ul><p>In the second test case, only two pairs of points won't break the compass: </p><ul> <li> The compass is at $(6,9)$, the morning star is at $(10,13)$: the compass will point $\text{NE}$. </li><li> The compass is at $(10,13)$, the morning star is at $(6,9)$: the compass will point $\text{SW}$. </li></ul>
