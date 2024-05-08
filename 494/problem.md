## Description

<div><p>Monocarp finally got the courage to register on ForceCoders. He came up with a handle but is still thinking about the password.</p><p>He wants his password to be as strong as possible, so he came up with the following criteria: </p><ul> <li> the length of the password should be exactly $m$; </li><li> the password should only consist of digits from $0$ to $9$; </li><li> the password should not appear in the password database (given as a string $s$) as a <span class="tex-font-style-bf">subsequence</span> (not necessarily contiguous). </li></ul><p>Monocarp also came up with two strings of length $m$: $l$ and $r$, both consisting only of digits from $0$ to $9$. He wants the $i$-th digit of his password to be between $l_i$ and $r_i$, inclusive.</p><p>Does there exist a password that fits all criteria?</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of testcases.</p><p>The first line of each testcase contains a string $s$ ($1 \le |s| \le 3 \cdot 10^5$), consisting only of digits from $0$ to $9$&nbsp;— the password database.</p><p>The second line contains a single integer $m$ ($1 \le m \le 10$)&nbsp;— the required length of the password.</p><p>The third line contains a string $l$ ($|l| = m$), consisting only of digits from $0$ to $9$&nbsp;— the lower restriction on each digit.</p><p>The fourth line contains a string $r$ ($|r| = m$), consisting only of digits from $0$ to $9$&nbsp;— the upper restriction on each digit. $l_i \le r_i$ for all $i$ from $1$ to $m$.</p><p>The sum of lengths of $s$ over all testcases doesn't exceed $3 \cdot 10^5$.</p></div><div class="output-specification"><p>For each testcase, print "<span class="tex-font-style-tt">YES</span>" if there exists a password that fits all criteria. Print "<span class="tex-font-style-tt">NO</span>" otherwise.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of testcases.</p><p>The first line of each testcase contains a string $s$ ($1 \le |s| \le 3 \cdot 10^5$), consisting only of digits from $0$ to $9$&nbsp;— the password database.</p><p>The second line contains a single integer $m$ ($1 \le m \le 10$)&nbsp;— the required length of the password.</p><p>The third line contains a string $l$ ($|l| = m$), consisting only of digits from $0$ to $9$&nbsp;— the lower restriction on each digit.</p><p>The fourth line contains a string $r$ ($|r| = m$), consisting only of digits from $0$ to $9$&nbsp;— the upper restriction on each digit. $l_i \le r_i$ for all $i$ from $1$ to $m$.</p><p>The sum of lengths of $s$ over all testcases doesn't exceed $3 \cdot 10^5$.</p>

## Output

<p>For each testcase, print "<span class="tex-font-style-tt">YES</span>" if there exists a password that fits all criteria. Print "<span class="tex-font-style-tt">NO</span>" otherwise.</p>





```input1|2,3,4,5,10,11,12,13,18,19,20,21
5
88005553535123456
2
50
56
123412341234
3
111
444
1234
4
4321
4321
459
2
49
59
00010
2
10
11
```




```output1
YES
NO
YES
NO
YES
```



## Note

<p>In the first testcase, Monocarp can choose password "<span class="tex-font-style-tt">50</span>". It doesn't appear in $s$ as a subsequence.</p><p>In the second testcase, all combinations of three digits, each of them being from $1$ to $4$, fit the criteria on $l$ and $r$. However, all of them appear in $s$ as subsequences. For example, "<span class="tex-font-style-tt">314</span>" appears at positions $[3, 5, 12]$ and "<span class="tex-font-style-tt">222</span>" appears at positions $[2, 6, 10]$.</p><p>In the third testcase, Monocarp can choose password "<span class="tex-font-style-tt">4321</span>". Actually, that is the only password that fits the criteria on $l$ and $r$. Luckily, it doesn't appear in $s$ as a subsequence.</p><p>In the fourth testcase, only "<span class="tex-font-style-tt">49</span>" and "<span class="tex-font-style-tt">59</span>" fit the criteria on $l$ and $r$. Both of them appear in $s$ as subsequences.</p><p>In the fifth testcase, Monocarp can choose password "<span class="tex-font-style-tt">11</span>".</p>
