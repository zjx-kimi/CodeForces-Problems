## Description

<div><p>You are given an integer $n$ and $k$ intervals. The $i$-th interval is $[l_i,r_i]$ where $1 \leq l_i \leq r_i \leq n$.</p><p>Let us call a <span class="tex-font-style-bf">regular</span> bracket sequence$^{\dagger,\ddagger}$ of length $n$ <span class="tex-font-style-it">hyperregular</span> if for each $i$ such that $1 \leq i \leq k$, the substring $\overline{s_{l_i} s_{l_{i}+1} \ldots s_{r_i}}$ is also a regular bracket sequence.</p><p>Your task is to count the number of hyperregular bracket sequences. Since this number can be really large, you are only required to find it modulo $998\,244\,353$.</p><p>$^\dagger$ A bracket sequence is a string containing only the characters "<span class="tex-font-style-tt">(</span>" and "<span class="tex-font-style-tt">)</span>".</p><p>$^\ddagger$ A bracket sequence is called regular if one can turn it into a valid math expression by adding characters <span class="tex-font-style-tt">+</span> and <span class="tex-font-style-tt">1</span>. For example, sequences <span class="tex-font-style-tt">(())()</span>, <span class="tex-font-style-tt">()</span>, <span class="tex-font-style-tt">(()(()))</span> and the empty string are regular, while <span class="tex-font-style-tt">)(</span>, <span class="tex-font-style-tt">(()</span>, and <span class="tex-font-style-tt">(()))(</span> are not.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line of input contains a single integer $t$ ($1 \le t \le 10^5$)&nbsp;— the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains two integers $n$ and $k$ ($1 \le n \le 3 \cdot 10^5$, $0 \le k \le 3 \cdot 10^5$) — the length of the hyperregular bracket sequences and the number of intervals respectively.</p><p>The following $k$ lines of each test case contains two integers $l_i$ and $r_i$ ($1 \le l \le r \le n$).</p><p>It is guaranteed that the sum of $n$ across all test cases does not exceed $3 \cdot 10^5$ and the sum of $k$ across all test cases does not exceed $3 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output the number of hyperregular bracket sequences modulo $998\,244\,353$.</p></div>

## Input

<p>Each test contains multiple test cases. The first line of input contains a single integer $t$ ($1 \le t \le 10^5$)&nbsp;— the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains two integers $n$ and $k$ ($1 \le n \le 3 \cdot 10^5$, $0 \le k \le 3 \cdot 10^5$) — the length of the hyperregular bracket sequences and the number of intervals respectively.</p><p>The following $k$ lines of each test case contains two integers $l_i$ and $r_i$ ($1 \le l \le r \le n$).</p><p>It is guaranteed that the sum of $n$ across all test cases does not exceed $3 \cdot 10^5$ and the sum of $k$ across all test cases does not exceed $3 \cdot 10^5$.</p>

## Output

<p>For each test case, output the number of hyperregular bracket sequences modulo $998\,244\,353$.</p>





```input1|2,4,5,9,10,11,12,19,20,21,22
7
6 0
5 0
8 1
1 3
10 2
3 4
6 9
1000 3
100 701
200 801
300 901
28 5
1 12
3 20
11 14
4 9
18 19
4 3
1 4
1 4
1 4
```




```output1
5
0
0
4
839415253
140
2
```



## Note

<ul> <li> For the first testcase, the $5$ <span class="tex-font-style-it">hyperregular bracket strings</span> of length $6$ are: <span class="tex-font-style-tt">((()))</span>, <span class="tex-font-style-tt">(()())</span>, <span class="tex-font-style-tt">(())()</span>, <span class="tex-font-style-tt">()(())</span> and <span class="tex-font-style-tt">()()()</span>.</li><li> For the second testcase, there are no regular bracket strings of length $5$, and consequently, there are no <span class="tex-font-style-it">hyperregular bracket strings</span> of length $5$.</li><li> For the third testcase, there are no hyperregular bracket strings of length $8$ for which the substring $[1 \ldots 3]$ is a regular bracket string.</li><li> For the fourth testcase, there $4$ <span class="tex-font-style-it">hyperregular bracket strings</span> are: <span class="tex-font-style-tt">((())(()))</span>, <span class="tex-font-style-tt">((())()())</span>, <span class="tex-font-style-tt">()()((()))</span> and <span class="tex-font-style-tt">()()(()())</span> </li></ul>
