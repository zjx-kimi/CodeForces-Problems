## Description

<div><p>Consider all equalities of form $a + b = c$, where $a$ has $A$ digits, $b$ has $B$ digits, and $c$ has $C$ digits. All the numbers are <span class="tex-font-style-bf">positive</span> integers and are written without leading zeroes. Find the $k$-th lexicographically smallest equality when written as a string like above or determine that it does not exist.</p><p>For example, the first three equalities satisfying $A = 1$, $B = 1$, $C = 2$ are </p><ul> <li> $1 + 9 = 10$, </li><li> $2 + 8 = 10$, </li><li> $2 + 9 = 11$. </li></ul><p>An equality $s$ is lexicographically smaller than an equality $t$ with the same lengths of the numbers if and only if the following holds: </p><ul> <li> in the first position where $s$ and $t$ differ, the equality $s$ has a smaller digit than the corresponding digit in $t$. </li></ul></div><div class="input-specification"><p>Each test contains multiple test cases. The first line of input contains a single integer $t$ ($1 \leq t \leq 10^3$) — the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains integers $A$, $B$, $C$, $k$ ($1 \leq A, B, C \leq 6$, $1 \leq k \leq 10^{12}$).</p><p>Each input file has at most $5$ test cases which <span class="tex-font-style-bf">do not</span> satisfy $A, B, C \leq 3$.</p></div><div class="output-specification"><p>For each test case, if there are strictly less than $k$ valid equalities, output $-1$.</p><p>Otherwise, output the $k$-th equality as a string of form $a + b = c$.</p></div>

## Input

<p>Each test contains multiple test cases. The first line of input contains a single integer $t$ ($1 \leq t \leq 10^3$) — the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains integers $A$, $B$, $C$, $k$ ($1 \leq A, B, C \leq 6$, $1 \leq k \leq 10^{12}$).</p><p>Each input file has at most $5$ test cases which <span class="tex-font-style-bf">do not</span> satisfy $A, B, C \leq 3$.</p>

## Output

<p>For each test case, if there are strictly less than $k$ valid equalities, output $-1$.</p><p>Otherwise, output the $k$-th equality as a string of form $a + b = c$.</p>





```input1|2,4,6,8
7
1 1 1 9
2 2 3 1
2 2 1 1
1 5 6 42
1 6 6 10000000
5 5 6 3031568815
6 6 6 1000000000000
```




```output1
2 + 1 = 3
10 + 90 = 100
-1
9 + 99996 = 100005
-1
78506 + 28543 = 107049
-1
```



## Note

<p>In the first test case, the first $9$ solutions are: $\langle 1, 1, 2 \rangle, \langle 1, 2, 3 \rangle, \langle 1, 3, 4 \rangle, \langle 1, 4, 5 \rangle, \langle 1, 5, 6 \rangle, \langle 1, 6, 7 \rangle, \langle 1, 7, 8 \rangle, \langle 1, 8, 9 \rangle, \langle 2, 1, 3 \rangle$.</p><p>Int the third test case, there are no solutions as the smallest possible values for $a$ and $b$ are larger than the maximal possible value of $c$ — $10 + 10 = 20 &gt; 9$.</p><p>Please note that whitespaces in the output <span class="tex-font-style-bf">matter</span>.</p>
