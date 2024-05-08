## Description

<div><p>During Zhongkao examination, Reycloer met an interesting problem, but he cannot come up with a solution immediately. Time is running out! Please help him.</p><p>Initially, you are given an array $a$ consisting of $n \ge 2$ integers, and you want to change all elements in it to $0$.</p><p>In one operation, you select two indices $l$ and $r$ ($1\le l\le r\le n$) and do the following:</p><ul> <li> Let $s=a_l\oplus a_{l+1}\oplus \ldots \oplus a_r$, where $\oplus$ denotes the <a href="https://en.wikipedia.org/wiki/Bitwise_operation#XOR">bitwise XOR operation</a>; </li><li> Then, for all $l\le i\le r$, replace $a_i$ with $s$. </li></ul><p>You can use the operation above in any order at most $8$ times in total.</p><p>Find a sequence of operations, such that after performing the operations in order, all elements in $a$ are equal to $0$. It can be proven that the solution always exists.</p></div><div class="input-specification"><p>The first line of input contains a single integer $t$ ($1\le t\le 500$) — the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2\le n\le 100$) — the length of the array $a$.</p><p>The second line of each test case contains $n$ integers $a_1,a_2,\ldots,a_n$ ($0\le a_i\le 100$) — the elements of the array $a$.</p></div><div class="output-specification"><p>For each test case, in the first line output a single integer $k$ ($0\le k\le 8$) — the number of operations you use.</p><p>Then print $k$ lines, in the $i$-th line output two integers $l_i$ and $r_i$ ($1\le l_i\le r_i\le n$) representing that you select $l_i$ and $r_i$ in the $i$-th operation. </p><p>Note that you <span class="tex-font-style-bf">do not</span> have to minimize $k$. If there are multiple solutions, you may output any of them.</p></div>

## Input

<p>The first line of input contains a single integer $t$ ($1\le t\le 500$) — the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2\le n\le 100$) — the length of the array $a$.</p><p>The second line of each test case contains $n$ integers $a_1,a_2,\ldots,a_n$ ($0\le a_i\le 100$) — the elements of the array $a$.</p>

## Output

<p>For each test case, in the first line output a single integer $k$ ($0\le k\le 8$) — the number of operations you use.</p><p>Then print $k$ lines, in the $i$-th line output two integers $l_i$ and $r_i$ ($1\le l_i\le r_i\le n$) representing that you select $l_i$ and $r_i$ in the $i$-th operation. </p><p>Note that you <span class="tex-font-style-bf">do not</span> have to minimize $k$. If there are multiple solutions, you may output any of them.</p>





```input1|2,3,6,7,10,11
6
4
1 2 3 0
8
3 1 4 1 5 9 2 6
6
1 5 4 1 4 7
5
0 0 0 0 0
7
1 1 9 9 0 1 8
3
100 100 0
```




```output1
1
1 4
2
4 7
1 8
6
1 2
3 4
5 6
1 3
4 6
1 6
0
4
1 2
6 7
3 4
6 7
1
1 2
```



## Note

<p>In the first test case, since $1\oplus2\oplus3\oplus0=0$, after performing the operation on segment $[1,4]$, all the elements in the array are equal to $0$.</p><p>In the second test case, after the first operation, the array becomes equal to $[3,1,4,15,15,15,15,6]$, after the second operation, the array becomes equal to $[0,0,0,0,0,0,0,0]$.</p><p>In the third test case:</p><center> <table class="tex-tabular"><tbody><tr><td class="tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-bottom">Operation</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-bottom">$a$ before</td><td class="tex-tabular-text-align-center tex-tabular-border-bottom"></td><td class="tex-tabular-text-align-center tex-tabular-border-bottom">$a$ after</td></tr><tr><td class="tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">$1$</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-top tex-tabular-border-bottom">$[\underline{1,5},4,1,4,7]$</td><td class="tex-tabular-text-align-center tex-tabular-border-top tex-tabular-border-bottom">$\rightarrow$</td><td class="tex-tabular-text-align-center tex-tabular-border-top tex-tabular-border-bottom">$[4,4,4,1,4,7]$</td></tr><tr><td class="tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">$2$</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-top tex-tabular-border-bottom">$[4,4,\underline{4,1},4,7]$</td><td class="tex-tabular-text-align-center tex-tabular-border-top tex-tabular-border-bottom">$\rightarrow$</td><td class="tex-tabular-text-align-center tex-tabular-border-top tex-tabular-border-bottom">$[4,4,5,5,4,7]$</td></tr><tr><td class="tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">$3$</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-top tex-tabular-border-bottom">$[4,4,5,5,\underline{4,7}]$</td><td class="tex-tabular-text-align-center tex-tabular-border-top tex-tabular-border-bottom">$\rightarrow$</td><td class="tex-tabular-text-align-center tex-tabular-border-top tex-tabular-border-bottom">$[4,4,5,5,3,3]$</td></tr><tr><td class="tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">$4$</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-top tex-tabular-border-bottom">$[\underline{4,4,5},5,3,3]$</td><td class="tex-tabular-text-align-center tex-tabular-border-top tex-tabular-border-bottom">$\rightarrow$</td><td class="tex-tabular-text-align-center tex-tabular-border-top tex-tabular-border-bottom">$[5,5,5,5,3,3]$</td></tr><tr><td class="tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top tex-tabular-border-bottom">$5$</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-top tex-tabular-border-bottom">$[5,5,5,\underline{5,3,3}]$</td><td class="tex-tabular-text-align-center tex-tabular-border-top tex-tabular-border-bottom">$\rightarrow$</td><td class="tex-tabular-text-align-center tex-tabular-border-top tex-tabular-border-bottom">$[5,5,5,5,5,5]$</td></tr><tr><td class="tex-tabular-text-align-center tex-tabular-border-right tex-tabular-border-top">$6$</td><td class="tex-tabular-border-left tex-tabular-text-align-center tex-tabular-border-top">$[\underline{5,5,5,5,5,5}]$</td><td class="tex-tabular-text-align-center tex-tabular-border-top">$\rightarrow$</td><td class="tex-tabular-text-align-center tex-tabular-border-top">$[0,0,0,0,0,0]$</td></tr></tbody></table> </center><p>In the fourth test case, the initial array contains only $0$, so we do not need to perform any operations with it.</p>
