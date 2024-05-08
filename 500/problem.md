## Description

<div><p>An $n \times m$ grid of characters is called <span class="tex-font-style-it">great</span> if it satisfies these three conditions: </p><ul> <li> Each character is either '<span class="tex-font-style-tt">A</span>', '<span class="tex-font-style-tt">B</span>', or '<span class="tex-font-style-tt">C</span>'. </li><li> Every $2 \times 2$ contiguous subgrid contains all three different letters. </li><li> Any two cells that share a common edge contain different letters. </li></ul><p>Let $(x,y)$ denote the cell in the $x$-th row from the top and $y$-th column from the left.</p><p>You want to construct a great grid that satisfies $k$ constraints. Each constraint consists of two cells, $(x_{i,1},y_{i,1})$ and $(x_{i,2},y_{i,2})$, that share exactly one corner. You want your great grid to have the same letter in cells $(x_{i,1},y_{i,1})$ and $(x_{i,2},y_{i,2})$.</p><p>Determine whether there exists a great grid satisfying all the constraints. </p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^3$). The description of the test cases follows.</p><p>The first line of each test case contains three integers, $n$, $m$, and $k$ ($2 \le n,m \le 2 \cdot 10^3$, $1 \le k \le 4 \cdot 10^3$).</p><p>Each of the next $k$ lines contains four integers, $x_{i,1}$, $y_{i,1}$, $x_{i,2}$, and $y_{i,2}$ ($1 \le x_{i,1} &lt; x_{i,2} \le n$, $1 \le y_{i,1},y_{i,2} \le m$). It is guaranteed that either $(x_{i,2},y_{i,2}) = (x_{i,1}+1,y_{i,1}+1)$ or $(x_{i,2},y_{i,2}) = (x_{i,1}+1,y_{i,1}-1)$.</p><p>The pairs of cells are pairwise distinct, i.e. for all $1 \le i &lt; j \le k$, it is <span class="tex-font-style-bf">not</span> true that $x_{i,1} = x_{j,1}$, $y_{i,1} = y_{j,1}$, $x_{i,2} = x_{j,2}$, and $y_{i,2} = y_{j,2}$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^3$.</p><p>It is guaranteed that the sum of $m$ over all test cases does not exceed $2 \cdot 10^3$.</p><p>It is guaranteed that the sum of $k$ over all test cases does not exceed $4 \cdot 10^3$.</p></div><div class="output-specification"><p>For each test case, output "<span class="tex-font-style-tt">YES</span>" if a great grid satisfying all the constraints exists and "<span class="tex-font-style-tt">NO</span>" otherwise.</p><p>You can output the answer in any case (upper or lower). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as positive responses.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^3$). The description of the test cases follows.</p><p>The first line of each test case contains three integers, $n$, $m$, and $k$ ($2 \le n,m \le 2 \cdot 10^3$, $1 \le k \le 4 \cdot 10^3$).</p><p>Each of the next $k$ lines contains four integers, $x_{i,1}$, $y_{i,1}$, $x_{i,2}$, and $y_{i,2}$ ($1 \le x_{i,1} &lt; x_{i,2} \le n$, $1 \le y_{i,1},y_{i,2} \le m$). It is guaranteed that either $(x_{i,2},y_{i,2}) = (x_{i,1}+1,y_{i,1}+1)$ or $(x_{i,2},y_{i,2}) = (x_{i,1}+1,y_{i,1}-1)$.</p><p>The pairs of cells are pairwise distinct, i.e. for all $1 \le i &lt; j \le k$, it is <span class="tex-font-style-bf">not</span> true that $x_{i,1} = x_{j,1}$, $y_{i,1} = y_{j,1}$, $x_{i,2} = x_{j,2}$, and $y_{i,2} = y_{j,2}$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^3$.</p><p>It is guaranteed that the sum of $m$ over all test cases does not exceed $2 \cdot 10^3$.</p><p>It is guaranteed that the sum of $k$ over all test cases does not exceed $4 \cdot 10^3$.</p>

## Output

<p>For each test case, output "<span class="tex-font-style-tt">YES</span>" if a great grid satisfying all the constraints exists and "<span class="tex-font-style-tt">NO</span>" otherwise.</p><p>You can output the answer in any case (upper or lower). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as positive responses.</p>





```input1|2,3,4,5,6,10,11,12,13,14
4
3 4 4
1 1 2 2
2 1 3 2
1 4 2 3
2 3 3 2
2 7 2
1 1 2 2
1 2 2 1
8 5 4
1 2 2 1
1 5 2 4
7 1 8 2
7 4 8 5
8 5 4
1 2 2 1
1 5 2 4
7 1 8 2
7 5 8 4
```




```output1
YES
NO
YES
NO
```



## Note

<p>In the first test case, the following great grid satisfies all the constraints: </p><table class="tex-tabular"><tbody><tr><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom"><span class="tex-font-style-tt">B</span></td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom"><span class="tex-font-style-tt">A</span></td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom"><span class="tex-font-style-tt">B</span></td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom"><span class="tex-font-style-tt">C</span></td></tr><tr><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom"><span class="tex-font-style-tt">C</span></td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom"><span class="tex-font-style-tt">B</span></td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom"><span class="tex-font-style-tt">C</span></td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom"><span class="tex-font-style-tt">A</span></td></tr><tr><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom"><span class="tex-font-style-tt">A</span></td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom"><span class="tex-font-style-tt">C</span></td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom"><span class="tex-font-style-tt">A</span></td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom"><span class="tex-font-style-tt">B</span></td></tr></tbody></table><p></p><p>In the second test case, the two constraints imply that cells $(1,1)$ and $(2,2)$ have the same letter and cells $(1,2)$ and $(2,1)$ have the same letter, which makes it impossible for the only $2 \times 2$ subgrid to contain all three different letters.</p>
