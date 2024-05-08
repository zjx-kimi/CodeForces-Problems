## Description

<div><p>In this problem, you are initially given an empty multiset. You have to process two types of queries:</p><ol> <li> <span class="tex-font-style-tt">ADD</span> $x$ — add an element equal to $2^{x}$ to the multiset; </li><li> <span class="tex-font-style-tt">GET</span> $w$ — say whether it is possible to take the sum of some subset of the current multiset and get a value equal to $w$. </li></ol></div><div class="input-specification"><p>The first line contains one integer $m$ ($1 \le m \le 10^5$) — the number of queries.</p><p>Then $m$ lines follow, each of which contains two integers $t_i$, $v_i$, denoting the $i$-th query. If $t_i = 1$, then the $i$-th query is <span class="tex-font-style-tt">ADD</span> $v_i$ ($0 \le v_i \le 29$). If $t_i = 2$, then the $i$-th query is <span class="tex-font-style-tt">GET</span> $v_i$ ($0 \le v_i \le 10^9$).</p></div><div class="output-specification"><p>For each <span class="tex-font-style-tt">GET</span> query, print <span class="tex-font-style-tt">YES</span> if it is possible to choose a subset with sum equal to $w$, or <span class="tex-font-style-tt">NO</span> if it is impossible.</p></div>

## Input

<p>The first line contains one integer $m$ ($1 \le m \le 10^5$) — the number of queries.</p><p>Then $m$ lines follow, each of which contains two integers $t_i$, $v_i$, denoting the $i$-th query. If $t_i = 1$, then the $i$-th query is <span class="tex-font-style-tt">ADD</span> $v_i$ ($0 \le v_i \le 29$). If $t_i = 2$, then the $i$-th query is <span class="tex-font-style-tt">GET</span> $v_i$ ($0 \le v_i \le 10^9$).</p>

## Output

<p>For each <span class="tex-font-style-tt">GET</span> query, print <span class="tex-font-style-tt">YES</span> if it is possible to choose a subset with sum equal to $w$, or <span class="tex-font-style-tt">NO</span> if it is impossible.</p>





```input1|
5
1 0
1 0
1 0
2 3
2 4
```




```input2|
7
1 0
1 1
1 2
1 10
2 4
2 6
2 7
```




```output1
YES
NO
```




```output2
YES
YES
YES
```


