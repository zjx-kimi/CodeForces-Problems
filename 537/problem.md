## Description

<div><p>You have $n$ lamps, numbered by integers from $1$ to $n$. Each lamp $i$ has two integer parameters $a_i$ and $b_i$.</p><p>At each moment each lamp is <span class="tex-font-style-bf">in one of three states</span>: it may be turned on, turned off, or broken.</p><p>Initially all lamps are turned off. In one operation you can select one lamp that is turned off and turn it on (you can't turn on broken lamps). You <span class="tex-font-style-bf">receive</span> $b_i$ points for turning lamp $i$ on. The following happens after each performed operation: </p><ul> <li> Let's denote the number of lamps that are turned on as $x$ (broken lamps <span class="tex-font-style-bf">do not count</span>). All lamps $i$ such that $a_i \le x$ simultaneously break, whether they were turned on or off. </li></ul><p>Please note that broken lamps never count as turned on and that after a turned on lamp breaks, you still keep points received for turning it on.</p><p>You can perform an arbitrary number of operations.</p><p>Find the maximum number of points you can get.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The first line contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$)&nbsp;— the number of lamps.</p><p>Each of the next $n$ lines contains two integers $a_i$ and $b_i$ ($1 \le a_i \le n, 1 \le b_i \le 10^9$)&nbsp;— parameters of the $i$-th lamp.</p><p>It is guaranteed that sum of $n$ over all test cases doesn't exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output one integer&nbsp;— the maximum number of points you can get.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The first line contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$)&nbsp;— the number of lamps.</p><p>Each of the next $n$ lines contains two integers $a_i$ and $b_i$ ($1 \le a_i \le n, 1 \le b_i \le 10^9$)&nbsp;— parameters of the $i$-th lamp.</p><p>It is guaranteed that sum of $n$ over all test cases doesn't exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output one integer&nbsp;— the maximum number of points you can get.</p>





```input1|2,3,4,5,6,13,14,15,16,17,18,19
4
4
2 2
1 6
1 10
1 13
5
3 4
3 1
2 5
3 2
3 3
6
1 2
3 4
1 4
3 4
3 5
2 3
1
1 1
```




```output1
15
14
20
1
```



## Note

<p>In first test case $n = 4$. One of ways to get the maximum number of points is as follows: </p><ul> <li> You turn lamp $4$ on and receive $b_4 = 13$ points. </li><li> The number of lamps that are turned on is $1$, so all lamps with $a_i \le 1$ (namely lamps $2$, $3$ and $4$) break. Lamp $4$ is no longer turned on, so the number of lamps that are turned becomes $0$. </li><li> The only lamp you can turn on is lamp $1$, as all other lamps are broken. You receive $b_1 = 2$ points for turning it on. </li><li> The number of lamps that are turned on is $1$. As $a_1 = 2$, lamp $1$ doesn't break. </li></ul><p>Your receive $13 + 2 = 15$ points in total. It can be shown that this is the maximum number of points you can get, so the answer for the first test case is $15$.</p><p>In the second test case, one of the ways to get the maximum number of points is as follows:</p><ul> <li> On the first operation you turn on lamp $4$ and receive $2$ points. No lamps break after the first operation. </li><li> On the second operation you turn on lamp $3$ and receive $5$ points. After the second operation, there are $2$ lamps turned on. As $a_3 \le 2$, lamp $3$ breaks. </li><li> On the third operation, you turn on lamp $1$ and receive $4$ points. </li><li> On the fourth operation, you turn on lamp $5$ and receive $3$ points. After that there are $3$ lamps turned on: lamps $1$, $4$ and $5$. Lamps $1$, $2$, $4$ and $5$ simultaneously break, because for all of them $a_i \le 3$. </li></ul><p>You receive $2 + 5 + 4 + 3 = 14$ points in total. It can be shown that this is the maximum number of points you can get.</p><p>In the third test case, one of the ways to get the maximum number of points is as follows:</p><ul> <li> Turn the lamp $3$ on and receive $4$ points. Lamps $1$ and $3$ break. </li><li> Turn the lamp $2$ on and receive $4$ points. </li><li> Turn the lamp $6$ on and receive $3$ points. Lamp $6$ breaks. </li><li> Turn the lamp $4$ on and receive $4$ points. </li><li> Turn the lamp $5$ on and receive $5$ points. Lamps $2$, $4$ and $5$ break. </li></ul><p>You receive $4 + 4 + 3 + 4 + 5 = 20$ points in total. It can be shown that this is the maximum number of points you can get.</p>
