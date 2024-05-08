## Description

<div><p>You are given a string $s$, consisting only of characters '<span class="tex-font-style-tt">0</span>' and/or '<span class="tex-font-style-tt">1</span>'.</p><p>In one operation, you choose a position $i$ from $1$ to $|s| - 1$, where $|s|$ is the current length of string $s$. Then you insert a character between the $i$-th and the $(i+1)$-st characters of $s$. If $s_i = s_{i+1}$, you insert '<span class="tex-font-style-tt">1</span>'. If $s_i \neq s_{i+1}$, you insert '<span class="tex-font-style-tt">0</span>'.</p><p>Is it possible to make the number of zeroes in the string strictly greater than the number of ones, using any number of operations (possibly, none)?</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 100$)&nbsp;— the number of testcases.</p><p>The first line of each testcase contains an integer $n$ ($1 \le n \le 100$).</p><p>The second line contains a string $s$ of length exactly $n$, consisting only of characters '<span class="tex-font-style-tt">0</span>' and/or '<span class="tex-font-style-tt">1</span>'.</p></div><div class="output-specification"><p>For each testcase, print "<span class="tex-font-style-tt">YES</span>" if it's possible to make the number of zeroes in $s$ strictly greater than the number of ones, using any number of operations (possibly, none). Otherwise, print "<span class="tex-font-style-tt">NO</span>".</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 100$)&nbsp;— the number of testcases.</p><p>The first line of each testcase contains an integer $n$ ($1 \le n \le 100$).</p><p>The second line contains a string $s$ of length exactly $n$, consisting only of characters '<span class="tex-font-style-tt">0</span>' and/or '<span class="tex-font-style-tt">1</span>'.</p>

## Output

<p>For each testcase, print "<span class="tex-font-style-tt">YES</span>" if it's possible to make the number of zeroes in $s$ strictly greater than the number of ones, using any number of operations (possibly, none). Otherwise, print "<span class="tex-font-style-tt">NO</span>".</p>





```input1|2,3,6,7
3
2
00
2
11
2
10
```




```output1
YES
NO
YES
```



## Note

<p>In the first testcase, the number of zeroes is already greater than the number of ones.</p><p>In the second testcase, it's impossible to insert any zeroes in the string.</p><p>In the third testcase, you can choose $i = 1$ to insert a zero between the $1$-st and the $2$-nd characters. Since $s_1 \neq s_2$, you insert a '<span class="tex-font-style-tt">0</span>'. The resulting string is "<span class="tex-font-style-tt">100</span>". It has two zeroes and only a single one, so the answer is "<span class="tex-font-style-tt">YES</span>".</p>
