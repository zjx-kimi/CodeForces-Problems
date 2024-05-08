## Description

<div><p>You are given a string $s$ consisting of $n$ characters <span class="tex-font-style-tt">0</span> and/or <span class="tex-font-style-tt">1</span>.</p><p>You make $m$ copies of this string, let the $i$-th copy be the string $t_i$. Then you perform exactly one operation on each of the copies: for the $i$-th copy, you sort its substring $[l_i; r_i]$ (the substring from the $l_i$-th character to the $r_i$-th character, both endpoints inclusive). <span class="tex-font-style-bf">Note that each operation affects only one copy, and each copy is affected by only one operation</span>.</p><p>Your task is to calculate the number of different strings among $t_1, t_2, \ldots, t_m$. Note that the initial string $s$ should be counted only if at least one of the copies stays the same after the operation.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains two integers $n$ and $m$ ($1 \le n, m \le 2 \cdot 10^5$) — the length of $s$ and the number of copies, respectively.</p><p>The second line contains $n$ characters <span class="tex-font-style-tt">0</span> and/or <span class="tex-font-style-tt">1</span> — the string $s$.</p><p>Then $m$ lines follow. The $i$-th of them contains two integers $l_i$ and $r_i$ ($1 \le l_i \le r_i \le n$) — the description of the operation applied to the $i$-th copy.</p><p>The sum of $n$ over all test cases doesn't exceed $2 \cdot 10^5$. The sum of $m$ over all test cases doesn't exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>Print one integer — the number of different strings among $t_1, t_2, \ldots, t_m$.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains two integers $n$ and $m$ ($1 \le n, m \le 2 \cdot 10^5$) — the length of $s$ and the number of copies, respectively.</p><p>The second line contains $n$ characters <span class="tex-font-style-tt">0</span> and/or <span class="tex-font-style-tt">1</span> — the string $s$.</p><p>Then $m$ lines follow. The $i$-th of them contains two integers $l_i$ and $r_i$ ($1 \le l_i \le r_i \le n$) — the description of the operation applied to the $i$-th copy.</p><p>The sum of $n$ over all test cases doesn't exceed $2 \cdot 10^5$. The sum of $m$ over all test cases doesn't exceed $2 \cdot 10^5$.</p>

## Output

<p>Print one integer — the number of different strings among $t_1, t_2, \ldots, t_m$.</p>





```input1|2,3,4,5,6,7,8,15,16,17
3
6 5
101100
1 2
1 3
2 4
5 5
1 6
6 4
100111
2 2
1 4
1 3
1 2
1 1
0
1 1
```




```output1
3
3
1
```



## Note

<p>Consider the first example. Copies below are given in order of the input operations. Underlined substrings are substrings that are sorted:</p><ol> <li> <span class="tex-font-style-tt"><span class="tex-font-style-underline">10</span>1100</span> $\rightarrow$ <span class="tex-font-style-tt"><span class="tex-font-style-underline">01</span>1100</span>; </li><li> <span class="tex-font-style-tt"><span class="tex-font-style-underline">101</span>100</span> $\rightarrow$ <span class="tex-font-style-tt"><span class="tex-font-style-underline">011</span>100</span>; </li><li> <span class="tex-font-style-tt">1<span class="tex-font-style-underline">011</span>00</span> $\rightarrow$ <span class="tex-font-style-tt">1<span class="tex-font-style-underline">011</span>00</span>; </li><li> <span class="tex-font-style-tt">1011<span class="tex-font-style-underline">0</span>0</span> $\rightarrow$ <span class="tex-font-style-tt">1011<span class="tex-font-style-underline">0</span>0</span>; </li><li> <span class="tex-font-style-tt"><span class="tex-font-style-underline">101100</span></span> $\rightarrow$ <span class="tex-font-style-tt"><span class="tex-font-style-underline">000111</span></span>. </li></ol><p>There are three different strings among $t_1, t_2, t_3, t_4, t_5$: <span class="tex-font-style-tt">000111</span>, <span class="tex-font-style-tt">011100</span> and <span class="tex-font-style-tt">101100</span>.</p><p>Consider the second example:</p><ol> <li> <span class="tex-font-style-tt">1<span class="tex-font-style-underline">0</span>0111</span> $\rightarrow$ <span class="tex-font-style-tt">1<span class="tex-font-style-underline">0</span>0111</span>; </li><li> <span class="tex-font-style-tt"><span class="tex-font-style-underline">1001</span>11</span> $\rightarrow$ <span class="tex-font-style-tt"><span class="tex-font-style-underline">0011</span>11</span>; </li><li> <span class="tex-font-style-tt"><span class="tex-font-style-underline">100</span>111</span> $\rightarrow$ <span class="tex-font-style-tt"><span class="tex-font-style-underline">001</span>111</span>; </li><li> <span class="tex-font-style-tt"><span class="tex-font-style-underline">10</span>0111</span> $\rightarrow$ <span class="tex-font-style-tt"><span class="tex-font-style-underline">01</span>0111</span>. </li></ol><p>There are three different strings among $t_1, t_2, t_3, t_4$: <span class="tex-font-style-tt">001111</span>, <span class="tex-font-style-tt">010111</span> and <span class="tex-font-style-tt">100111</span>.</p>
