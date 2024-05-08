## Description

<div><p>You are given two arrays $a$ and $b$ of size $n$ along with a fixed integer $v$.</p><p>An interval $[l, r]$ is called a <span class="tex-font-style-bf">good</span> interval if $(b_l \mid b_{l+1} \mid \ldots \mid b_r) \ge v$, where $|$ denotes the <a href="https://en.wikipedia.org/wiki/Bitwise_operation#OR">bitwise OR operation</a>. The <span class="tex-font-style-bf">beauty</span> of a good interval is defined as $\max(a_l, a_{l+1}, \ldots, a_r)$.</p><p>You are given $q$ queries of two types:</p><ul> <li> "<span class="tex-font-style-tt">1 i x</span>": assign $b_i := x$; </li><li> "<span class="tex-font-style-tt">2 l r</span>": find the <span class="tex-font-style-bf">minimum</span> beauty among all <span class="tex-font-style-bf">good</span> intervals $[l_0,r_0]$ satisfying $l \le l_0 \le r_0 \le r$. If there is no suitable good interval, output $-1$ instead. </li></ul><p>Please process all queries.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^5$). The description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $v$ ($1 \le n \le 2 \cdot 10^5$, $1 \le v \le 10^9$).</p><p>The second line of each testcase contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le 10^9$).</p><p>The third line of each testcase contains $n$ integers $b_1, b_2, \ldots, b_n$ ($1 \le b_i \le 10^9$).</p><p>The fourth line of each testcase contains one integer $q$ ($1 \le q \le 2 \cdot 10^5$).</p><p>The $i$-th of the following $q$ lines contains the description of queries. Each line is of one of two types:</p><ul> <li> "<span class="tex-font-style-tt">1 i x</span>" ($1 \le i \le n$, $1 \le x \le 10^9)$; </li><li> "<span class="tex-font-style-tt">2 l r</span>" ($1 \le l \le r \le n$). </li></ul><p>It is guaranteed that both the sum of $n$ and the sum of $q$ over all test cases do not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output the answers for all queries of the second type.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^5$). The description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $v$ ($1 \le n \le 2 \cdot 10^5$, $1 \le v \le 10^9$).</p><p>The second line of each testcase contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le 10^9$).</p><p>The third line of each testcase contains $n$ integers $b_1, b_2, \ldots, b_n$ ($1 \le b_i \le 10^9$).</p><p>The fourth line of each testcase contains one integer $q$ ($1 \le q \le 2 \cdot 10^5$).</p><p>The $i$-th of the following $q$ lines contains the description of queries. Each line is of one of two types:</p><ul> <li> "<span class="tex-font-style-tt">1 i x</span>" ($1 \le i \le n$, $1 \le x \le 10^9)$; </li><li> "<span class="tex-font-style-tt">2 l r</span>" ($1 \le l \le r \le n$). </li></ul><p>It is guaranteed that both the sum of $n$ and the sum of $q$ over all test cases do not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output the answers for all queries of the second type.</p>





```input1|2,3,4,5,6,7,8,9,20,21,22,23,24
3
3 7
2 1 3
2 2 3
4
2 1 3
1 2 5
2 2 3
2 1 3
4 5
5 1 2 4
4 2 3 3
6
2 1 4
1 3 15
2 3 4
2 2 4
1 2 13
2 1 4
1 5
6
4
1
2 1 1
```




```output1
-1 3 2 
5 2 2 1 
-1
```



## Note

<p>In the first test case, $a = [2, 1, 3]$, $b = [2, 2, 3]$, and $v = 7$.</p><p>The first query is of the second type and has $l = 1$ and $r = 3$. The largest interval available is $[1, 3]$, and its bitwise OR is $b_1 \mid b_2 \mid b_3 = 3$ which is less than $v$. Thus, no good interval exists.</p><p>The second query asks to change $b_2$ to $5$, so $b$ becomes $[2, 5, 3]$.</p><p>The third query is of the second type and has $l = 2$ and $r = 3$. There are three possible intervals: $[2, 2]$, $[3, 3]$, and $[2, 3]$. However, $b_2 = 5 &lt; v$, $b_3 = 3 &lt; v$. So only the last interval is good: it has $b_2 \mid b_3 = 7$. The answer is thus $\max(a_2, a_3) = 3$.</p><p>The fourth query is of the second type and has $l = 1$ and $r = 3$. There are three good intervals: $[1, 2]$, $[2, 3]$, and $[1, 3]$. Their beauty is $2$, $3$, $3$ correspondingly. The answer is thus $2$.</p><p>In the second test case, $a = [5, 1, 2, 4]$, $b = [4, 2, 3, 3]$, and $v = 5$.</p><p>The first query has $l = 1$ and $r = 4$. The only good intervals are: $[1, 2]$, $[1, 3]$, $[1, 4]$. Their beauty is $5$, $5$, $5$ correspondingly. The answer is thus $5$.</p>
