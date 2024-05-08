## Description

<div><p>The Oak has $n$ nesting places, numbered with integers from $1$ to $n$. Nesting place $i$ is home to $b_i$ bees and $w_i$ wasps.</p><p>Some nesting places are connected by branches. We call two nesting places <span class="tex-font-style-underline">adjacent</span> if there exists a branch between them. A <span class="tex-font-style-underline">simple path</span> from nesting place $x$ to $y$ is given by a sequence $s_0, \ldots, s_p$ of distinct nesting places, where $p$ is a non-negative integer, $s_0 = x$, $s_p = y$, and $s_{i-1}$ and $s_{i}$ are adjacent for each $i = 1, \ldots, p$. The branches of The Oak are set up in such a way that for any two pairs of nesting places $x$ and $y$, there exists a unique simple path from $x$ to $y$. Because of this, biologists and computer scientists agree that The Oak is in fact, a tree.</p><p>A <span class="tex-font-style-underline">village</span> is a <span class="tex-font-style-underline">nonempty</span> set $V$ of nesting places such that for any two $x$ and $y$ in $V$, there exists a simple path from $x$ to $y$ whose intermediate nesting places all lie in $V$. </p><p>A set of villages $\cal P$ is called a <span class="tex-font-style-underline">partition</span> if each of the $n$ nesting places is contained in exactly one of the villages in $\cal P$. In other words, no two villages in $\cal P$ share any common nesting place, and altogether, they contain all $n$ nesting places.</p><p>The Oak holds its annual Miss Punyverse beauty pageant. The two contestants this year are Ugly Wasp and Pretty Bee. The winner of the beauty pageant is determined by voting, which we will now explain. Suppose $\mathcal{P}$ is a partition of the nesting places into $m$ villages $V_1, \ldots, V_m$. There is a local election in each village. Each of the insects in this village vote for their favorite contestant. If there are <span class="tex-font-style-bf">strictly</span> more votes for Ugly Wasp than Pretty Bee, then Ugly Wasp is said to <span class="tex-font-style-it">win</span> in that village. Otherwise, Pretty Bee <span class="tex-font-style-it">wins</span>. Whoever wins in the most number of villages wins.</p><p>As it always goes with these pageants, bees always vote for the bee (which is Pretty Bee this year) and wasps always vote for the wasp (which is Ugly Wasp this year). Unlike their general elections, no one abstains from voting for Miss Punyverse as everyone takes it very seriously.</p><p>Mayor Waspacito, and his assistant Alexwasp, wants Ugly Wasp to win. He has the power to choose how to partition The Oak into exactly $m$ villages. If he chooses the partition optimally, determine the maximum number of villages in which Ugly Wasp wins.</p></div><div class="input-specification"><p>The first line of input contains a single integer $t$ ($1 \le t \le 100$) denoting the number of test cases. The next lines contain descriptions of the test cases. </p><p>The first line of each test case contains two space-separated integers $n$ and $m$ ($1 \le m \le n \le 3000$). The second line contains $n$ space-separated integers $b_1, b_2, \ldots, b_n$ ($0 \le b_i \le 10^9$). The third line contains $n$ space-separated integers $w_1, w_2, \ldots, w_n$ ($0 \le w_i \le 10^9$). The next $n - 1$ lines describe the pairs of adjacent nesting places. In particular, the $i$-th of them contains two space-separated integers $x_i$ and $y_i$ ($1 \le x_i, y_i \le n$, $x_i \neq y_i$) denoting the numbers of two adjacent nesting places. It is guaranteed that these pairs form a tree.</p><p>It is guaranteed that the sum of $n$ in a single file is at most $10^5$.</p></div><div class="output-specification"><p>For each test case, output a single line containing a single integer denoting the maximum number of villages in which Ugly Wasp wins, among all partitions of The Oak into $m$ villages.</p></div>

## Input

<p>The first line of input contains a single integer $t$ ($1 \le t \le 100$) denoting the number of test cases. The next lines contain descriptions of the test cases. </p><p>The first line of each test case contains two space-separated integers $n$ and $m$ ($1 \le m \le n \le 3000$). The second line contains $n$ space-separated integers $b_1, b_2, \ldots, b_n$ ($0 \le b_i \le 10^9$). The third line contains $n$ space-separated integers $w_1, w_2, \ldots, w_n$ ($0 \le w_i \le 10^9$). The next $n - 1$ lines describe the pairs of adjacent nesting places. In particular, the $i$-th of them contains two space-separated integers $x_i$ and $y_i$ ($1 \le x_i, y_i \le n$, $x_i \neq y_i$) denoting the numbers of two adjacent nesting places. It is guaranteed that these pairs form a tree.</p><p>It is guaranteed that the sum of $n$ in a single file is at most $10^5$.</p>

## Output

<p>For each test case, output a single line containing a single integer denoting the maximum number of villages in which Ugly Wasp wins, among all partitions of The Oak into $m$ villages.</p>





```input1
2
4 3
10 160 70 50
70 111 111 0
1 2
2 3
3 4
2 1
143 420
214 349
2 1
```




```output1
2
0
```



## Note

<p>In the first test case, we need to partition the $n = 4$ nesting places into $m = 3$ villages. We can make Ugly Wasp win in $2$ villages via the following partition: $\{\{1, 2\}, \{3\}, \{4\}\}$. In this partition,</p><ul> <li> Ugly Wasp wins in village $\{1, 2\}$, garnering $181$ votes as opposed to Pretty Bee's $170$; </li><li> Ugly Wasp also wins in village $\{3\}$, garnering $111$ votes as opposed to Pretty Bee's $70$; </li><li> Ugly Wasp loses in the village $\{4\}$, garnering $0$ votes as opposed to Pretty Bee's $50$. </li></ul><p>Thus, Ugly Wasp wins in $2$ villages, and it can be shown that this is the maximum possible number.</p><p>In the second test case, we need to partition the $n = 2$ nesting places into $m = 1$ village. There is only one way to do this: $\{\{1, 2\}\}$. In this partition's sole village, Ugly Wasp gets $563$ votes, and Pretty Bee also gets $563$ votes. Ugly Wasp needs strictly more votes in order to win. Therefore, Ugly Wasp doesn't win in any village.</p>
