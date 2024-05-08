## Description

<div><p>You are given three integers $x$, $y$, and $n$.</p><p>Your task is to construct an array $a$ consisting of $n$ integers which satisfies the following conditions:</p><ol> <li> $a_1=x$, $a_n=y$; </li><li> $a$ is <span class="tex-font-style-bf">strictly</span> increasing (i.e. $a_1 &lt; a_2 &lt; \ldots &lt; a_n$); </li><li> if we denote $b_i=a_{i+1}-a_{i}$ for $1 \leq i \leq n-1$, then $b$ is <span class="tex-font-style-bf">strictly</span> decreasing (i.e. $b_1 &gt; b_2 &gt; \ldots &gt; b_{n-1}$). </li></ol><p>If there is no such array $a$, print a single integer $-1$.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 1000$). The description of the test cases follows.</p><p>The only line of each test case contains three integers $x$, $y$, $n$ ($1 \le x &lt; y \le 1000,3 \le n \le 1000$).</p></div><div class="output-specification"><p>For each test case, output $n$ integers $a_1,a_2,\ldots,a_n$. If there are multiple solutions, print any of them.</p><p>If there is no solution, print a single integer $-1$.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 1000$). The description of the test cases follows.</p><p>The only line of each test case contains three integers $x$, $y$, $n$ ($1 \le x &lt; y \le 1000,3 \le n \le 1000$).</p>

## Output

<p>For each test case, output $n$ integers $a_1,a_2,\ldots,a_n$. If there are multiple solutions, print any of them.</p><p>If there is no solution, print a single integer $-1$.</p>





```input1|2,4
3
1 4 3
1 3 3
100 200 4
```




```output1
1 3 4
-1
100 150 180 200
```



## Note

<p>In the first test case, $a=[1,3,4]$, which is strictly increasing. Next, $b_1=a_2-a_1=3-1=2$, $b_2=a_3-a_2=4-3=1$, thus $b=[2,1]$, which is strictly decreasing.</p><p>In the second test case, there is no array $a$ that satisfies all the conditions above.</p>
