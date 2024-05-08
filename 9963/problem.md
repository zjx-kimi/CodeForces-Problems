## Description

<div><p>Anya is engaged in needlework. Today she decided to knit a scarf from semi-transparent threads. Each thread is characterized by a single integer — the transparency coefficient.</p><p>The scarf is made according to the following scheme: horizontal threads with transparency coefficients $a_1, a_2, \ldots, a_n$ and vertical threads with transparency coefficients $b_1, b_2, \ldots, b_m$ are selected. Then they are interwoven as shown in the picture below, forming a piece of fabric of size $n \times m$, consisting of exactly $nm$ nodes:</p><center>  <img class="tex-graphics" src="file://lEPvs4V1.png" style="max-width: 100.0%;max-height: 100.0%;" width="270px">   <span class="tex-font-size-small">Example of a piece of fabric for $n = m = 4$.</span> </center><p>After the interweaving tightens and there are no gaps between the threads, each node formed by a horizontal thread with number $i$ and a vertical thread with number $j$ will turn into a cell, which we will denote as $(i, j)$. Cell $(i, j)$ will have a transparency coefficient of $a_i + b_j$.</p><p>The <span class="tex-font-style-it">interestingness</span> of the resulting scarf will be the number of its sub-squares$^{\dagger}$ in which there are no pairs of neighboring$^{\dagger \dagger}$ cells with the same transparency coefficients.</p><p>Anya has not yet decided which threads to use for the scarf, so you will also be given $q$ queries to increase/decrease the coefficients for the threads on some ranges. After each query of which you need to output the interestingness of the resulting scarf.</p><p>$^{\dagger}$A sub-square of a piece of fabric is defined as the set of all its cells $(i, j)$, such that $x_0 \le i \le x_0 + d$ and $y_0 \le j \le y_0 + d$ for some integers $x_0$, $y_0$, and $d$ ($1 \le x_0 \le n - d$, $1 \le y_0 \le m - d$, $d \ge 0$).</p><p>$^{\dagger \dagger}$. Cells $(i_1, j_1)$ and $(i_2, j_2)$ are neighboring if and only if $|i_1 - i_2| + |j_1 - j_2| = 1$.</p></div><div class="input-specification"><p>The first line contains three integers $n$, $m$, and $q$ ($1 \le n, m \le 3 \cdot 10^5$, $0 \le q \le 3 \cdot 10^5$)&nbsp;— the number of horizontal threads, the number of vertical threads, and the number of change requests.</p><p>The second line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($-10^9 \le a_i \le 10^9$)&nbsp;— the transparency coefficients for the horizontal threads, with the threads numbered from top to bottom.</p><p>The third line contains $m$ integers $b_1, b_2, \ldots, b_m$ ($-10^9 \le b_i \le 10^9$)&nbsp;— the transparency coefficients for the vertical threads, with the threads numbered from left to right.</p><p>The next $q$ lines specify the change requests. Each request is described by a quadruple of integers $t$, $l$, $r$, and $x$ ($1 \le t \le 2$, $l \le r$, $-10^9 \le x \le 10^9$). Depending on the parameter $t$ in the request, the following actions are required:</p><ul> <li> $t=1$. The transparency coefficients for the horizontal threads in the range $[l, r]$ are increased by $x$ (in other words, for all integers $l \le i \le r$, the value of $a_i$ is increased by $x$); </li><li> $t=2$. The transparency coefficients for the vertical threads in the range $[l, r]$ are increased by $x$ (in other words, for all integers $l \le i \le r$, the value of $b_i$ is increased by $x$). </li></ul></div><div class="output-specification"><p>Output $(q+1)$ lines. In the $(i + 1)$-th line ($0 \le i \le q$), output a single integer — the interestingness of the scarf after applying the first $i$ requests.</p></div>

## Input

<p>The first line contains three integers $n$, $m$, and $q$ ($1 \le n, m \le 3 \cdot 10^5$, $0 \le q \le 3 \cdot 10^5$)&nbsp;— the number of horizontal threads, the number of vertical threads, and the number of change requests.</p><p>The second line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($-10^9 \le a_i \le 10^9$)&nbsp;— the transparency coefficients for the horizontal threads, with the threads numbered from top to bottom.</p><p>The third line contains $m$ integers $b_1, b_2, \ldots, b_m$ ($-10^9 \le b_i \le 10^9$)&nbsp;— the transparency coefficients for the vertical threads, with the threads numbered from left to right.</p><p>The next $q$ lines specify the change requests. Each request is described by a quadruple of integers $t$, $l$, $r$, and $x$ ($1 \le t \le 2$, $l \le r$, $-10^9 \le x \le 10^9$). Depending on the parameter $t$ in the request, the following actions are required:</p><ul> <li> $t=1$. The transparency coefficients for the horizontal threads in the range $[l, r]$ are increased by $x$ (in other words, for all integers $l \le i \le r$, the value of $a_i$ is increased by $x$); </li><li> $t=2$. The transparency coefficients for the vertical threads in the range $[l, r]$ are increased by $x$ (in other words, for all integers $l \le i \le r$, the value of $b_i$ is increased by $x$). </li></ul>

## Output

<p>Output $(q+1)$ lines. In the $(i + 1)$-th line ($0 \le i \le q$), output a single integer — the interestingness of the scarf after applying the first $i$ requests.</p>





```input1|
4 4 0
1 1 2 3
1 2 2 3
```




```input2|
3 3 2
1 1 1
2 2 8
1 2 3 1
2 2 3 -6
```




```input3|
3 2 2
-1000000000 0 1000000000
-1000000000 1000000000
1 1 1 1000000000
2 2 2 -1000000000
```




```output1
20
```




```output2
9
10
11
```




```output3
8
7
7
```



## Note

<p>In the first example, the transparency coefficients of the cells in the resulting plate are as follows:</p><center> <table class="tex-tabular"><tbody><tr><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">2</td><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">3</td><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">3</td><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">4</td></tr><tr><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">2</td><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">3</td><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">3</td><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">4</td></tr><tr><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">3</td><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">4</td><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">4</td><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">5</td></tr><tr><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">4</td><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">5</td><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">5</td><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">6</td></tr></tbody></table> </center><p>Then there are the following sub-squares that do not contain two neighboring cells with the same transparency coefficient:</p><ul><li> Each of the $16$ cells separately;</li><li> A sub-square with the upper left corner at cell $(3, 1)$ and the lower right corner at cell $(4, 2)$;</li><li> A sub-square with the upper left corner at cell $(2, 3)$ and the lower right corner at cell $(3, 4)$;</li><li> A sub-square with the upper left corner at cell $(2, 1)$ and the lower right corner at cell $(3, 2)$;</li><li> A sub-square with the upper left corner at cell $(3, 3)$ and the lower right corner at cell $(4, 4)$.</li></ul><p>In the second example, after the first query, the transparency coefficients of the horizontal threads are $[1, 2, 2]$. After the second query, the transparency coefficients of the vertical threads are $[2, -4, 2]$.</p>
