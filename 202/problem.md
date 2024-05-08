## Description

<div><p>Milena has received an array of integers $a_1, a_2, \ldots, a_n$ of length $n$ from a secret admirer. She thinks that making it non-decreasing should help her identify the secret admirer.</p><p>She can use the following operation to make this array non-decreasing:</p><ul> <li> Select an element $a_i$ of array $a$ and an integer $x$ such that $1 \le x &lt; a_i$. Then, replace $a_i$ by two elements $x$ and $a_i - x$ in array $a$. New elements ($x$ and $a_i - x$) are placed in the array $a$ in this order instead of $a_i$.<p>More formally, let $a_1, a_2, \ldots, a_i, \ldots, a_k$ be an array $a$ before the operation. After the operation, it becomes equal to $a_1, a_2, \ldots, a_{i-1}, x, a_i - x, a_{i+1}, \ldots, a_k$. Note that the length of $a$ increases by $1$ on each operation. </p></li></ul><p>Milena can perform this operation multiple times (possibly zero). She wants you to determine the minimum number of times she should perform this operation to make array $a$ non-decreasing.</p><p>An array $x_1, x_2, \ldots, x_k$ of length $k$ is called non-decreasing if $x_i \le x_{i+1}$ for all $1 \le i &lt; k$.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \leq t \leq 10\,000$). The description of test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1\leq n\leq 2\cdot 10^5$)&nbsp;— the length of the array $a$.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1\leq a_i\leq 10^9$)&nbsp;– the array $a$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2\cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output one integer&nbsp;— the minimum number of operations required to make the array non-decreasing.</p><p>It can be shown that it is always possible to make the array $a$ non-decreasing in the finite number of operations.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \leq t \leq 10\,000$). The description of test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1\leq n\leq 2\cdot 10^5$)&nbsp;— the length of the array $a$.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1\leq a_i\leq 10^9$)&nbsp;– the array $a$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2\cdot 10^5$.</p>

## Output

<p>For each test case, output one integer&nbsp;— the minimum number of operations required to make the array non-decreasing.</p><p>It can be shown that it is always possible to make the array $a$ non-decreasing in the finite number of operations.</p>





```input1|2,3,6,7
4
3
1 3 2
4
1 2 3 4
3
3 2 1
7
1 4 4 3 5 7 6
```




```output1
1
0
3
9
```



## Note

<p>In the first test case, Milena can replace the second element of array $a$ by integers $1$ and $2$, so the array would become $[\, 1, \, \underline{1}, \, \underline{2}, \, 2 \,]$. Only $1$ operation is required.</p><p>In the second test case, the array $a$ is already non-decreasing, so the answer is $0$.</p><p>In the third test case, Milena can make array $a$ non-decreasing in $3$ operations as follows. </p><ul> <li> Select $i=1$ and $x=2$ and replace $a_1$ by $2$ and $1$. The array $a$ becomes equal to $[\, \underline{2}, \, \underline{1}, \, 2, \, 1 \, ]$. </li><li> Select $i=3$ and $x=1$ and replace $a_3$ by $1$ and $1$. The array $a$ becomes equal to $[\, 2, \, 1, \, \underline{1}, \, \underline{1}, \, 1 \,]$. </li><li> Select $i=1$ and $x=1$ and replace $a_1$ by $2$ and $1$. The array $a$ becomes equal to $[\, \underline{1}, \, \underline{1}, \, 1, \, 1, \, 1, \, 1 \,]$. </li></ul><p>It can be shown that it is impossible to make it non-decreasing in $2$ or less operations, so the answer is $3$.</p>
