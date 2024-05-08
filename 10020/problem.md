## Description

<div><p>You are given three <span class="tex-font-style-bf">positive</span> integers $a$, $b$ and $l$ ($a,b,l&gt;0$). </p><p>It can be shown that there always exists a way to choose <span class="tex-font-style-bf">non-negative</span> (i.e. $\ge 0$) integers $k$, $x$, and $y$ such that $l = k \cdot a^x \cdot b^y$. </p><p>Your task is to find the number of distinct possible values of $k$ across all such ways.</p></div><div class="input-specification"><p>The first line contains the integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The following $t$ lines contain three integers, $a$, $b$ and $l$ ($2 \le a, b \le 100$, $1 \le l \le 10^6$)&nbsp;— description of a test case.</p></div><div class="output-specification"><p>Output $t$ lines, with the $i$-th ($1 \le i \le t$) line containing an integer, the answer to the $i$-th test case.</p></div>

## Input

<p>The first line contains the integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The following $t$ lines contain three integers, $a$, $b$ and $l$ ($2 \le a, b \le 100$, $1 \le l \le 10^6$)&nbsp;— description of a test case.</p>

## Output

<p>Output $t$ lines, with the $i$-th ($1 \le i \le t$) line containing an integer, the answer to the $i$-th test case.</p>





```input1|2,4,6,8,10,12
11
2 5 20
2 5 21
4 6 48
2 3 72
3 5 75
2 2 1024
3 7 83349
100 100 1000000
7 3 2
2 6 6
17 3 632043
```




```output1
6
1
5
12
6
11
24
4
1
3
24
```



## Note

<p>In the first test case, $a=2, b=5, l=20$. The possible values of $k$ (and corresponding $x,y$) are as follows: </p><ul> <li> Choose $k = 1, x = 2, y = 1$. Then $k \cdot a^x \cdot b^y = 1 \cdot 2^2 \cdot 5^1 = 20 = l$. </li><li> Choose $k = 2, x = 1, y = 1$. Then $k \cdot a^x \cdot b^y = 2 \cdot 2^1 \cdot 5^1 = 20 = l$. </li><li> Choose $k = 4, x = 0, y = 1$. Then $k \cdot a^x \cdot b^y = 4 \cdot 2^0 \cdot 5^1 = 20 = l$. </li><li> Choose $k = 5, x = 2, y = 0$. Then $k \cdot a^x \cdot b^y = 5 \cdot 2^2 \cdot 5^0 = 20 = l$. </li><li> Choose $k = 10, x = 1, y = 0$. Then $k \cdot a^x \cdot b^y = 10 \cdot 2^1 \cdot 5^0 = 20 = l$. </li><li> Choose $k = 20, x = 0, y = 0$. Then $k \cdot a^x \cdot b^y = 20 \cdot 2^0 \cdot 5^0 = 20 = l$. </li></ul><p>In the second test case, $a=2, b=5, l=21$. Note that $l = 21$ is not divisible by either $a = 2$ or $b = 5$. Therefore, we can only set $x = 0, y = 0$, which corresponds to $k = 21$.</p><p>In the third test case, $a=4, b=6, l=48$. The possible values of $k$ (and corresponding $x,y$) are as follows: </p><ul> <li> Choose $k = 2, x = 1, y = 1$. Then $k \cdot a^x \cdot b^y = 2 \cdot 4^1 \cdot 6^1 = 48 = l$. </li><li> Choose $k = 3, x = 2, y = 0$. Then $k \cdot a^x \cdot b^y = 3 \cdot 4^2 \cdot 6^0 = 48 = l$. </li><li> Choose $k = 8, x = 0, y = 1$. Then $k \cdot a^x \cdot b^y = 8 \cdot 4^0 \cdot 6^1 = 48 = l$. </li><li> Choose $k = 12, x = 1, y = 0$. Then $k \cdot a^x \cdot b^y = 12 \cdot 4^1 \cdot 6^0 = 48 = l$. </li><li> Choose $k = 48, x = 0, y = 0$. Then $k \cdot a^x \cdot b^y = 48 \cdot 4^0 \cdot 6^0 = 48 = l$. </li></ul>
