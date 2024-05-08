## Description

<div><p>LuoTianyi gave an array $b$ of $n \cdot m$ integers. She asks you to construct a table $a$ of size $n \times m$, filled with these $n \cdot m$ numbers, and each element of the array must be used <span class="tex-font-style-bf">exactly once</span>. Also she asked you to maximize the following value:</p><center> <span>$\sum\limits_{i=1}^{n}\sum\limits_{j=1}^{m}\left(\max\limits_{1 \le x \le i, 1 \le y \le j}a_{x,y}-\min\limits_{1 \le x \le i, 1 \le y \le j}a_{x,y}\right)$</span> </center><p>This means that we consider $n \cdot m$ subtables with the upper left corner in $(1,1)$ and the bottom right corner in $(i, j)$ ($1 \le i \le n$, $1 \le j \le m$), for each such subtable calculate the difference of the maximum and minimum elements in it, then sum up all these differences. You should maximize the resulting sum.</p><p>Help her find the maximal possible value, you don't need to reconstruct the table itself.</p></div><div class="input-specification"><p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 200$) — the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains two integers $n$ and $m$ ($2 \le n, m \le 100$) — the number of rows and columns of the table.</p><p>The second line of each test case contains $n \cdot m$ integers $b_1, b_2, \ldots, b_{n\cdot m}$ ($-10^5 \le b_{i} \le 10^5$) — the numbers you can put in the table.</p><p>Note, that integers in the array $b$ <span class="tex-font-style-bf">can be negative</span>.</p><p>It is guaranteed that the sum of $n \cdot m$ over all test cases doesn't exceed $2\cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output a single integer — the maximal value, that can be obtained.</p></div>

## Input

<p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 200$) — the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains two integers $n$ and $m$ ($2 \le n, m \le 100$) — the number of rows and columns of the table.</p><p>The second line of each test case contains $n \cdot m$ integers $b_1, b_2, \ldots, b_{n\cdot m}$ ($-10^5 \le b_{i} \le 10^5$) — the numbers you can put in the table.</p><p>Note, that integers in the array $b$ <span class="tex-font-style-bf">can be negative</span>.</p><p>It is guaranteed that the sum of $n \cdot m$ over all test cases doesn't exceed $2\cdot 10^5$.</p>

## Output

<p>For each test case, output a single integer — the maximal value, that can be obtained.</p>





```input1|2,3,6,7,10,11
5
2 2
1 3 1 4
2 2
-1 -1 -1 -1
2 3
7 8 9 -3 10 8
3 2
4 8 -3 0 -7 1
4 3
-32030 59554 16854 -85927 68060 -64460 -79547 90932 85063 82703 -12001 38762
```




```output1
9
0
64
71
1933711
```



## Note

<p>In the first test case, the table is follows:</p><p></p><table class="tex-tabular"><tbody><tr><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">4</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">1</td></tr><tr><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">1</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">3</td></tr></tbody></table> <p></p><p>In the subtable with the bottom right corner in $(1, 1)$, the difference of the maximal and minimal elements is $4 - 4 = 0$.</p><p>In the subtable with the bottom right corner in $(1, 2)$, the difference of the maximal and minimal elements is $4 - 1 = 3$.</p><p>In the subtable with the bottom right corner in $(2, 1)$, the difference of the maximal and minimal elements is $4 - 1 = 3$.</p><p>In the subtable with the bottom right corner in $(2, 2)$, the difference of the maximal and minimal elements is $4 - 1 = 3$.</p><p>Then the maximum possible value is $0+3+3+3=9$.</p><p>In the second test case, all elements are equal, so all differences are $0$, and the answer is $0$.</p>
