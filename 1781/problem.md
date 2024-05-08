## Description

<div><p>Railway network of one city consists of $n$ stations connected by $n-1$ roads. These stations and roads forms a tree. Station $1$ is a city center. For each road you know the time trains spend to pass this road. You can assume that trains don't spend time on stops. Let's define $dist(v)$ as the time that trains spend to get from the station $v$ to the station $1$.</p><p>This railway network is splitted into zones named by first $k$ capital latin letters. The zone of the $i$-th station is $z_i$. City center is in the zone A. For all other stations it is guaranteed that the first station on the road from this station to the city center is either in the same zone or in the zone with lexicographically smaller name. Any road is completely owned by the zone of the most distant end from the city center.</p><p>Tourist will arrive at the airport soon and then he will go to the city center. Here's how the trip from station $v$ to station $1$ happends: </p><ul> <li> At the moment $0$, tourist enters the train that follows directly from the station $v$ to the station $1$. The trip will last for $dist(v)$ minutes. </li><li> Tourist can buy tickets for any subset of zones at any moment. Ticket for zone $i$ costs $pass_i$ euro. </li><li> Every $T$ minutes since the start of the trip (that is, at the moments $T, 2T, \ldots$) the control system will scan tourist. If at the moment of scan tourist is in the zone $i$ without zone $i$ ticket, he should pay $fine_i$ euro. Formally, the zone of tourist is determined in the following way: <ul> <li> If tourist is at the station $1$, then he already at the city center so he shouldn't pay fine. </li><li> If tourist is at the station $u \neq 1$, then he is in the zone $z_u$. </li><li> If tourist is moving from the station $x$ to the station $y$ that are directly connected by road, then he is in the zone $z_x$. </li></ul> Note, that tourist can pay fine multiple times in the same zone. </li></ul><p>Tourist always selects such way to buy tickets and pay fines that minimizes the total cost of trip. Let $f(v)$ be such cost for station $v$.</p><p>Unfortunately, tourist doesn't know the current values of $pass_i$ and $fine_i$ for different zones and he has forgot the location of the airport. He will ask you queries of $3$ types:</p><ul> <li> $1$ $i$ $c$&nbsp;— the cost of <span class="tex-font-style-bf">ticket</span> in zone $i$ has changed. Now $pass_i$ is $c$. </li><li> $2$ $i$ $c$&nbsp;— the cost of <span class="tex-font-style-bf">fine</span> in zone $i$ has changed. Now $fine_i$ is $c$. </li><li> $3$ $u$&nbsp;— solve the following problem for current values of $pass$ and $fine$: <ul> <li> You are given the station $u$. Consider all the stations $v$ that satisfy the following conditions: <ul> <li> $z_v = z_u$ </li><li> The station $u$ is on the path from the station $v$ to the station $1$. </li></ul> Find the value of $\min(f(v))$ over all such stations $v$ with the following assumption: <span class="tex-font-style-bf">tourist has the ticket for the zone of station</span> $z_u$. </li></ul> </li></ul></div><div class="input-specification"><p>The first line contains the single integer $n$ ($2 \leq n \leq 2 \cdot 10^5$)&nbsp;— the number of stations.</p><p>Each of the next $n - 1$ lines contains three integers $v_i$, $u_i$, $t_i$ ($1 \leq v_i, u_i \leq n, 1 \leq t_i \leq 10^9$)&nbsp;— the ends of the $i$-th road and the time it takes a train to pass this road. It is guaranteed that this roads forms a tree.</p><p>The next line contains the single integer $k$ ($1 \leq k \leq 26$)&nbsp;— the number of zones.</p><p>The next line contains $n$ symbols $z_1z_2 \ldots z_n$&nbsp;— $z_i$ is the name of the zone of the $i$-th station. It is guaranteed that the conditions from the second paragraph are satisfied.</p><p>The next line contains $k$ integers $pass_1$, $pass_2$, $\ldots$, $pass_k$ ($1 \leq pass_i \leq 10^9$)&nbsp;— initial costs of tickets.</p><p>The next line contains $k$ integers $fine_1$, $fine_2$, $\ldots$, $fine_k$ ($1 \leq fine_i \leq 10^9$)&nbsp;— initial fines.</p><p>The next line contains the single integer $T$ ($1 \leq T \leq 10^9$)&nbsp;— the time gap between scans of control system.</p><p>The next line contains the single integer $q$ ($1 \leq q \leq 2 \cdot 10^5$)&nbsp;— the number of queries.</p><p>Next $q$ lines contains queries as described in the statement. It is guaranteed that in the queries of the first and the second type $i$ is a correct name of the zone (one of the first $k$ capital latin letters) and $1 \leq c \leq 10^9$, and in the queries of the third type $1 \leq u \leq n$.</p></div><div class="output-specification"><p>For each query of the third type print the answer to it.</p></div>

## Input

<p>The first line contains the single integer $n$ ($2 \leq n \leq 2 \cdot 10^5$)&nbsp;— the number of stations.</p><p>Each of the next $n - 1$ lines contains three integers $v_i$, $u_i$, $t_i$ ($1 \leq v_i, u_i \leq n, 1 \leq t_i \leq 10^9$)&nbsp;— the ends of the $i$-th road and the time it takes a train to pass this road. It is guaranteed that this roads forms a tree.</p><p>The next line contains the single integer $k$ ($1 \leq k \leq 26$)&nbsp;— the number of zones.</p><p>The next line contains $n$ symbols $z_1z_2 \ldots z_n$&nbsp;— $z_i$ is the name of the zone of the $i$-th station. It is guaranteed that the conditions from the second paragraph are satisfied.</p><p>The next line contains $k$ integers $pass_1$, $pass_2$, $\ldots$, $pass_k$ ($1 \leq pass_i \leq 10^9$)&nbsp;— initial costs of tickets.</p><p>The next line contains $k$ integers $fine_1$, $fine_2$, $\ldots$, $fine_k$ ($1 \leq fine_i \leq 10^9$)&nbsp;— initial fines.</p><p>The next line contains the single integer $T$ ($1 \leq T \leq 10^9$)&nbsp;— the time gap between scans of control system.</p><p>The next line contains the single integer $q$ ($1 \leq q \leq 2 \cdot 10^5$)&nbsp;— the number of queries.</p><p>Next $q$ lines contains queries as described in the statement. It is guaranteed that in the queries of the first and the second type $i$ is a correct name of the zone (one of the first $k$ capital latin letters) and $1 \leq c \leq 10^9$, and in the queries of the third type $1 \leq u \leq n$.</p>

## Output

<p>For each query of the third type print the answer to it.</p>





```input1
8
1 2 7
2 3 4
2 4 3
4 5 1
5 6 6
4 7 10
6 8 6
4
AABABBDB
11 12 10 42
16 15 15 30
4
6
3 2
1 A 10
3 3
2 A 3
3 7
3 6
```




```output1
0
10
6
6
```



## Note

<p>Note, that the fine can be cheaper than the pass.</p><center> <img class="tex-graphics" src="file://2h9ZUAkC.png" style="max-width: 100.0%;max-height: 100.0%;"> <span class="tex-font-size-small">The railway network from the example. Green color is used for stations and roads of zone A, blue color is used for zone B and red color is used for zone D. The integer near each road is time that trains spend to pass it.</span> </center><p>In the first query, the airport can be located near the station $2$ or near the station $4$. During the trip, tourist will always stay in the zone <span class="tex-font-style-tt">A</span>. He already has the pass for this zone so the answer is $0$.</p><p>After the second query, the cost of the pass in the zone <span class="tex-font-style-tt">A</span> has become $10$.</p><p>In the third query, the airport can be located only near the station $3$. Optimal solution will be to buy the pass for zone <span class="tex-font-style-tt">A</span>. During the first $3$ seconds of trip tourist will be in the zone <span class="tex-font-style-tt">B</span>. Then he will move to the zone <span class="tex-font-style-tt">A</span> and will be scanned there on the $4$-th and the $8$-th second of his ride. Since he have a pass for this zone, he won't pay fines.</p><p>After the forth query, the fine in the zone <span class="tex-font-style-tt">A</span> has become $3$.</p><p>In the fifth query, the airport can be located only near the station $7$ and $f(7) = 6$.</p><p>In the sixth query, the airport can be located near the station $6$ or near the station $8$. Since $f(6)=9$ and $f(8)=6$ the answer is $6$.</p>
