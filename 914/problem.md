## Description

<div><p>As soon as SWERC starts, your experienced $3$-person team immediately realizes that the contest features $a$ easy problems, $b$ medium problems, and $c$ hard problems. Solving a problem will take any of you $2$, $3$, or $4$ time units, depending on whether the problem is easy, medium, or hard. Regardless of the difficulty of the problem, the last time unit spent to solve it has to be spent using your shared computer.</p><p>You organize your efforts so that each of you starts (and ends) solving problems at integer time units. Any given problem can be solved by only one contestant; it requires a contiguous amount of time (which depends on the difficulty of the problem). None of the $3$ of you can solve more than one problem at a time, but you can start solving a new problem immediately after finishing one. Similarly, the shared computer cannot be used by more than one of you at a time, but any of you can start using the computer (to complete the problem currently being solved) immediately after someone else stops using it.</p><p>Given that the contest lasts $l$ time units, find the maximum number of problems that your team can solve. Additionally, find one way to solve the maximum number of problems.</p></div><div class="input-specification"><p>The input has a single line. It contains four integers $a$, $b$, $c$, $l$ ($0 \leq a, b, c, \leq 10^4$, $0 \le l \le 10^5$) — the number of easy, medium, and hard problems, and the duration of the contest.</p></div><div class="output-specification"><p>On the first line, print a single integer $n$ — the maximum number of problems that your team can solve.</p><p>Then, on the $j$-th of the following $n$ lines, print three integers $x_j$, $p_j$, $q_j$ ($1 \leq x \leq 3$, $0 \leq p_j &lt; q_j \leq l$) — the contestant that solves the $j$-th problem, and the start and end time for solving the $j$-th problem (measured as time units elapsed from the beginning of the contest). The difference $q_j - p_j$ is $2$, $3$, or $4$, depending on the difficulty of the problem.</p><p>The last $n$ lines are to be provided in increasing order of end time: $q_1 &lt; q_2 &lt; \cdots &lt; q_n$. If there are multiple ways to solve $n$ problems, output any of them.</p></div>

## Input

<p>The input has a single line. It contains four integers $a$, $b$, $c$, $l$ ($0 \leq a, b, c, \leq 10^4$, $0 \le l \le 10^5$) — the number of easy, medium, and hard problems, and the duration of the contest.</p>

## Output

<p>On the first line, print a single integer $n$ — the maximum number of problems that your team can solve.</p><p>Then, on the $j$-th of the following $n$ lines, print three integers $x_j$, $p_j$, $q_j$ ($1 \leq x \leq 3$, $0 \leq p_j &lt; q_j \leq l$) — the contestant that solves the $j$-th problem, and the start and end time for solving the $j$-th problem (measured as time units elapsed from the beginning of the contest). The difference $q_j - p_j$ is $2$, $3$, or $4$, depending on the difficulty of the problem.</p><p>The last $n$ lines are to be provided in increasing order of end time: $q_1 &lt; q_2 &lt; \cdots &lt; q_n$. If there are multiple ways to solve $n$ problems, output any of them.</p>





```input1
2 1 1 3
```




```input2
1 2 3 5
```




```input3
0 1 2 2
```




```output1
2
1 0 2
2 0 3
```




```output2
4
1 0 2
2 0 3
3 0 4
1 2 5
```




```output3
0
```



## Note

<p>In the <span class="tex-font-style-bf">first sample</span>, the first contestant solves an easy problem between time $0$ and time $2$ while the second contestant solves a medium problem between time $0$ and time $3$.</p><p>In the <span class="tex-font-style-bf">second sample</span>, the first contestant solves an easy problem between time $0$ and time $2$, and then also solves a medium problem between time $2$ and time $5$. In the meantime, the second contestant solves another medium problem between time $0$ and time $3$, while the third contestant solves a hard problem between time $0$ and time $4$.</p><p>In the <span class="tex-font-style-bf">third sample</span>, the contest only has medium and hard problems, and there is not enough time to solve any of them.</p>
