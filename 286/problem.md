## Description

<div><p>You are given an array of integers $a_1, a_2, \ldots, a_n$ and a number $k$ ($2 \leq k \leq 5$). In one operation, you can do the following:</p><ul><li> Choose an index $1 \leq i \leq n$,</li><li> Set $a_i = a_i + 1$.</li></ul><p>Find the minimum number of operations needed to make the product of all the numbers in the array $a_1 \cdot a_2 \cdot \ldots \cdot a_n$ divisible by $k$.</p></div><div class="input-specification"><p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 10^4$) — the number of test cases. Then follows the description of the test cases.</p><p>The first line of each test case contains two integers $n$ and $k$ ($2 \leq n \leq 10^5$, $2 \leq k \leq 5$) — the size of the array $a$ and the number $k$.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \leq a_i \leq 10$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output the minimum number of operations needed to make the product of all the numbers in the array divisible by $k$.</p></div>

## Input

<p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 10^4$) — the number of test cases. Then follows the description of the test cases.</p><p>The first line of each test case contains two integers $n$ and $k$ ($2 \leq n \leq 10^5$, $2 \leq k \leq 5$) — the size of the array $a$ and the number $k$.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \leq a_i \leq 10$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output the minimum number of operations needed to make the product of all the numbers in the array divisible by $k$.</p>





```input1|2,3,6,7,10,11,14,15,18,19,22,23,26,27,30,31
15
2 5
7 3
3 3
7 4 1
5 2
9 7 7 3 9
5 5
5 4 1 2 3
7 4
9 5 1 5 9 5 1
3 4
6 3 6
3 4
6 1 5
3 4
1 5 9
4 4
1 4 1 1
3 4
3 5 3
4 5
8 9 9 3
2 5
1 6
2 5
10 10
4 5
1 6 1 1
2 5
7 7
```




```output1
2
2
1
0
2
0
1
2
0
1
1
4
0
4
3
```



## Note

<p>In the first test case, we need to choose the index $i = 2$ twice. After that, the array will be $a = [7, 5]$. The product of all the numbers in the array is $35$.</p><p>In the fourth test case, the product of the numbers in the array is $120$, which is already divisible by $5$, so no operations are needed.</p><p>In the eighth test case, we can perform two operations by choosing $i = 2$ and $i = 3$ in any order. After that, the array will be $a = [1, 6, 10]$. The product of the numbers in the array is $60$.</p>
