## Description

<div><p>There are $n$ cities and $m$ bidirectional roads in Berland. The $i$-th road connects the cities $x_i$ and $y_i$, and has the speed limit $s_i$. The road network allows everyone to get from any city to any other city. </p><p>The Berland Transport Ministry is planning a road reform.</p><p>First of all, maintaining all $m$ roads is too costly, so $m - (n - 1)$ roads will be demolished in such a way that the remaining $(n - 1)$ roads still allow to get to any city from any other city. Formally, the remaining roads should represent an undirected tree.</p><p>Secondly, the speed limits on the remaining roads might be changed. The changes will be done sequentially, each change is either increasing the speed limit on some road by $1$, or decreasing it by $1$. Since changing the speed limit requires a lot of work, the Ministry wants to minimize the number of changes.</p><p>The goal of the Ministry is to have a road network of $(n - 1)$ roads with the maximum speed limit over all roads equal to exactly $k$. They assigned you the task of calculating the minimum number of speed limit changes they have to perform so the road network meets their requirements.</p><p>For example, suppose the initial map of Berland looks like that, and $k = 7$:</p><center> <img class="tex-graphics" src="file://Tkn5RN3G.png" style="max-width: 100.0%;max-height: 100.0%;"> </center><p>Then one of the optimal courses of action is to demolish the roads $1$–$4$ and $3$–$4$, and then decrease the speed limit on the road $2$–$3$ by $1$, so the resulting road network looks like that:</p><center> <img class="tex-graphics" src="file://dAiIGN3j.png" style="max-width: 100.0%;max-height: 100.0%;"> </center></div><div class="input-specification"><p>The first line contains one integer $t$ ($1 \le t \le 1000$) — the number of test cases.</p><p>The first line of each test case contains three integers $n$, $m$ and $k$ ($2 \le n \le 2 \cdot 10^5$; $n - 1 \le m \le \min(2 \cdot 10^5, \frac{n(n-1)}{2})$; $1 \le k \le 10^9$) — the number of cities, the number of roads and the required maximum speed limit, respectively.</p><p>Then $m$ lines follow. The $i$-th line contains three integers $x_i$, $y_i$ and $s_i$ ($1 \le x_i, y_i \le n$; $x_i \ne y_i$; $1 \le s_i \le 10^9$) — the cities connected by the $i$-th road and the speed limit on it, respectively. All roads are bidirectional.</p><p>The road network in each test case is connected (that is, it is possible to reach any city from any other city by traveling along the road), and each pair of cities is connected by at most one road.</p><p>The sum of $n$ over all test cases does not exceed $2 \cdot 10^5$. Similarly, the sum of $m$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, print one integer — the minimum number of changes the Ministry has to perform so that the maximum speed limit among the remaining $(n - 1)$ roads is exactly $k$.</p></div>

## Input

<p>The first line contains one integer $t$ ($1 \le t \le 1000$) — the number of test cases.</p><p>The first line of each test case contains three integers $n$, $m$ and $k$ ($2 \le n \le 2 \cdot 10^5$; $n - 1 \le m \le \min(2 \cdot 10^5, \frac{n(n-1)}{2})$; $1 \le k \le 10^9$) — the number of cities, the number of roads and the required maximum speed limit, respectively.</p><p>Then $m$ lines follow. The $i$-th line contains three integers $x_i$, $y_i$ and $s_i$ ($1 \le x_i, y_i \le n$; $x_i \ne y_i$; $1 \le s_i \le 10^9$) — the cities connected by the $i$-th road and the speed limit on it, respectively. All roads are bidirectional.</p><p>The road network in each test case is connected (that is, it is possible to reach any city from any other city by traveling along the road), and each pair of cities is connected by at most one road.</p><p>The sum of $n$ over all test cases does not exceed $2 \cdot 10^5$. Similarly, the sum of $m$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, print one integer — the minimum number of changes the Ministry has to perform so that the maximum speed limit among the remaining $(n - 1)$ roads is exactly $k$.</p>





```input1
4
4 5 7
4 1 3
1 2 5
2 3 8
2 4 1
3 4 4
4 6 5
1 2 1
1 3 1
1 4 2
2 4 1
4 3 1
3 2 1
3 2 10
1 2 8
1 3 10
5 5 15
1 2 17
3 1 15
2 3 10
1 4 14
2 5 8
```




```output1
1
3
0
0
```



## Note

<p>The explanation for the example test:</p><p>The first test case is described in the problem statement.</p><p>In the second test case, the road network initially looks like that:</p><center> <img class="tex-graphics" src="file://LVAWmgMe.png" style="max-width: 100.0%;max-height: 100.0%;"> </center><p>The Ministry can demolish the roads $1$–$2$, $3$–$2$ and $3$–$4$, and then increase the speed limit on the road $1$–$4$ three times.</p><p>In the third test case, the road network already meets all the requirements.</p><p>In the fourth test case, it is enough to demolish the road $1$–$2$ so the resulting road network meets the requirements.</p>
