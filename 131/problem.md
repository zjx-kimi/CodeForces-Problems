## Description

<div><div class="epigraph"><div class="epigraph-text"><span class="tex-font-style-it"><a href="https://soundcloud.com/lux-gg-198448038/desert-ruins">eliteLAQ - Desert Ruins</a></span></div><div class="epigraph-source">⠀</div></div><p>There are $n$ positive integers $a_1, a_2, \dots, a_n$ on a blackboard. You are also given a positive integer $k$. You can perform the following operation some (possibly $0$) times:</p><ul> <li> choose a number $x$ on the blackboard; </li><li> erase one occurrence of $x$; </li><li> write two <span class="tex-font-style-bf">positive</span> integers $y$, $z$ such that $y+z = x+k$ on the blackboard. </li></ul><p>Is it possible to make all the numbers on the blackboard equal? If yes, what is the minimum number of operations you need?</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^4$). The description of the test cases follows.</p><p>The first line of each test case contains two integers $n$, $k$ ($1 \le n \le 2 \cdot 10^5$, $1 \leq k \leq 10^{12}$)&nbsp;— the number of integers initially on the blackboard and the constant $k$.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le 10^{12}$)&nbsp;— the initial state of the blackboard.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output a single line containing an integer: the minimum number of operations you need to make all the numbers on the blackboard equal, or $-1$ if it is impossible.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^4$). The description of the test cases follows.</p><p>The first line of each test case contains two integers $n$, $k$ ($1 \le n \le 2 \cdot 10^5$, $1 \leq k \leq 10^{12}$)&nbsp;— the number of integers initially on the blackboard and the constant $k$.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le 10^{12}$)&nbsp;— the initial state of the blackboard.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output a single line containing an integer: the minimum number of operations you need to make all the numbers on the blackboard equal, or $-1$ if it is impossible.</p>





```input1|2,3,6,7,10,11,14,15,18,19
9
2 1
3 4
2 3
7 11
3 10
100 40 100
2 1
1 2
2 2
1 2
1 327869541
327869541
5 26250314066
439986238782 581370817372 409476934981 287439719777 737637983182
5 616753575719
321037808624 222034505841 214063039282 441536506916 464097941819
5 431813672576
393004301966 405902283416 900951084746 672201172466 518769038906
```




```output1
3
1
4
-1
-1
0
3119
28999960732
-1
```



## Note

<p>In the first test case, $k = 1$. You can make all the numbers on the blackboard equal to $2$ with the following operations: </p><ul> <li> Erase $x = 4$ and write $(y, z) = (2, 3)$. Note that $y+z=x+k$. The blackboard now contains the multiset $\{3, 2, 3\}$. </li><li> Erase $x = 3$ and write $(y, z) = (2, 2)$. Note that $y+z=x+k$. The blackboard now contains $\{2, 2, 2, 3\}$. </li><li> Erase $x = 3$ and write $(y, z) = (2, 2)$. Note that $y+z=x+k$. The blackboard now contains $\{2, 2, 2, 2, 2\}$. </li></ul><p>This makes all the numbers equal in $3$ operations. It can be shown that you cannot make all the numbers equal in less than $3$ operations.</p><p>In the second test case, $k = 3$. You can make all the numbers on the blackboard equal to $7$ with the following operation: </p><ul> <li> Erase $x = 11$ and write $(y, z) = (7, 7)$. Note that $y+z=x+k$. The blackboard now contains $\{7, 7, 7\}$. </li></ul><p>In the third test case, $k = 10$. You can make all the numbers on the blackboard equal to $40$ with the following operations: </p><ul> <li> Erase $x = 100$ and write $(y, z) = (70, 40)$. Note that $y+z=x+k$. The blackboard now contains $\{70, 40, 40, 100\}$. </li><li> Erase $x = 70$ and write $(y, z) = (40, 40)$. Note that $y+z=x+k$. The blackboard now contains $\{40, 40, 40, 40, 100\}$. </li><li> Erase $x = 100$ and write $(y, z) = (40, 70)$. Note that $y+z=x+k$. The blackboard now contains $\{40, 40, 40, 40, 40, 70\}$. </li><li> Erase $x = 70$ and write $(y, z) = (40, 40)$. Note that $y+z=x+k$. The blackboard now contains $\{40, 40, 40, 40, 40, 40, 40\}$. </li></ul><p>In the fourth and in the fifth test case, you can show that it is impossible to make all the numbers on the blackboard equal.</p>
