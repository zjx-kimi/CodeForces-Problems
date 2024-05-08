## Description

<div><p>All of Slavic's friends are planning to travel from the place where they live to a party using their bikes. And they all have a bike except Slavic. There are $n$ cities through which they can travel. They all live in the city $1$ and want to go to the party located in the city $n$. The map of cities can be seen as an undirected graph with $n$ nodes and $m$ edges. Edge $i$ connects cities $u_i$ and $v_i$ and has a length of $w_i$.</p><p>Slavic doesn't have a bike, but what he has is money. Every city has exactly one bike for sale. The bike in the $i$-th city has a slowness factor of $s_{i}$. Once Slavic buys a bike, he can use it <span class="tex-font-style-bf">whenever</span> to travel from the city he is currently in to any neighboring city, by taking $w_i \cdot s_j$ time, considering he is traversing edge $i$ using a bike $j$ he owns.</p><p>Slavic can buy as many bikes as he wants as money isn't a problem for him. Since Slavic hates traveling by bike, he wants to get from his place to the party in the shortest amount of time possible. And, since his informatics skills are quite rusty, he asks you for help.</p><p>What's the shortest amount of time required for Slavic to travel from city $1$ to city $n$? Slavic can't travel without a bike. It is guaranteed that it is possible for Slavic to travel from city $1$ to any other city.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \leq t \leq 100$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains two space-separated integers $n$ and $m$ ($2 \leq n \leq 1000$; $n - 1 \leq m \leq 1000$)&nbsp;— the number of cities and the number of roads, respectively.</p><p>The $i$-th of the following $m$ lines each contain three integers $u_i$, $v_i$, $w_i$ ($1 \le u_i, v_i \le n$, $u_i \neq v_i$; $1 \leq w_i \leq 10^5$), denoting that there is a road between cities $u_i$ and $v_i$ of length $w_i$. The same pair of cities can be connected by more than one road.</p><p>The next line contains $n$ integers $s_1, \ldots, s_n$ ($1 \leq s_i \leq 1000$)&nbsp;— the slowness factor of each bike.</p><p>The sum of $n$ over all test cases does not exceed $1000$, and the sum of $m$ over all test cases does not exceed $1000$.</p><p>Additional constraint on the input: it is possible to travel from city $1$ to any other city.</p></div><div class="output-specification"><p>For each test case, output a single integer denoting the shortest amount of time Slavic can reach city $n$ starting from city $1$.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \leq t \leq 100$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains two space-separated integers $n$ and $m$ ($2 \leq n \leq 1000$; $n - 1 \leq m \leq 1000$)&nbsp;— the number of cities and the number of roads, respectively.</p><p>The $i$-th of the following $m$ lines each contain three integers $u_i$, $v_i$, $w_i$ ($1 \le u_i, v_i \le n$, $u_i \neq v_i$; $1 \leq w_i \leq 10^5$), denoting that there is a road between cities $u_i$ and $v_i$ of length $w_i$. The same pair of cities can be connected by more than one road.</p><p>The next line contains $n$ integers $s_1, \ldots, s_n$ ($1 \leq s_i \leq 1000$)&nbsp;— the slowness factor of each bike.</p><p>The sum of $n$ over all test cases does not exceed $1000$, and the sum of $m$ over all test cases does not exceed $1000$.</p><p>Additional constraint on the input: it is possible to travel from city $1$ to any other city.</p>

## Output

<p>For each test case, output a single integer denoting the shortest amount of time Slavic can reach city $n$ starting from city $1$.</p>





```input1|2,3,4,5,6,7,8,21,22,23,24,25,26,27,28,29,30,31,32
3
5 5
1 2 2
3 2 1
2 4 5
2 5 7
4 5 1
5 2 1 3 3
5 10
1 2 5
1 3 5
1 4 4
1 5 8
2 3 6
2 4 3
2 5 2
3 4 1
3 5 8
4 5 2
7 2 8 4 1
7 10
3 2 8
2 1 4
2 5 7
2 6 4
7 1 2
4 3 5
6 4 2
6 7 1
6 7 4
4 5 9
7 6 5 4 3 2 1
```




```output1
19
36
14
```


