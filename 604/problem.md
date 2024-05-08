## Description

<div><div class="epigraph"><div class="epigraph-text"><span class="tex-font-style-it">Because to take away a man's freedom of choice, even his freedom to make the wrong choice, is to manipulate him as though he were a puppet and not a person.</span></div><div class="epigraph-source">— Madeleine L'Engle</div></div><p>There are $n$ programmers choosing their favorite algorithm amongst $m$ different choice options. Before the first round, all $m$ options are available. In each round, every programmer makes a vote for one of the remaining algorithms. After the round, only the algorithms with the maximum number of votes remain. The voting process ends when there is only one option left. Determine whether the voting process can continue indefinitely or no matter how people vote, they will eventually choose a single option after some finite amount of rounds?</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \leq t \leq 10^5$) — the number of test cases.</p><p>Each test case consists of a single line containing two integers $n$ and $m$ ($1 \leq n, m \leq 10^6$) — the number of people and choice options respectively.</p></div><div class="output-specification"><p>For each test case output "<span class="tex-font-style-tt">YES</span>" if the programmers will eventually choose a single option, and "<span class="tex-font-style-tt">NO</span>" otherwise.</p><p>You may print each letter in any case (for example, <span class="tex-font-style-tt">YES</span>, <span class="tex-font-style-tt">Yes</span>, <span class="tex-font-style-tt">yes</span>, <span class="tex-font-style-tt">yEs</span> will all be recognized as a positive answer).</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \leq t \leq 10^5$) — the number of test cases.</p><p>Each test case consists of a single line containing two integers $n$ and $m$ ($1 \leq n, m \leq 10^6$) — the number of people and choice options respectively.</p>

## Output

<p>For each test case output "<span class="tex-font-style-tt">YES</span>" if the programmers will eventually choose a single option, and "<span class="tex-font-style-tt">NO</span>" otherwise.</p><p>You may print each letter in any case (for example, <span class="tex-font-style-tt">YES</span>, <span class="tex-font-style-tt">Yes</span>, <span class="tex-font-style-tt">yes</span>, <span class="tex-font-style-tt">yEs</span> will all be recognized as a positive answer).</p>





```input1|2,4,6
5
3 2
4 2
5 3
1000000 1000000
1 1000000
```




```output1
YES
NO
YES
NO
YES
```



## Note

<p>In the first example, there are $8$ ways people could vote: $\{1|1|1, 1|1|2, 1|2|1, 1|2|2, 2|1|1, 2|1|2, 2|2|1, 2|2|2\}$.</p><p>In cases $1$, $2$, $3$, and $5$, the programmers are left with the first algorithm, and in the remaining cases people are left with the second one, so the voting ends in one round in any case.</p><p>In the second example, the programmers could always vote $1|1|2|2$. Both algorithms have the maximum number of votes and remain for the next round, so the voting never ends.</p>
