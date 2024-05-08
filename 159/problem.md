## Description

<div><p>Gridlandia has been hit by flooding and now has to reconstruct all of it's cities. Gridlandia can be described by an $n \times m$ matrix.</p><p>Initially, all of its cities are in economic collapse. The government can choose to rebuild certain cities. Additionally, any collapsed city which has at least one vertically neighboring rebuilt city and at least one horizontally neighboring rebuilt city can ask for aid from them and become rebuilt <span class="tex-font-style-bf">without help from the government</span>. More formally, collapsed city positioned in $(i, j)$ can become rebuilt if <span class="tex-font-style-bf">both</span> of the following conditions are satisfied:</p><ul> <li> At least one of cities with positions $(i + 1, j)$ and $(i - 1, j)$ is rebuilt; </li><li> At least one of cities with positions $(i, j + 1)$ and $(i, j - 1)$ is rebuilt. </li></ul><p>If the city is located on the border of the matrix and has only one horizontally or vertically neighbouring city, then we consider only that city.</p><center> <table class="tex-tabular"><tbody><tr><td class="tex-tabular-text-align-center"><img class="tex-graphics" src="file://cmAywLJX.png" style="max-width: 100.0%;max-height: 100.0%;"></td></tr></tbody></table> <span class="tex-font-size-small"> Illustration of two possible ways cities can be rebuilt by adjacent aid. White cells are collapsed cities, yellow cells are initially rebuilt cities (either by the government or adjacent aid), and orange cells are rebuilt cities after adjacent aid.</span> </center><p>The government wants to know the minimum number of cities it has to rebuild such that <span class="tex-font-style-bf">after some time</span> all the cities can be rebuild.</p></div><div class="input-specification"><p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 10^4$) — the number of test cases. The description of the test cases follows.</p><p>The only line of each test case contains two integers $n$ and $m$ ($2 \le n, m \le 100$) — the sizes of Gridlandia.</p></div><div class="output-specification"><p>For each test case, output a single integer — the minimum number of cities the government needs to rebuild.</p></div>

## Input

<p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 10^4$) — the number of test cases. The description of the test cases follows.</p><p>The only line of each test case contains two integers $n$ and $m$ ($2 \le n, m \le 100$) — the sizes of Gridlandia.</p>

## Output

<p>For each test case, output a single integer — the minimum number of cities the government needs to rebuild.</p>





```input1|2,4
3
2 2
5 7
3 2
```




```output1
2
7
3
```



## Note

<p>In the first test case, it's enough for the government to rebuild cities $(1, 2)$ and $(2, 1)$.</p><p>In the second test case, it's enough for the government to rebuild cities $(1, 4)$, $(2, 2)$, $(3, 1)$, $(3, 6)$, $(4, 3)$, $(5, 5)$, $(5, 7)$.</p>
