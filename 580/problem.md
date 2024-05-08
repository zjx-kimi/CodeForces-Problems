## Description

<div><p>You are given $n$ intervals and $m$ points on the number line. The $i$-th intervals covers coordinates $[l_i,r_i]$ and the $i$-th point is on coordinate $i$ and has coefficient $p_i$.</p><p>Initially, all points are not activated. You should choose a subset of the $m$ points to activate. For each of $n$ interval, we define its <span class="tex-font-style-it">cost</span> as: </p><ul> <li> $0$, if there are no activated points in the interval; </li><li> the coefficient of the activated point with the <span class="tex-font-style-bf">largest coordinate</span> within it, otherwise. </li></ul><p>Your task is to maximize the sum of the costs of all intervals by choosing which points to activate.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line of input contains a single integer $t$ ($1 \le t \le 10^5$)&nbsp;— the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains two integers $n$ and $m$ ($1 \le n \le 10^6, 1 \le m \le 10^6$)&nbsp;— the number of intervals and the number of points.</p><p>The following $n$ lines of each test case contains two integers $l_i$ and $r_i$ ($1 \le l_i \le r_i \le m$)&nbsp;— the endpoints of the $i$-th interval.</p><p>The following line of each test case contains $m$ integers $p_1,p_2,\ldots,p_m$ ($0 \le p_i \le 10^9$)&nbsp;— the coefficients of the points.</p><p>It is guaranteed that the sum of $n$ does not exceed $10^6$ and the sum of $m$ does not exceed $10^6$.</p></div><div class="output-specification"><p>Output the maximum possible sum of costs of all intervals.</p></div>

## Input

<p>Each test contains multiple test cases. The first line of input contains a single integer $t$ ($1 \le t \le 10^5$)&nbsp;— the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains two integers $n$ and $m$ ($1 \le n \le 10^6, 1 \le m \le 10^6$)&nbsp;— the number of intervals and the number of points.</p><p>The following $n$ lines of each test case contains two integers $l_i$ and $r_i$ ($1 \le l_i \le r_i \le m$)&nbsp;— the endpoints of the $i$-th interval.</p><p>The following line of each test case contains $m$ integers $p_1,p_2,\ldots,p_m$ ($0 \le p_i \le 10^9$)&nbsp;— the coefficients of the points.</p><p>It is guaranteed that the sum of $n$ does not exceed $10^6$ and the sum of $m$ does not exceed $10^6$.</p>

## Output

<p>Output the maximum possible sum of costs of all intervals.</p>





```input1|2,3,4,5
2
2 8
1 5
3 8
78 0 50 0 0 0 0 30
1 6
1 5
0 0 0 0 0 100
```




```output1
108
0
```



## Note

<p>In the first sample, we can activate points $1$ and $8$. The sum of costs of all intervals will be $78+30=108$.</p><p>In the second sample, we will activate no points. The sum of costs of all intervals will be $0$.</p>
