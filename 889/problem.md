## Description

<div><p>Baltic, a famous chess player who is also a mathematician, has an array $a_1,a_2, \ldots, a_n$, and he can perform the following operation several (possibly $0$) times:</p><ul> <li> Choose some index $i$ ($1 \leq i \leq n$); </li><li> multiply $a_i$ with $-1$, that is, set $a_i := -a_i$. </li></ul><p>Baltic's favorite number is $m$, and he wants $a_1 + a_2 + \cdots + a_m$ to be the smallest of all non-empty prefix sums. More formally, for each $k = 1,2,\ldots, n$ it should hold that $$a_1 + a_2 + \cdots + a_k \geq a_1 + a_2 + \cdots + a_m.$$</p><p>Please note that multiple smallest prefix sums may exist and that it is only required that $a_1 + a_2 + \cdots + a_m$ is one of them.</p><p>Help Baltic find the minimum number of operations required to make $a_1 + a_2 + \cdots + a_m$ the least of all prefix sums. It can be shown that a valid sequence of operations always exists.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \leq t \leq 10\,000$). The description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $m$ ($1 \leq m \leq n \leq 2\cdot 10^5$)&nbsp;— the size of Baltic's array and his favorite number.</p><p>The second line contains $n$ integers $a_1,a_2, \ldots, a_n$ ($-10^9 \leq a_i \leq 10^9$)&nbsp;— the array.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2\cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, print a single integer&nbsp;— the minimum number of required operations.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \leq t \leq 10\,000$). The description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $m$ ($1 \leq m \leq n \leq 2\cdot 10^5$)&nbsp;— the size of Baltic's array and his favorite number.</p><p>The second line contains $n$ integers $a_1,a_2, \ldots, a_n$ ($-10^9 \leq a_i \leq 10^9$)&nbsp;— the array.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2\cdot 10^5$.</p>

## Output

<p>For each test case, print a single integer&nbsp;— the minimum number of required operations.</p>





```input1|2,3,6,7,10,11
6
4 3
-1 -2 -3 -4
4 3
1 2 3 4
1 1
1
5 5
-2 3 -5 1 -20
5 2
-2 3 -5 -5 -20
10 4
345875723 -48 384678321 -375635768 -35867853 -35863586 -358683842 -81725678 38576 -357865873
```




```output1
1
1
0
0
3
4
```



## Note

<p>In the first example, we perform the operation $a_4 := -a_4$. The array becomes $[-1,-2,-3,4]$ and the prefix sums, $[a_1, \ a_1+a_2, \ a_1+a_2+a_3, \ a_1+a_2+a_3+a_4]$, are equal to $[-1,-3,-6,-2]$. Thus $a_1 + a_2 + a_3=-6$ is the smallest of all prefix sums.</p><p>In the second example, we perform the operation $a_3 := -a_3$. The array becomes $[1,2,-3,4]$ with prefix sums equal to $[1,3,0,4]$.</p><p>In the third and fourth examples, $a_1 + a_2 + \cdots + a_m$ is already the smallest of the prefix sums&nbsp;— no operation needs to be performed.</p><p>In the fifth example, a valid sequence of operations is:</p><ul> <li> $a_3 := -a_3$, </li><li> $a_2 := -a_2$, </li><li> $a_5 := -a_5$. </li></ul><p>The array becomes $[-2,-3,5,-5,20]$ and its prefix sums are $[-2,-5,0,-5,15]$. Note that $a_1+a_2=-5$ and $a_1+a_2+a_3+a_4=-5$ are both the smallest of the prefix sums (and this is a valid solution).</p>
