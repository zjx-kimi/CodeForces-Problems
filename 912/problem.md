## Description

<div><p>There are $n$ big cities in Italy, and there are $m$ train routes between pairs of cities. Each route connects two different cities bidirectionally. Moreover, using the trains one can reach every city starting from any other city.</p><p>Right now, all the routes are operated by the government-owned Italian Carriage Passenger Company, but the government wants to privatize the routes. The government does not want to give too much power to a single company, but it also does not want to make people buy a lot of different subscriptions. Also, it would like to give a fair chance to all companies. In order to formalize all these wishes, the following model was proposed.</p><p>There will be $k \ge 2$ private companies indexed by $1, \, 2, \, \dots, \, k$. Each train route will be operated by exactly one of the $k$ companies. Then:</p><ul> <li> For any company, there should exist two cities such that it is impossible to reach one from the other using only routes operated by that company. </li><li> On the other hand, for any two companies, it should be possible to reach every city from any other city using only routes operated by these two companies. </li></ul><p>Find a plan satisfying all these criteria. It can be shown that a viable plan always exists. Please note that you can choose the number $k$ and you do not have to minimize or maximize it.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains an integer $t$ ($1 \le t \le 1000$) — the number of test cases. The descriptions of the $t$ test cases follow.</p><p>The first line of each test case contains two integers $n$ and $m$ ($3 \le n \le 50$, $n-1 \le m \le n(n-1)/2$) — the number of cities and the number of train routes.</p><p>The next $m$ lines contain two integers $u_i$ and $v_i$ each ($1 \le u_i, v_i \le n$, $u_i \ne v_i$) — the $i$-th train route connects cities $u_i$ and $v_i$.</p><p>It is guaranteed that the routes connect $m$ distinct pairs of cities. It is guaranteed that using the trains one can reach every city starting from any other city.</p><p>The sum of the values of $n$ over all test cases does not exceed $5000$.</p></div><div class="output-specification"><p>For each test case, on the first line print an integer $k$ ($2 \le k \le m$) — the number of companies in your plan; on the second line print $m$ integers $c_1, \, c_2, \, \dots, \, c_m$ ($1 \le c_i \le k$) — in your plan company $c_i$ operates the $i$-th route.</p><p>If there are multiple valid plans, you may print any of them.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains an integer $t$ ($1 \le t \le 1000$) — the number of test cases. The descriptions of the $t$ test cases follow.</p><p>The first line of each test case contains two integers $n$ and $m$ ($3 \le n \le 50$, $n-1 \le m \le n(n-1)/2$) — the number of cities and the number of train routes.</p><p>The next $m$ lines contain two integers $u_i$ and $v_i$ each ($1 \le u_i, v_i \le n$, $u_i \ne v_i$) — the $i$-th train route connects cities $u_i$ and $v_i$.</p><p>It is guaranteed that the routes connect $m$ distinct pairs of cities. It is guaranteed that using the trains one can reach every city starting from any other city.</p><p>The sum of the values of $n$ over all test cases does not exceed $5000$.</p>

## Output

<p>For each test case, on the first line print an integer $k$ ($2 \le k \le m$) — the number of companies in your plan; on the second line print $m$ integers $c_1, \, c_2, \, \dots, \, c_m$ ($1 \le c_i \le k$) — in your plan company $c_i$ operates the $i$-th route.</p><p>If there are multiple valid plans, you may print any of them.</p>





```input1|2,3,4,5,6,7,8,9,10,11
2
5 9
1 2
1 3
1 4
1 5
2 3
2 4
2 5
3 4
3 5
3 3
1 2
3 1
2 3
```




```output1
4
1 2 3 1 4 2 2 4 3
3
2 3 1
```



## Note

<p>In the <span class="tex-font-style-bf">first test case</span>, the output is illustrated in the following picture, where different colors correspond to different companies (blue for $1$, red for $2$, green for $3$, and yellow for $4$):</p><center> <img class="tex-graphics" src="file://9rQcUejj.png" style="max-width: 100.0%;max-height: 100.0%;"> </center><p>If we consider, for example, only companies $2$ and $3$, we can see that from any city it is possible to reach every other city (picture on the left below). However, if we restrict to company $2$ alone, it becomes impossible to reach city $5$ from city $1$ (picture on the right).</p><center> <img class="tex-graphics" src="file://cUV6HGHe.png" style="max-width: 100.0%;max-height: 100.0%;"> </center><p>In the <span class="tex-font-style-bf">second test case</span>, the output is illustrated in the following picture:</p><center> <img class="tex-graphics" src="file://kjgqGT8l.png" style="max-width: 100.0%;max-height: 100.0%;"> </center>
