## Description

<div><p>Ntarsis has been given a set $S$, initially containing integers $1, 2, 3, \ldots, 10^{1000}$ in sorted order. Every day, he will remove the $a_1$-th, $a_2$-th, $\ldots$, $a_n$-th smallest numbers in $S$ <span class="tex-font-style-bf">simultaneously</span>.</p><p>What is the smallest element in $S$ after $k$ days?</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^5$). The description of the test cases follows.</p><p>The first line of each test case consists of two integers $n$ and $k$ ($1 \leq n,k \leq 2 \cdot 10^5$)&nbsp;— the length of $a$ and the number of days.</p><p>The following line of each test case consists of $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \leq a_i \leq 10^9$)&nbsp;— the elements of array $a$.</p><p>It is guaranteed that: </p><ul> <li> The sum of $n$ over all test cases won't exceed $2 \cdot 10^5$; </li><li> The sum of $k$ over all test cases won't exceed $2 \cdot 10^5$; </li><li> $a_1 &lt; a_2 &lt; \cdots &lt; a_n$ for all test cases. </li></ul></div><div class="output-specification"><p>For each test case, print an integer that is the smallest element in $S$ after $k$ days.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^5$). The description of the test cases follows.</p><p>The first line of each test case consists of two integers $n$ and $k$ ($1 \leq n,k \leq 2 \cdot 10^5$)&nbsp;— the length of $a$ and the number of days.</p><p>The following line of each test case consists of $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \leq a_i \leq 10^9$)&nbsp;— the elements of array $a$.</p><p>It is guaranteed that: </p><ul> <li> The sum of $n$ over all test cases won't exceed $2 \cdot 10^5$; </li><li> The sum of $k$ over all test cases won't exceed $2 \cdot 10^5$; </li><li> $a_1 &lt; a_2 &lt; \cdots &lt; a_n$ for all test cases. </li></ul>

## Output

<p>For each test case, print an integer that is the smallest element in $S$ after $k$ days.</p>





```input1|2,3,6,7,10,11,14,15
7
5 1
1 2 4 5 6
5 3
1 3 5 6 7
4 1000
2 3 4 5
9 1434
1 4 7 9 12 15 17 18 20
10 4
1 3 5 7 9 11 13 15 17 19
10 6
1 4 7 10 13 16 19 22 25 28
10 150000
1 3 4 5 10 11 12 13 14 15
```




```output1
3
9
1
12874
16
18
1499986
```



## Note

<p>For the first test case, each day the $1$-st, $2$-nd, $4$-th, $5$-th, and $6$-th smallest elements need to be removed from $S$. So after the first day, $S$ will become $\require{cancel}$ $\{\cancel 1, \cancel 2, 3, \cancel 4, \cancel 5, \cancel 6, 7, 8, 9, \ldots\} = \{3, 7, 8, 9, \ldots\}$. The smallest element is $3$.</p><p>For the second case, each day the $1$-st, $3$-rd, $5$-th, $6$-th and $7$-th smallest elements need to be removed from $S$. $S$ will be changed as follows:</p><center> <table class="tex-tabular"><tbody><tr><td class="tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-bottom">Day</td><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-bottom">$S$ before</td><td class="tex-tabular-text-align-center tex-tabular-border-bottom"></td><td class="tex-tabular-text-align-left tex-tabular-border-bottom">$S$ after</td></tr><tr><td class="tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top">1</td><td class="tex-tabular-border-left tex-tabular-text-align-left tex-tabular-border-top">$\{\cancel 1, 2, \cancel 3, 4, \cancel 5, \cancel 6, \cancel 7, 8, 9, 10, \ldots \}$</td><td class="tex-tabular-text-align-center tex-tabular-border-top">$\to$</td><td class="tex-tabular-text-align-left tex-tabular-border-top">$\{2, 4, 8, 9, 10, \ldots\}$</td></tr><tr><td class="tex-tabular-text-align-center tex-tabular-border-right">2</td><td class="tex-tabular-border-left tex-tabular-text-align-left">$\{\cancel 2, 4, \cancel 8, 9, \cancel{10}, \cancel{11}, \cancel{12}, 13, 14, 15, \ldots\}$</td><td class="tex-tabular-text-align-center">$\to$</td><td class="tex-tabular-text-align-left">$\{4, 9, 13, 14, 15, \ldots\}$</td></tr><tr><td class="tex-tabular-text-align-center tex-tabular-border-right">3</td><td class="tex-tabular-border-left tex-tabular-text-align-left">$\{\cancel 4, 9, \cancel{13}, 14, \cancel{15}, \cancel{16}, \cancel{17}, 18, 19, 20, \ldots\}$</td><td class="tex-tabular-text-align-center">$\to$</td><td class="tex-tabular-text-align-left">$\{9, 14, 18, 19, 20, \ldots\}$</td></tr></tbody></table> </center><p>The smallest element left after $k = 3$ days is $9$.</p>
