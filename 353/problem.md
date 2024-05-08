## Description

<div><p>You have an array $a$ of size $n$, initially filled with zeros ($a_1 = a_2 = \ldots = a_n = 0$). You also have an array of integers $c$ of size $n$.</p><p>Initially, you have $k$ coins. By paying $c_i$ coins, you can add $1$ to all elements of the array $a$ from the first to the $i$-th element ($a_j \mathrel{+}= 1$ for all $1 \leq j \leq i$). You can buy any $c_i$ any number of times. A purchase is only possible if $k \geq c_i$, meaning that at any moment $k \geq 0$ must hold true.</p><p>Find the lexicographically largest array $a$ that can be obtained.</p><p>An array $a$ is lexicographically smaller than an array $b$ of the same length if and only if in the first position where $a$ and $b$ differ, the element in array $a$ is smaller than the corresponding element in $b$.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \leq t \leq 10^4$) — the number of test cases. This is followed by a description of the test cases.</p><p>The first line of each test case contains a single integer $n$ ($1 \leq n \leq 2 \cdot 10^5$) — the size of arrays $a$ and $c$.</p><p>The second line of each test case contains $n$ integers $c_1, c_2, \ldots, c_n$ ($1 \leq c_i \leq 10^9$) — the array $c$.</p><p>The third line of each test case contains a single integer $k$ ($1 \leq k \leq 10^9$) — the number of coins you have.</p><p>It is guaranteed that the sum of all $n$ values across all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output $n$ integers $a_1, a_2, \ldots, a_n$ — the lexicographically largest array $a$ that can be obtained.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \leq t \leq 10^4$) — the number of test cases. This is followed by a description of the test cases.</p><p>The first line of each test case contains a single integer $n$ ($1 \leq n \leq 2 \cdot 10^5$) — the size of arrays $a$ and $c$.</p><p>The second line of each test case contains $n$ integers $c_1, c_2, \ldots, c_n$ ($1 \leq c_i \leq 10^9$) — the array $c$.</p><p>The third line of each test case contains a single integer $k$ ($1 \leq k \leq 10^9$) — the number of coins you have.</p><p>It is guaranteed that the sum of all $n$ values across all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output $n$ integers $a_1, a_2, \ldots, a_n$ — the lexicographically largest array $a$ that can be obtained.</p>





```input1|2,3,4,8,9,10
4
3
1 2 3
5
2
3 4
7
3
3 2 1
2
6
10 6 4 6 3 4
7
```




```output1
5 0 0 
2 1 
2 2 2 
2 2 2 2 2 1
```



## Note

<p>In the first test case, $a_1$ cannot be greater than $5$, and if we buy $c_1$ five times, we will run out of money, so $a = [5, 0, 0]$.</p><p>In the second test case, $a_1$ cannot be greater than $2$, but we can buy $c_1$ and $c_2$ once each (buying $c_2$ twice is not possible), so $a = [2, 1]$.</p>
