## Description

<div><p>One day, Pak Chanek who is already bored of being alone at home decided to go traveling. While looking for an appropriate place, he found that Londonesia has an interesting structure.</p><p>According to the information gathered by Pak Chanek, there are $N$ cities numbered from $1$ to $N$. The cities are connected to each other with $N-1$ two-directional roads, with the $i$-th road connecting cities $U_i$ and $V_i$, and taking a time of $W_i$ hours to be traversed. In other words, Londonesia's structure forms a tree.</p><p>Pak Chanek wants to go on a journey in Londonesia starting and ending in any city (not necessarily the same city) such that each city is visited <span class="tex-font-style-bf">at least once</span> with the least time possible. In order for the journey to end quicker, Pak Chanek also carries an instant teleportation device for moving from one city to any city that can only be used at most once. Help Pak Chanek for finding the minimum time needed.</p><p>Notes: </p><ul> <li> Pak Chanek only needs to visit each city at least once. Pak Chanek does not have to traverse each road. </li><li> In the journey, a city or a road can be visited more than once. </li></ul></div><div class="input-specification"><p>The first line contains a single integer $N$ ($1 \le N \le 10^5$) — the number of cities in Londonesia.</p><p>The $i$-th of the next $N-1$ lines contains three integers $U_i$, $V_i$, and $W_i$ ($1 \le U_i, V_i \le N$, $1 \le W_i \le 10^9$) — a two-directional road that connects cities $U_i$ and $V_i$ that takes $W_i$ hours to be traversed. The roads in Londonesia form a tree.</p></div><div class="output-specification"><p>Output one integer, which represents the minimum time in hours that is needed to visit each city at least once.</p></div>

## Input

<p>The first line contains a single integer $N$ ($1 \le N \le 10^5$) — the number of cities in Londonesia.</p><p>The $i$-th of the next $N-1$ lines contains three integers $U_i$, $V_i$, and $W_i$ ($1 \le U_i, V_i \le N$, $1 \le W_i \le 10^9$) — a two-directional road that connects cities $U_i$ and $V_i$ that takes $W_i$ hours to be traversed. The roads in Londonesia form a tree.</p>

## Output

<p>Output one integer, which represents the minimum time in hours that is needed to visit each city at least once.</p>





```input1
4
1 2 4
2 3 5
3 4 4
```




```input2
5
1 2 45
1 3 50
1 4 10
1 5 65
```




```output1
8
```




```output2
115
```



## Note

<p>In the first example, the journey that has the minimum time is $2 → 1 \xrightarrow{\text{teleport}} 4 → 3$.</p><p>In the second example, the journey that has the minimum time is $3 → 1 → 4 → 1 → 2 \xrightarrow{\text{teleport}} 5$.</p>
