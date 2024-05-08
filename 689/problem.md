## Description

<div><p>There are $n$ cities in Berland, arranged in a circle and numbered from $1$ to $n$ in clockwise order.</p><p>You want to travel all over Berland, starting in some city, visiting all the other cities and returning to the starting city. Unfortunately, you can only drive along the Berland Ring Highway, which connects all $n$ cities. The road was designed by a very titled and respectable minister, so it is one-directional&nbsp;— it can only be traversed clockwise, only from the city $i$ to the city $(i \bmod n) + 1$ (i.e. from $1$ to $2$, from $2$ in $3$, ..., from $n$ to $1$).</p><p>The fuel tank of your car holds up to $k$ liters of fuel. To drive from the $i$-th city to the next one, $a_i$ liters of fuel are needed (and are consumed in the process).</p><p>Every city has a fuel station; a liter of fuel in the $i$-th city costs $b_i$ burles. Refueling between cities is not allowed; if fuel has run out between cities, then your journey is considered incomplete.</p><p>For each city, calculate the minimum cost of the journey if you start and finish it in that city.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains two integers $n$ and $k$ ($3 \le n \le 2 \cdot 10^5$; $1 \le k \le 10^9$)&nbsp;— the number of cities and the volume of fuel tank, respectively.</p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le k$).</p><p>The third line contains $n$ integers $b_1, b_2, \dots, b_n$ ($1 \le b_i \le 2$).</p><p>The sum of $n$ over all test cases doesn't exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, print $n$ integers, where the $i$-th of them is equal to the minimum cost of the journey if you start and finish in the $i$-th city.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains two integers $n$ and $k$ ($3 \le n \le 2 \cdot 10^5$; $1 \le k \le 10^9$)&nbsp;— the number of cities and the volume of fuel tank, respectively.</p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le k$).</p><p>The third line contains $n$ integers $b_1, b_2, \dots, b_n$ ($1 \le b_i \le 2$).</p><p>The sum of $n$ over all test cases doesn't exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, print $n$ integers, where the $i$-th of them is equal to the minimum cost of the journey if you start and finish in the $i$-th city.</p>





```input1|2,3,4,8,9,10
4
3 5
3 4 4
1 2 2
5 7
1 3 2 5 1
2 1 1 1 2
4 3
1 2 1 3
2 2 2 2
3 2
2 2 2
1 2 1
```




```output1
17 19 17 
13 12 12 12 14 
14 14 14 14 
8 8 8
```


