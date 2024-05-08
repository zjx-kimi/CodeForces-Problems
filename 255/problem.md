## Description

<div><p><span class="tex-font-style-bf">The only differences between the two versions of this problem are the constraint on $k$, the time limit and the memory limit. You can make hacks only if all versions of the problem are solved.</span></p><p>Doremy lives in a rainy country consisting of $n$ cities numbered from $1$ to $n$.</p><p>The weather broadcast predicted the distribution of rain in the next $m$ days. In the $i$-th day, it will rain in the cities in the interval $[l_i, r_i]$. A city is called dry if it will never rain in that city in the next $m$ days.</p><p>It turns out that Doremy has a special power. She can choose $k$ days, and during these days it will not rain. Doremy wants to calculate the maximum number of dry cities after using the special power.</p></div><div class="input-specification"><p>The input consists of multiple test cases. The first line contains a single integer $t$ ($1\le t\le 10^4$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line contains three integers $n$, $m$ and $k$ ($1\le n\le 2\cdot 10^5$, $2 \le m \le 2\cdot 10^5$, $2 \le k \le \min(10, m)$)&nbsp;— the number of cities, the number of days, and the number of days of rain that Doremy can prevent.</p><p>Then, $m$ lines follow. The $i$-th line contains two integers $l_i$, $r_i$ ($1\le l_i\le r_i\le n$)&nbsp;— the rain coverage on day $i$.</p><p>It is guaranteed that the sum of $n$ and the sum of $m$ over all test cases do not exceed $2\cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output one integer&nbsp;— the maximum number of dry cities.</p></div>

## Input

<p>The input consists of multiple test cases. The first line contains a single integer $t$ ($1\le t\le 10^4$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line contains three integers $n$, $m$ and $k$ ($1\le n\le 2\cdot 10^5$, $2 \le m \le 2\cdot 10^5$, $2 \le k \le \min(10, m)$)&nbsp;— the number of cities, the number of days, and the number of days of rain that Doremy can prevent.</p><p>Then, $m$ lines follow. The $i$-th line contains two integers $l_i$, $r_i$ ($1\le l_i\le r_i\le n$)&nbsp;— the rain coverage on day $i$.</p><p>It is guaranteed that the sum of $n$ and the sum of $m$ over all test cases do not exceed $2\cdot 10^5$.</p>

## Output

<p>For each test case, output one integer&nbsp;— the maximum number of dry cities.</p>





```input1|2,3,4,5,10,11,12,13,14,15,16,24,25,26
6
2 3 2
1 2
1 2
1 1
5 3 2
1 3
2 4
3 5
10 6 4
1 5
6 10
2 2
3 7
5 8
1 4
100 6 5
1 100
1 100
1 100
1 100
1 100
1 100
1000 2 2
1 1
1 1
20 5 3
9 20
3 3
10 11
11 13
6 18
```




```output1
1
2
6
0
1000
17
```



## Note

<p>In the first test case, if Doremy prevents</p><ul> <li> rain $1,2$, then city $2$ will be dry; </li><li> rain $2,3$, then no city will be dry; </li><li> rain $1,3$, then no city will be dry; </li></ul><p>So there is at most $1$ dry city.</p><p>In the second test case, if Doremy prevents</p><ul> <li> rain $1,2$, then city $1,2$ will be dry; </li><li> rain $2,3$, then city $4,5$ will be dry; </li><li> rain $1,3$, then city $1,5$ will be dry. </li></ul><p>So there are at most $2$ dry cities.</p><p>In the third test case, it is optimal to prevent rain $1,2,4,5$.</p><p>In the forth test case, there is always a day of rain that wets all the cities and cannot be prevented.</p>
