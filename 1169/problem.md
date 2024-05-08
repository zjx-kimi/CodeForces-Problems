## Description

<div><p>Demodogs from the Upside-down have attacked Hawkins again. El wants to reach Mike and also kill as many Demodogs in the way as possible.</p><p>Hawkins can be represented as an $n \times n$ grid. The number of Demodogs in a cell at the $i$-th row and the $j$-th column is $i \cdot j$. El is at position $(1, 1)$ of the grid, and she has to reach $(n, n)$ where she can find Mike. </p><p>The only directions she can move are the right (from $(i, j)$ to $(i, j + 1)$) and the down (from $(i, j)$ to $(i + 1, j)$). She can't go out of the grid, as there are doors to the Upside-down at the boundaries. </p><p>Calculate the maximum possible number of Demodogs $\mathrm{ans}$ she can kill on the way, considering that she kills all Demodogs in cells she visits (including starting and finishing cells).</p><p>Print $2022 \cdot \mathrm{ans}$ modulo $10^9 + 7$. Modulo $10^9 + 7$ because the result can be too large and multiplied by $2022$ because we are never gonna see it again!</p><p>(Note, you firstly multiply by $2022$ and <span class="tex-font-style-bf">only after</span> that take the remainder.)</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \leq t \leq 10^4$). Description of the test cases follows.</p><p>The first line of each test case contains one integer $n$ ($2 \leq n \leq 10^9$)&nbsp;— the size of the grid.</p></div><div class="output-specification"><p>For each test case, print a single integer&nbsp;— the maximum number of Demodogs that can be killed multiplied by $2022$, modulo $10^9 + 7$.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \leq t \leq 10^4$). Description of the test cases follows.</p><p>The first line of each test case contains one integer $n$ ($2 \leq n \leq 10^9$)&nbsp;— the size of the grid.</p>

## Output

<p>For each test case, print a single integer&nbsp;— the maximum number of Demodogs that can be killed multiplied by $2022$, modulo $10^9 + 7$.</p>





```input1|2,4
4
2
3
50
1000000000
```




```output1
14154
44484
171010650
999589541
```



## Note

<p>In the first test case, for any path chosen by her the number of Demodogs to be killed would be $7$, so the answer would be $2022 \cdot 7 = 14154$.</p>
