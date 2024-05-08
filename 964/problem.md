## Description

<div><p>You are given an integer $k$. Find the largest integer $x$, where $1 \le x &lt; k$, such that $x! + (x - 1)!^\dagger$ is a multiple of $^\ddagger$ $k$, or determine that no such $x$ exists.</p><p>$^\dagger$ $y!$ denotes the factorial of $y$, which is defined recursively as $y! = y \cdot (y-1)!$ for $y \geq 1$ with the base case of $0! = 1$. For example, $5! = 5 \cdot 4 \cdot 3 \cdot 2 \cdot 1 \cdot 0! = 120$.</p><p>$^\ddagger$ If $a$ and $b$ are integers, then $a$ is a multiple of $b$ if there exists an integer $c$ such that $a = b \cdot c$. For example, $10$ is a multiple of $5$ but $9$ is not a multiple of $6$.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. The description of test cases follows.</p><p>The only line of each test case contains a single integer $k$ ($2 \le k \le 10^9$).</p></div><div class="output-specification"><p>For each test case output a single integer&nbsp;— the largest possible integer $x$ that satisfies the conditions above. </p><p>If no such $x$ exists, output $-1$.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. The description of test cases follows.</p><p>The only line of each test case contains a single integer $k$ ($2 \le k \le 10^9$).</p>

## Output

<p>For each test case output a single integer&nbsp;— the largest possible integer $x$ that satisfies the conditions above. </p><p>If no such $x$ exists, output $-1$.</p>





```input1|2,4
4
3
6
8
10
```




```output1
2
5
7
9
```



## Note

<p>In the first test case, $2! + 1! = 2 + 1 = 3$, which is a multiple of $3$.</p><p>In the third test case, $7! + 6! = 5040 + 720 = 5760$, which is a multiple of $8$.</p>
