## Description

<div><p>Sasha decided to give his girlfriend an array $a_1, a_2, \ldots, a_n$. He found out that his girlfriend evaluates the <span class="tex-font-style-it">beauty</span> of the array as the sum of the values $(a_i - a_{i - 1})$ for all integers $i$ from $2$ to $n$.</p><p>Help Sasha and tell him the maximum beauty of the array $a$ that he can obtain, if he can rearrange its elements in any way.</p></div><div class="input-specification"><p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 500$) — the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2 \leq n \leq 100$) — the length of the array $a$.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \leq a_i \leq 10^9$) — the elements of the array $a$.</p></div><div class="output-specification"><p>For each test case, output a single integer — the maximum beauty of the array $a$ that can be obtained.</p></div>

## Input

<p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 500$) — the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2 \leq n \leq 100$) — the length of the array $a$.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \leq a_i \leq 10^9$) — the elements of the array $a$.</p>

## Output

<p>For each test case, output a single integer — the maximum beauty of the array $a$ that can be obtained.</p>





```input1|2,3,6,7,10,11
5
3
2 1 3
3
69 69 69
5
100 54 80 43 90
4
3 4 3 3
2
2 1
```




```output1
2
0
57
1
1
```



## Note

<p>In the first test case, the elements of the array $a$ can be rearranged to make $a = [1, 2, 3]$. Then its beauty will be equal to $(a_2 - a_1) + (a_3 - a_2) = (2 - 1) + (3 - 2) = 2$.</p><p>In the second test case, there is no need to rearrange the elements of the array $a$. Then its beauty will be equal to $0$.</p>
