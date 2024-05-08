## Description

<div><p>Because the railway system in Gensokyo is often congested, as an enthusiastic engineer, Kawasiro Nitori plans to construct more railway to ease the congestion.</p><p>There are $n$ stations numbered from $1$ to $n$ and $m$ two-way railways in Gensokyo. Every two-way railway connects two different stations and has a positive integer length $d$. No two two-way railways connect the same two stations. Besides, it is possible to travel from any station to any other using those railways. Among these $n$ stations, station $1$ is the main station. You can get to any station from any other station using only two-way railways.</p><p>Because of the technological limitation, Nitori can only construct one-way railways, whose length can be arbitrary positive integer. Constructing a one-way railway from station $u$ will costs $w_u$ units of resources, no matter where the railway ends. To ease the congestion, Nitori plans that after construction there are at least two shortest paths from station $1$ to any other station, and these two shortest paths do not pass the same station except station $1$ and the terminal. Besides, Nitori also does not want to change the distance of the shortest path from station $1$ to any other station.</p><p>Due to various reasons, sometimes the cost of building a new railway will increase uncontrollably. There will be a total of $q$ occurrences of this kind of incident, and the $i$-th event will add additional amount of $x_i$ to the cost of building a new railway from the station $k_i$.</p><p>To save resources, before all incidents and after each incident, Nitori wants you to help her calculate the minimal cost of railway construction.</p></div><div class="input-specification"><p>The first line contains three integers $n$, $m$, and $q$ ($1 \le n \le 2 \cdot 10^5$, $1 \le m \le 3 \cdot 10^5$, $0 \le q \le 2\cdot10^5$).</p><p>The second line contains $n$ integers $w_1,w_2,\ldots,w_n$ ($1 \le w_i \le 10^9$).</p><p>Each of the next $m$ lines contains three integers $u$, $v$, $d$ ($1 \le u,v \le n$, $u \ne v$, $1 \le d \le 10^9$), denoting a two-way railway connecting station $u$ and station $v$, with length $d$.</p><p>The $i$-th of the next $q$ lines contains two integers $k_i,x_i$ ($1 \le k_i \le n, 1 \le x_i \le 4 \times 10^8$).</p></div><div class="output-specification"><p>Print $q+1$ lines, and the $i$-th of these lines contains one integer, denoting the minimal cost of railway construction after the $i-1$-th incident (especially, the $0$-th incident means no incident occurred).</p></div>

## Input

<p>The first line contains three integers $n$, $m$, and $q$ ($1 \le n \le 2 \cdot 10^5$, $1 \le m \le 3 \cdot 10^5$, $0 \le q \le 2\cdot10^5$).</p><p>The second line contains $n$ integers $w_1,w_2,\ldots,w_n$ ($1 \le w_i \le 10^9$).</p><p>Each of the next $m$ lines contains three integers $u$, $v$, $d$ ($1 \le u,v \le n$, $u \ne v$, $1 \le d \le 10^9$), denoting a two-way railway connecting station $u$ and station $v$, with length $d$.</p><p>The $i$-th of the next $q$ lines contains two integers $k_i,x_i$ ($1 \le k_i \le n, 1 \le x_i \le 4 \times 10^8$).</p>

## Output

<p>Print $q+1$ lines, and the $i$-th of these lines contains one integer, denoting the minimal cost of railway construction after the $i-1$-th incident (especially, the $0$-th incident means no incident occurred).</p>





```input1
5 5 1
1 1 1 1 1
1 2 1
2 3 1
2 4 1
3 5 1
4 5 1
1 2
```




```input2
8 11 0
14 4 16 15 1 3 1 14
4 2 1
1 2 3
7 5 4
2 3 1
8 6 2
8 5 5
5 4 5
7 6 7
3 5 5
1 6 6
8 1 4
```




```input3
10 16 8
29 1 75 73 51 69 24 17 1 97
1 2 18
2 3 254
2 4 546
2 5 789
5 6 998
6 7 233
7 8 433
1 9 248
5 10 488
2 6 1787
10 8 1176
3 8 2199
4 8 1907
2 10 1277
4 10 731
9 10 1047
1 11
1 9
8 8
1 3
2 19
9 5
9 4
7 6
```




```output1
3
9
```




```output2
46
```




```output3
34
45
54
54
57
76
96
112
112
```



## Note

<p>In the second example, Nitori can build railways as follows: $1 \rightarrow 2$, $1 \rightarrow 3$, $1 \rightarrow 4$, $2 \rightarrow 8$, and the cost is $14 + 14 + 14 + 4 = 46$.</p>
