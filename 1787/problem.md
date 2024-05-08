## Description

<div><p>The integers shop sells $n$ segments. The $i$-th of them contains all integers from $l_i$ to $r_i$ and costs $c_i$ coins.</p><p>Tomorrow Vasya will go to this shop and will buy some segments there. He will get all integers that appear in at least one of bought segments. The total cost of the purchase is the sum of costs of all segments in it.</p><p>After shopping, Vasya will get some more integers as a gift. He will get integer $x$ as a gift if and only if all of the following conditions are satisfied: </p><ul> <li> Vasya hasn't bought $x$. </li><li> Vasya has bought integer $l$ that is less than $x$. </li><li> Vasya has bought integer $r$ that is greater than $x$. </li></ul><p>Vasya can get integer $x$ as a gift only once so he won't have the same integers after receiving a gift.</p><p>For example, if Vasya buys segment $[2, 4]$ for $20$ coins and segment $[7, 8]$ for $22$ coins, he spends $42$ coins and receives integers $2, 3, 4, 7, 8$ from these segments. He also gets integers $5$ and $6$ as a gift.</p><p>Due to the technical issues only the first $s$ segments (that is, segments $[l_1, r_1], [l_2, r_2], \ldots, [l_s, r_s]$) will be available tomorrow in the shop.</p><p>Vasya wants to get (to buy or to get as a gift) as many integers as possible. If he can do this in differents ways, he selects the cheapest of them.</p><p>For each $s$ from $1$ to $n$, find how many coins will Vasya spend if only the first $s$ segments will be available.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \leq t \leq 1000$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains the single integer $n$ ($1 \leq n \leq 10^5$)&nbsp;— the number of segments in the shop.</p><p>Each of next $n$ lines contains three integers $l_i$, $r_i$, $c_i$ ($1 \leq l_i \leq r_i \leq 10^9, 1 \leq c_i \leq 10^9$)&nbsp;— the ends of the $i$-th segments and its cost.</p><p>It is guaranteed that the total sum of $n$ over all test cases doesn't exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case output $n$ integers: the $s$-th ($1 \leq s \leq n$) of them should be the number of coins Vasia will spend in the shop if only the first $s$ segments will be available.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \leq t \leq 1000$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains the single integer $n$ ($1 \leq n \leq 10^5$)&nbsp;— the number of segments in the shop.</p><p>Each of next $n$ lines contains three integers $l_i$, $r_i$, $c_i$ ($1 \leq l_i \leq r_i \leq 10^9, 1 \leq c_i \leq 10^9$)&nbsp;— the ends of the $i$-th segments and its cost.</p><p>It is guaranteed that the total sum of $n$ over all test cases doesn't exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case output $n$ integers: the $s$-th ($1 \leq s \leq n$) of them should be the number of coins Vasia will spend in the shop if only the first $s$ segments will be available.</p>





```input1|2,3,4,8,9,10,11,12,13,14
3
2
2 4 20
7 8 22
2
5 11 42
5 11 42
6
1 4 4
5 8 9
7 8 7
2 10 252
1 11 271
1 10 1
```




```output1
20
42
42
42
4
13
11
256
271
271
```



## Note

<p>In the first test case if $s = 1$ then Vasya can buy only the segment $[2, 4]$ for $20$ coins and get $3$ integers.</p><p>The way to get $7$ integers for $42$ coins in case $s = 2$ is described in the statement.</p><p>In the second test case note, that there can be the same segments in the shop.</p>
