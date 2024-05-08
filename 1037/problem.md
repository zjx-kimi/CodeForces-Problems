## Description

<div><p>Tannhaus, the clockmaker in the town of Winden, makes mysterious clocks that measure time in $h$ hours numbered from $0$ to $h-1$. One day, he decided to make a puzzle with these clocks. </p><p>The puzzle consists of an $n \times m$ grid of clocks, and each clock always displays some hour exactly (that is, it doesn't lie between two hours). In one move, he can choose any row or column and shift all clocks in that row or column one hour forward$^\dagger$.</p><p>The grid of clocks is called <span class="tex-font-style-it">solvable</span> if it is possible to make all the clocks display the same time.</p><p>While building his puzzle, Tannhaus suddenly got worried that it might not be possible to make the grid solvable. Some cells of the grid have clocks already displaying a certain initial time, while the rest of the cells are empty.</p><p>Given the partially completed grid of clocks, find the number of ways$^\ddagger$ to assign clocks in the empty cells so that the grid is solvable. The answer can be enormous, so compute it modulo $10^9 + 7$.</p><p>$^\dagger$ If a clock currently displays hour $t$ and is shifted one hour forward, then the clock will instead display hour $(t+1) \bmod h$.</p><p>$^\ddagger$ Two assignments are different if there exists some cell with a clock that displays a different time in both arrangements.</p></div><div class="input-specification"><p>The first line of input contains $t$ ($1 \leq t \leq 5 \cdot 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case consists of 3 integers $n$, $m$, and $h$ ($1 \leq n, m \leq 2 \cdot 10^5$; $1 \leq h \leq 10^9$) — the number of rows in the grid, the number of columns in the grid, and the number of the hours in the day respectively.</p><p>The next $n$ lines each contain $m$ integers, describing the clock grid. The integer $x$ ($-1 \leq x &lt; h$) in the $i$-th row and the $j$-th column represents the initial hour of the corresponding clock, or if $x = -1$, an empty cell.</p><p>It is guaranteed that the sum of $n \cdot m$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output the number of ways to assign clocks in the empty cells so that the grid is solvable. The answer can be huge, so output it modulo $10^9 + 7$.</p></div>

## Input

<p>The first line of input contains $t$ ($1 \leq t \leq 5 \cdot 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case consists of 3 integers $n$, $m$, and $h$ ($1 \leq n, m \leq 2 \cdot 10^5$; $1 \leq h \leq 10^9$) — the number of rows in the grid, the number of columns in the grid, and the number of the hours in the day respectively.</p><p>The next $n$ lines each contain $m$ integers, describing the clock grid. The integer $x$ ($-1 \leq x &lt; h$) in the $i$-th row and the $j$-th column represents the initial hour of the corresponding clock, or if $x = -1$, an empty cell.</p><p>It is guaranteed that the sum of $n \cdot m$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output the number of ways to assign clocks in the empty cells so that the grid is solvable. The answer can be huge, so output it modulo $10^9 + 7$.</p>





```input1|2,3,4,8,9,10,11,12,17,18,19,20
5
2 3 4
1 0 -1
-1 -1 2
2 2 10
1 2
3 5
4 5 1024
1 -1 -1 -1 -1
-1 -1 -1 1000 -1
-1 -1 -1 -1 69
420 -1 -1 999 -1
3 3 3
-1 -1 1
2 -1 1
2 -1 2
3 3 3
1 -1 2
-1 0 -1
-1 1 0
```




```output1
4
0
73741817
0
1
```



## Note

<p>For the first sample, this is a possible configuration for the clocks: </p><table class="tex-tabular"><tbody><tr><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">1</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">0</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">3</td></tr><tr><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">0</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">3</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">2</td></tr></tbody></table><p></p><p>This is solvable since we can: </p><ol> <li> Move the middle column forward one hour. </li><li> Move the third column forward one hour. </li><li> Move the third column forward one hour. </li><li> Move the second row forward one hour. </li></ol> After that all the clocks show one hour.<p>For the second test case, it can be shown that there are no possible solvable clock configurations. </p>
