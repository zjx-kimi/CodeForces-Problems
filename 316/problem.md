## Description

<div><p>There are $n$ teams in a football tournament. Each pair of teams match up once. After every match, Pak Chanek receives two integers as the result of the match, the number of goals the two teams score during the match. The efficiency of a team is equal to the total number of goals the team scores in each of its matches minus the total number of goals scored by the opponent in each of its matches.</p><p>After the tournament ends, Pak Dengklek counts the efficiency of every team. Turns out that he forgot about the efficiency of one of the teams. Given the efficiency of $n-1$ teams $a_1,a_2,a_3,\ldots,a_{n-1}$. What is the efficiency of the missing team? It can be shown that the efficiency of the missing team can be uniquely determined.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains an integer $t$ ($1 \leq t \leq 500$) — the number of test cases. The following lines contain the description of each test case.</p><p>The first line contains a single integer $n$ ($2 \leq n \leq 100$) — the number of teams.</p><p>The second line contains $n-1$ integers $a_1,a_2,a_3,\ldots,a_{n-1}$ ($-100\leq a_i\leq100$) — the efficiency of $n-1$ teams.</p></div><div class="output-specification"><p>For each test case, output a line containing an integer representing the efficiency of the missing team.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains an integer $t$ ($1 \leq t \leq 500$) — the number of test cases. The following lines contain the description of each test case.</p><p>The first line contains a single integer $n$ ($2 \leq n \leq 100$) — the number of teams.</p><p>The second line contains $n-1$ integers $a_1,a_2,a_3,\ldots,a_{n-1}$ ($-100\leq a_i\leq100$) — the efficiency of $n-1$ teams.</p>

## Output

<p>For each test case, output a line containing an integer representing the efficiency of the missing team.</p>





```input1|2,3
2
4
3 -4 5
11
-30 12 -57 7 0 -81 -68 41 -89 0
```




```output1
-4
265
```



## Note

<p>In the first test case, below is a possible tournament result: </p><ul> <li> Team $1$ vs. Team $2$: $1-2$ </li><li> Team $1$ vs. Team $3$: $3-0$ </li><li> Team $1$ vs. Team $4$: $3-2$ </li><li> Team $2$ vs. Team $3$: $1-4$ </li><li> Team $2$ vs. Team $4$: $1-3$ </li><li> Team $3$ vs. Team $4$: $5-0$ </li></ul><p>The efficiency of each team is: </p><ol> <li> Team $1$: $(1+3+3)-(2+0+2)=7-4=3$ </li><li> Team $2$: $(2+1+1)-(1+4+3)=4-8=-4$ </li><li> Team $3$: $(0+4+5)-(3+1+0)=9-4=5$ </li><li> Team $4$: $(2+3+0)-(3+1+5)=5-9=-4$ </li></ol><p>Therefore, the efficiency of the missing team (team $4$) is $-4$.</p><p>It can be shown that any possible tournament of $4$ teams that has the efficiency of $3$ teams be $3$, $-4$, and $5$ will always have the efficiency of the $4$-th team be $-4$.</p>
