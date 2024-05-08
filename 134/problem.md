## Description

<div><div class="epigraph"><div class="epigraph-text"><span class="tex-font-style-it"><a href="https://soundcloud.com/iceloki/entrance-deemo">Deemo - Entrance</a></span></div><div class="epigraph-source">⠀</div></div><p>You are located at the point $(0, 0)$ of an infinite Cartesian plane. You have a controller with $4$ buttons which can perform one of the following operations:</p><ul> <li> $\texttt{U}$: move from $(x, y)$ to $(x, y+1)$; </li><li> $\texttt{R}$: move from $(x, y)$ to $(x+1, y)$; </li><li> $\texttt{D}$: move from $(x, y)$ to $(x, y-1)$; </li><li> $\texttt{L}$: move from $(x, y)$ to $(x-1, y)$. </li></ul><p>Unfortunately, the controller is broken. If you press all the $4$ buttons (in any order), the controller stops working. It means that, during the whole trip, you can only press at most $3$ distinct buttons (any number of times, in any order).</p><p>There are $n$ special points in the plane, with integer coordinates $(x_i, y_i)$.</p><p>Can you visit all the special points (in any order) without breaking the controller?</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 1000$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 100$)&nbsp;— the number of special points.</p><p>Each of the next $n$ lines contains two integers $x_i$, $y_i$ ($-100 \leq x_i, y_i \leq 100$), which represent the special point $(x_i, y_i)$.</p><p>Note that there are no constraints on the sum of $n$ over all test cases.</p></div><div class="output-specification"><p>For each test case, output "<span class="tex-font-style-tt">YES</span>" (without quotes), if you can reach all the special points without breaking the controller, and "<span class="tex-font-style-tt">NO</span>" (without quotes) otherwise.</p><p>You may output each letter in any case (for example, "<span class="tex-font-style-tt">YES</span>", "<span class="tex-font-style-tt">Yes</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">yEs</span>" will all be recognized as positive answer).</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 1000$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 100$)&nbsp;— the number of special points.</p><p>Each of the next $n$ lines contains two integers $x_i$, $y_i$ ($-100 \leq x_i, y_i \leq 100$), which represent the special point $(x_i, y_i)$.</p><p>Note that there are no constraints on the sum of $n$ over all test cases.</p>

## Output

<p>For each test case, output "<span class="tex-font-style-tt">YES</span>" (without quotes), if you can reach all the special points without breaking the controller, and "<span class="tex-font-style-tt">NO</span>" (without quotes) otherwise.</p><p>You may output each letter in any case (for example, "<span class="tex-font-style-tt">YES</span>", "<span class="tex-font-style-tt">Yes</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">yEs</span>" will all be recognized as positive answer).</p>





```input1|2,3,4,5,11,12,13,14,15,23,24,25,26,27,28,29
6
3
1 -1
0 0
1 -1
4
-3 -2
-3 -1
-3 0
-3 1
4
1 1
-1 -1
1 -1
-1 1
6
-4 14
-9 -13
-14 5
14 15
-8 -4
19 9
6
82 64
39 91
3 46
87 83
74 21
7 25
1
100 -100
```




```output1
YES
YES
NO
NO
YES
YES
```



## Note

<p>In the first test case, you can move as follows: </p><ul> <li> you start from $(0, 0)$; </li><li> you visit the special point $(x_2, y_2) = (0, 0)$; </li><li> you press $\texttt{R}$, and you move from $(0, 0)$ to $(1, 0)$; </li><li> you press $\texttt{D}$, and you move from $(1, 0)$ to $(1, -1)$; </li><li> you visit the special point $(x_1, y_1) = (1, -1)$; </li><li> you visit the special point $(x_3, y_3) = (1, -1)$. </li></ul><p>Therefore, you can visit all the special points using only the buttons $\texttt{R}$, $\texttt{D}$, so the controller does not break.</p><p>Note that the special points may coincide.</p><p>In the second test case, you can show that you can visit all the special points using only the buttons $\texttt{U}$, $\texttt{D}$, $\texttt{L}$.</p><p>In the third test case, you can show that you must press all the buttons ($\texttt{U}$, $\texttt{R}$, $\texttt{D}$, $\texttt{L}$) to visit all the points, so the controller would break.</p>
