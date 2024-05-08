## Description

<div><p>Game studio "DbZ Games" wants to introduce another map in their popular game "Valiant". This time, the map named "Panvel" will be based on the city of Mumbai.</p><p>Mumbai can be represented as $n \times m$ cellular grid. Each cell $(i, j)$ ($1 \le i \le n$; $1 \le j \le m$) of the grid is occupied by a cuboid building of height $a_{i,j}$.</p><p>This time, DbZ Games want to make a map that has perfect vertical gameplay. That's why they want to choose an $l \times l$ square inside Mumbai, such that each building inside the square has a height of at least $l$.</p><p>Can you help DbZ Games find such a square of the maximum possible size $l$?</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \leq t \leq 1000$). Description of the test cases follows.</p><p>The first line of each test case contains two positive integers $n$ and $m$ ($1 \le n \le m$; $1 \leq n \cdot m \leq 10^6$).</p><p>The $i$-th of next $n$ lines contains $m$ integers $a_{i,1}, a_{i,2}, \dots, a_{i,m}$ ($1 \leq a_{i,j} \leq 10^6$)&nbsp;— heights of buildings on the $i$-th row.</p><p>It's guaranteed that the sum of $n \cdot m$ over all test cases doesn't exceed $10^6$.</p></div><div class="output-specification"><p>For each test case, print the maximum side length $l$ of the square DbZ Games can choose.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \leq t \leq 1000$). Description of the test cases follows.</p><p>The first line of each test case contains two positive integers $n$ and $m$ ($1 \le n \le m$; $1 \leq n \cdot m \leq 10^6$).</p><p>The $i$-th of next $n$ lines contains $m$ integers $a_{i,1}, a_{i,2}, \dots, a_{i,m}$ ($1 \leq a_{i,j} \leq 10^6$)&nbsp;— heights of buildings on the $i$-th row.</p><p>It's guaranteed that the sum of $n \cdot m$ over all test cases doesn't exceed $10^6$.</p>

## Output

<p>For each test case, print the maximum side length $l$ of the square DbZ Games can choose.</p>





```input1|2,3,4,7,8,9
4
2 2
2 3
4 5
1 3
1 2 3
2 3
4 4 3
2 1 4
5 6
1 9 4 6 5 8
10 9 5 8 11 6
24 42 32 8 11 1
23 1 9 69 13 3
13 22 60 12 14 17
```




```output1
2
1
1
3
```



## Note

<p>In the first test case, we can choose the square of side $l = 2$ (i.&nbsp;e. the whole grid) since the heights of all buildings are greater than or equal to $2$.</p><p>In the second test case, we can only choose the side as $1$, so the answer is $1$.</p><p>In the third test case, there are no squares of size $2$ that have all buildings of height at least $2$, so the answer is $1$. </p>
