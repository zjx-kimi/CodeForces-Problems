## Description

<div><p><span class="tex-font-style-bf">Note that the memory limit is unusual.</span></p><p>There are $n$ chefs numbered $1, 2, \ldots, n$ that must prepare dishes for a king. Chef $i$ has skill $i$ and initially has a dish of tastiness $a_i$ where $|a_i| \leq i$. Each chef has a list of other chefs that he is allowed to copy from. To stop chefs from learning bad habits, the king makes sure that chef $i$ can only copy from chefs of larger skill.</p><p>There are a sequence of days that pass during which the chefs can work on their dish. During each day, there are two stages during which a chef can change the tastiness of their dish. </p><ol> <li> At the beginning of each day, each chef can <span class="tex-font-style-it">choose</span> to work (or not work) on their own dish, thereby multiplying the tastiness of their dish of their skill ($a_i := i \cdot a_i$) (or doing nothing).</li><li> After all chefs (who wanted) worked on their own dishes, each start observing the other chefs. In particular, for each chef $j$ on chef $i$'s list, chef $i$ can <span class="tex-font-style-it">choose</span> to copy (or not copy) $j$'s dish, thereby adding the tastiness of the $j$'s dish to $i$'s dish ($a_i := a_i + a_j$) (or doing nothing). It can be assumed that all copying occurs simultaneously. Namely, if chef $i$ chooses to copy from chef $j$ he will copy the tastiness of chef $j$'s dish at the end of stage $1$.</li></ol><p>All chefs work to maximize the tastiness of their <span class="tex-font-style-it">own</span> dish in order to please the king.</p><p>Finally, you are given $q$ queries. Each query is one of two types.</p><ol> <li> $1$ $k$ $l$ $r$&nbsp;— find the sum of tastiness $a_l, a_{l+1}, \ldots, a_{r}$ after the $k$-th day. Because this value can be large, find it modulo $10^9 + 7$. </li><li> $2$ $i$ $x$&nbsp;— the king adds $x$ tastiness to the $i$-th chef's dish before the $1$-st day begins ($a_i := a_i + x$). Note that, because the king wants to see tastier dishes, he only adds positive tastiness ($x &gt; 0$). </li></ol><p>Note that queries of type $1$ are independent of each all other queries. Specifically, each query of type $1$ is a <span class="tex-font-style-it">scenario</span> and does not change the initial tastiness $a_i$ of any dish for future queries. Note that queries of type $2$ are cumulative and only change the initial tastiness $a_i$ of a dish. See notes for an example of queries.</p></div><div class="input-specification"><p>The first line contains a single integer $n$ ($1 \le n \le 300$)&nbsp;— the number of chefs.</p><p>The second line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($-i \le a_i \le i$).</p><p>The next $n$ lines each begin with a integer $c_i$ ($0 \le c_i &lt; n$), denoting the number of chefs the $i$-th chef can copy from. This number is followed by $c_i$ distinct integers $d$ ($i &lt; d \le n$), signifying that chef $i$ is allowed to copy from chef $d$ during stage $2$ of each day.</p><p>The next line contains a single integer $q$ ($1 \le q \le 2 \cdot 10^5$)&nbsp;— the number of queries.</p><p>Each of the next $q$ lines contains a query of one of two types: </p><ul> <li> $1$ $k$ $l$ $r$ ($1 \le l \le r \le n$; $1 \le k \le 1000$); </li><li> $2$ $i$ $x$ ($1 \le i \le n$; $1 \le x \le 1000$). </li></ul><p>It is guaranteed that there is at least one query of the first type.</p></div><div class="output-specification"><p>For each query of the first type, print a single integer&nbsp;— the answer to the query.</p></div>

## Input

<p>The first line contains a single integer $n$ ($1 \le n \le 300$)&nbsp;— the number of chefs.</p><p>The second line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($-i \le a_i \le i$).</p><p>The next $n$ lines each begin with a integer $c_i$ ($0 \le c_i &lt; n$), denoting the number of chefs the $i$-th chef can copy from. This number is followed by $c_i$ distinct integers $d$ ($i &lt; d \le n$), signifying that chef $i$ is allowed to copy from chef $d$ during stage $2$ of each day.</p><p>The next line contains a single integer $q$ ($1 \le q \le 2 \cdot 10^5$)&nbsp;— the number of queries.</p><p>Each of the next $q$ lines contains a query of one of two types: </p><ul> <li> $1$ $k$ $l$ $r$ ($1 \le l \le r \le n$; $1 \le k \le 1000$); </li><li> $2$ $i$ $x$ ($1 \le i \le n$; $1 \le x \le 1000$). </li></ul><p>It is guaranteed that there is at least one query of the first type.</p>

## Output

<p>For each query of the first type, print a single integer&nbsp;— the answer to the query.</p>





```input1
5
1 0 -2 -2 4
4 2 3 4 5
1 3
1 4
1 5
0
7
1 1 1 5
2 4 3
1 1 1 5
2 3 2
1 2 2 4
2 5 1
1 981 4 5
```




```output1
57
71
316
278497818
```



## Note

<p>Below is the set of chefs that each chef is allowed to copy from:</p><ul> <li> $1$: $\{2, 3, 4, 5\}$ </li><li> $2$: $\{3\}$ </li><li> $3$: $\{4\}$ </li><li> $4$: $\{5\}$ </li><li> $5$: $\emptyset$ (no other chefs)</li></ul><p>Following is a description of the sample.</p><p>For the first query of type $1$, the initial tastiness values are $[1, 0, -2, -2, 4]$.</p><p>The final result of the first day is shown below: </p><ol> <li> $[1, 0, -2, -2, 20]$ (chef $5$ works on his dish). </li><li> $[21, 0, -2, 18, 20]$ (chef $1$ and chef $4$ copy from chef $5$). </li></ol><p>So, the answer for the $1$-st query is $21 + 0 - 2 + 18 + 20 = 57$.</p><p>For the $5$-th query ($3$-rd of type $1$). The initial tastiness values are now $[1, 0, 0, 1, 4]$.</p><p><span class="tex-font-style-bf">Day 1</span> </p><ol> <li> $[1, 0, 0, 4, 20]$ (chefs $4$ and $5$ work on their dishes). </li><li> $[25,0, 4, 24, 20]$ (chef $1$ copies from chefs $4$ and $5$, chef $3$ copies from chef $4$, chef $4$ copies from chef $5$). </li></ol><p><span class="tex-font-style-bf">Day 2</span> </p><ol> <li> $[25, 0, 12, 96, 100]$ (all chefs but chef $2$ work on their dish). </li><li> $[233, 12, 108, 196, 100]$ (chef $1$ copies from chefs $3$, $4$ and $5$, chef $2$ from $3$, chef $3$ from $4$, chef $4$ from chef $5$).<p>So, the answer for the $5$-th query is $12+108+196=316$. </p></li></ol><p>It can be shown that, in each step we described, all chefs moved optimally.</p>
