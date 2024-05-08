## Description

<div><p>In Japan, the number $4$ reads like death, so Bob decided to build a <span class="tex-font-style-it">live sequence</span>. <span class="tex-font-style-it">Living sequence</span> $a$ contains all natural numbers that do not contain the digit $4$. $a = [1, 2, 3, 5, 6, 7, 8, 9, 10, 11, 12, 13, 15, 16, \ldots]$.</p><p>For example, the number $1235$ is part of the sequence $a$, but the numbers $4321$, $443$ are not part of the sequence $a$.</p><p>Bob realized that he does not know how to quickly search for a particular number by the position $k$ in the sequence, so he asks for your help.</p><p>For example, if Bob wants to find the number at position $k = 4$ (indexing from $1$), you need to answer $a_k = 5$.</p></div><div class="input-specification"><p>The first line of input data contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>In the only line of each test case, there is a single integer $k$ ($1 \le k \le 10^{12}$)&nbsp;— the position Bob is interested in.</p></div><div class="output-specification"><p>For each test case, print on a separate line the number $a_k$ in indexing with $1$.</p></div>

## Input

<p>The first line of input data contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>In the only line of each test case, there is a single integer $k$ ($1 \le k \le 10^{12}$)&nbsp;— the position Bob is interested in.</p>

## Output

<p>For each test case, print on a separate line the number $a_k$ in indexing with $1$.</p>





```input1|2,4,6,8
7
3
5
22
10
100
12345
827264634912
```




```output1
3
6
25
11
121
18937
2932285320890
```


