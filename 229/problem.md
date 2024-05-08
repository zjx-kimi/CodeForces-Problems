## Description

<div><p>Let $f$($x$) be the floor of the binary logarithm of $x$. In other words, $f$($x$) is largest non-negative integer $y$, such that $2^y$ does not exceed $x$.</p><p>Let $g$($x$) be the floor of the logarithm of $x$ with base $f$($x$). In other words, $g$($x$) is the largest non-negative integer $z$, such that ${f(x)}^{z}$ does not exceed $x$.</p><p>You are given $q$ queries. The $i$-th query consists of two integers $l_i$ and $r_i$. The answer to the query is the sum of $g$($k$) across all integers $k$, such that $l_i \leq k \leq r_i$. Since the answers might be large, print them modulo ${10^9 + 7}$.</p></div><div class="input-specification"><p>The first line contains a single integer $q$ — the number of queries ($1 \leq q \leq 10^5$).</p><p>The next $q$ lines each contain two integers $l_i$ and $r_i$ — the bounds of the $i$-th query ($4 \leq l_i \leq r_i \leq 10^{18}$). </p></div><div class="output-specification"><p>For each query, output the answer to the query modulo $10^9 + 7$.</p></div>

## Input

<p>The first line contains a single integer $q$ — the number of queries ($1 \leq q \leq 10^5$).</p><p>The next $q$ lines each contain two integers $l_i$ and $r_i$ — the bounds of the $i$-th query ($4 \leq l_i \leq r_i \leq 10^{18}$). </p>

## Output

<p>For each query, output the answer to the query modulo $10^9 + 7$.</p>





```input1
12
4 6
4 7
4 8
4 100000
179 1000000000000000000
57 179
4 201018959
7 201018960
729 50624
728 50624
728 50625
729 50625
```




```output1
6
8
9
348641
41949982
246
1
0
149688
149690
149694
149692
```



## Note

<p>The table below contains the values of the functions $f$($x$) and $g$($x$) for all $x$ such that $1 \leq x \leq 8$. </p><center> <table class="tex-tabular"><tbody><tr><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">$x$</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">$1$</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">$2$</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">$3$</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">$4$</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">$5$</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">$6$</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">$7$</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">$8$</td></tr><tr><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">$f$</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">$0$</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">$1$</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">$1$</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">$2$</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">$2$</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">$2$</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">$2$</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">$3$</td></tr><tr><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">$g$</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">$-$</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">$-$</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">$-$</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">$2$</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">$2$</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">$2$</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">$2$</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">$1$</td></tr></tbody></table> </center>
