## Description

<div><p>You are given a multiset $S$. Initially, $S = \{1,2,3, \ldots, n\}$.</p><p>You will perform the following operation $n-1$ times.</p><ul> <li> Choose the largest number $S_{\text{max}}$ in $S$ and the smallest number $S_{\text{min}}$ in $S$. Remove the two numbers from $S$, and add $S_{\text{max}} - S_{\text{min}}$ into $S$. </li></ul><p>It's easy to show that there will be exactly one number left after $n-1$ operations. Output that number.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 10^5$) — the number of test cases. Their description follows.</p><p>For each test case, one single line contains a single integer $n$ ($2 \le n \le 10^9$) — the initial size of the multiset $S$.</p></div><div class="output-specification"><p>For each test case, output an integer denoting the only number left after $n-1$ operations.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 10^5$) — the number of test cases. Their description follows.</p><p>For each test case, one single line contains a single integer $n$ ($2 \le n \le 10^9$) — the initial size of the multiset $S$.</p>

## Output

<p>For each test case, output an integer denoting the only number left after $n-1$ operations.</p>





```input1|2,4,6
5
2
4
7
15
177567
```




```output1
1
2
2
4
33914
```



## Note

<p>We show how the multiset $S$ changes for $n=4$.</p><ul><li> Operation $1$: $S=\{1,2,3,4\}$, remove $4$, $1$, add $3$.</li><li> Operation $2$: $S=\{2,3,3\}$, remove $3$, $2$, add $1$.</li><li> Operation $3$: $S=\{1,3\}$, remove $3$, $1$, add $2$.</li><li> Final: $S = \{2\}$.</li></ul><p>Thus, the answer for $n = 4$ is $2$.</p>
