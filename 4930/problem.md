## Description

<div><p>You are given an integer $n$, which you want to obtain. You have an unlimited supply of every integer from $1$ to $k$, except integer $x$ (there are no integer $x$ at all).</p><p>You are allowed to take an arbitrary amount of each of these integers (possibly, zero). Can you make the sum of taken integers equal to $n$?</p><p>If there are multiple answers, print any of them.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 100$)&nbsp;— the number of testcases.</p><p>The only line of each testcase contains three integers $n, k$ and $x$ ($1 \le x \le k \le n \le 100$).</p></div><div class="output-specification"><p>For each test case, in the first line, print "<span class="tex-font-style-tt">YES</span>" or "<span class="tex-font-style-tt">NO</span>"&nbsp;— whether you can take an arbitrary amount of each integer from $1$ to $k$, except integer $x$, so that their sum is equal to $n$.</p><p>If you can, the second line should contain a single integer $m$&nbsp;— the total amount of taken integers. The third line should contain $m$ integers&nbsp;— each of them from $1$ to $k$, not equal to $x$, and their sum is $n$.</p><p>If there are multiple answers, print any of them.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 100$)&nbsp;— the number of testcases.</p><p>The only line of each testcase contains three integers $n, k$ and $x$ ($1 \le x \le k \le n \le 100$).</p>

## Output

<p>For each test case, in the first line, print "<span class="tex-font-style-tt">YES</span>" or "<span class="tex-font-style-tt">NO</span>"&nbsp;— whether you can take an arbitrary amount of each integer from $1$ to $k$, except integer $x$, so that their sum is equal to $n$.</p><p>If you can, the second line should contain a single integer $m$&nbsp;— the total amount of taken integers. The third line should contain $m$ integers&nbsp;— each of them from $1$ to $k$, not equal to $x$, and their sum is $n$.</p><p>If there are multiple answers, print any of them.</p>





```input1|2,4,6
5
10 3 2
5 2 1
4 2 1
7 7 3
6 1 1
```




```output1
YES
6
3 1 1 1 1 3
NO
YES
2
2 2
YES
1
7
NO
```



## Note

<p>Another possible answer for the first testcase is $[3, 3, 3, 1]$. Note that you don't have to minimize the amount of taken integers. There also exist other answers.</p><p>In the second testcase, you only have an unlimited supply of integer $2$. There is no way to get sum $5$ using only them.</p><p>In the fifth testcase, there are no integers available at all, so you can't get any positive sum.</p>
