## Description

<div><p>Given an array $a$ of length $n$, which elements are equal to $-1$ and $1$. Let's call the array $a$ <span class="tex-font-style-it">good</span> if the following conditions are held at the same time:</p><ul> <li> $a_1 + a_2 + \ldots + a_n \ge 0$;<p> </p></li><li> $a_1 \cdot a_2 \cdot \ldots \cdot a_n = 1$. </li></ul><p>In one operation, you can select an arbitrary element of the array $a_i$ and change its value to the opposite. In other words, if $a_i = -1$, you can assign the value to $a_i := 1$, and if $a_i = 1$, then assign the value to $a_i := -1$.</p><p>Determine the minimum number of operations you need to perform to make the array $a$ good. It can be shown that this is always possible.</p></div><div class="input-specification"><p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 500$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 100$) — the length of the array $a$.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($a_i = \pm 1$) — the elements of the array $a$.</p></div><div class="output-specification"><p>For each test case, output a single integer — the minimum number of operations that need to be done to make the $a$ array good.</p></div>

## Input

<p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 500$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 100$) — the length of the array $a$.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($a_i = \pm 1$) — the elements of the array $a$.</p>

## Output

<p>For each test case, output a single integer — the minimum number of operations that need to be done to make the $a$ array good.</p>





```input1|2,3,6,7,10,11,14,15
7
4
-1 -1 1 -1
5
-1 -1 -1 1 1
4
-1 1 -1 1
3
-1 -1 -1
5
1 1 1 1 1
1
-1
2
-1 -1
```




```output1
1
1
0
3
0
1
2
```



## Note

<p>In the first test case, we can assign the value $a_1 := 1$. Then $a_1 + a_2 + a_3 + a_4 = 1 + (-1) + 1 + (-1) = 0 \ge 0$ and $a_1 \cdot a_2 \cdot a_3 \cdot a_4 = 1 \cdot (-1) \cdot 1 \cdot (-1) = 1$. Thus, we performed $1$ operation.</p><p>In the second test case, we can assign $a_1 := 1$. Then $a_1 + a_2 + a_3 + a_4 + a_5 = 1 + (-1) + (-1) + 1 + 1 = 1 \ge 0$ and $a_1 \cdot a_2 \cdot a_3 \cdot a_4 \cdot a_5 = 1 \cdot (-1) \cdot (-1) \cdot 1 \cdot 1 = 1$. Thus, we performed $1$ operation.</p><p>In the third test case, $a_1 + a_2 + a_3 + a_4 = (-1) + 1 + (-1) + 1 = 0 \ge 0$ and $a_1 \cdot a_2 \cdot a_3 \cdot a_4 = (-1) \cdot 1 \cdot (-1) \cdot 1 = 1$. Thus, all conditions are already satisfied and no operations are needed.</p><p>In the fourth test case, we can assign the values $a_1 := 1, a_2 := 1, a_3 := 1$. Then $a_1 + a_2 + a_3 = 1 + 1 + 1 = 3 \ge 0$ and $a_1 \cdot a_2 \cdot a_3 = 1 \cdot 1 \cdot 1 = 1$. Thus, we performed $3$ operations.</p>
