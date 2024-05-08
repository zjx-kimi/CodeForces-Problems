## Description

<div><p>You are given two arrays $a_1, a_2, \ldots, a_n$ and $b_1, b_2, \ldots, b_n$.</p><p>In one operation, you can choose any integer $i$ from $1$ to $n$ and swap the numbers $a_i$ and $b_i$.</p><p>Determine whether, after using any (possibly zero) number of operations, the following two conditions can be satisfied simultaneously:</p><ul> <li> $a_n = \max(a_1, a_2, \ldots, a_n)$, </li><li> $b_n = \max(b_1, b_2, \ldots, b_n)$. </li></ul><p>Here $\max(c_1, c_2, \ldots, c_k)$ denotes the maximum number among $c_1, c_2, \ldots, c_k$. For example, $\max(3, 5, 4) = 5$, $\max(1, 7, 7) = 7$, $\max(6, 2) = 6$.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 200$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 100$)&nbsp;— the length of the arrays.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le 100$)&nbsp;— elements of the first array.</p><p>The third line of each test case contains $n$ integers $b_1, b_2, \ldots, b_n$ ($1 \le b_i \le 100$)&nbsp;— elements of the second array.</p></div><div class="output-specification"><p>For each test case, print "<span class="tex-font-style-tt">Yes</span>" if after using any (possibly zero) number of operations the conditions described above are satisfied. Otherwise, print "<span class="tex-font-style-tt">No</span>".</p><p>You can output the answer in any case (upper or lower). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as positive responses.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 200$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 100$)&nbsp;— the length of the arrays.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le 100$)&nbsp;— elements of the first array.</p><p>The third line of each test case contains $n$ integers $b_1, b_2, \ldots, b_n$ ($1 \le b_i \le 100$)&nbsp;— elements of the second array.</p>

## Output

<p>For each test case, print "<span class="tex-font-style-tt">Yes</span>" if after using any (possibly zero) number of operations the conditions described above are satisfied. Otherwise, print "<span class="tex-font-style-tt">No</span>".</p><p>You can output the answer in any case (upper or lower). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as positive responses.</p>





```input1|2,3,4,8,9,10,14,15,16,20,21,22
7
3
7 9 7
7 6 9
4
10 10 15 15
10 16 15 15
2
100 99
99 100
1
1
1
9
1 2 3 4 5 6 7 8 9
9 9 9 9 9 9 6 6 6
7
1 1 2 2 1 1 2
1 2 1 2 1 2 1
2
30 4
5 30
```




```output1
Yes
No
Yes
Yes
Yes
No
No
```



## Note

<p>In the first test case, you can swap the numbers $a_3$ and $b_3$, after which the array $a$ becomes equal to $[7, 9, 9]$, and the array $b$ becomes equal to $[7, 6, 7]$, and both conditions are met.</p><p>In the second test case, it can be proved that it is impossible to satisfy both conditions.</p><p>In the third test case, you can swap the numbers $a_1$ and $b_1$, after which the array $a$ becomes equal to $[99, 99]$, and the array $b$ becomes equal to $[100, 100]$, and both conditions are satisfied.</p><p>In fifth test case, you can swap $a_7$ and $b_7$, $a_8$ and $b_8$, $a_9$ and $b_9$, after which the array $a$ becomes equal to $[1, 2, 3, 4, 5, 6, 6, 6, 6]$, and the array $b$ becomes equal to $[9, 9, 9, 9, 9, 9, 7, 8, 9]$, and both conditions are satisfied.</p>
