## Description

<div><p>A certain number $1 \le x \le 10^9$ is chosen. You are given two integers $a$ and $b$, which are the two largest divisors of the number $x$. At the same time, the condition $1 \le a &lt; b &lt; x$ is satisfied.</p><p>For the given numbers $a$, $b$, you need to find the value of $x$.</p><p>$^{\dagger}$ The number $y$ is a divisor of the number $x$ if there is an integer $k$ such that $x = y \cdot k$.</p></div><div class="input-specification"><p>Each test consists of several test cases. The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. Then follows the description of the test cases.</p><p>The only line of each test cases contains two integers $a$, $b$ ($1 \le a &lt; b \le 10^9$).</p><p>It is guaranteed that $a$, $b$ are the two largest divisors for some number $1 \le x \le 10^9$.</p></div><div class="output-specification"><p>For each test case, output the number $x$, such that $a$ and $b$ are the two largest divisors of the number $x$.</p><p>If there are several answers, print any of them.</p></div>

## Input

<p>Each test consists of several test cases. The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. Then follows the description of the test cases.</p><p>The only line of each test cases contains two integers $a$, $b$ ($1 \le a &lt; b \le 10^9$).</p><p>It is guaranteed that $a$, $b$ are the two largest divisors for some number $1 \le x \le 10^9$.</p>

## Output

<p>For each test case, output the number $x$, such that $a$ and $b$ are the two largest divisors of the number $x$.</p><p>If there are several answers, print any of them.</p>





```input1|2,4,6,8
8
2 3
1 2
3 11
1 5
5 10
4 6
3 9
250000000 500000000
```




```output1
6
4
33
25
20
12
27
1000000000
```



## Note

<p>For the first test case, all divisors less than $6$ are equal to $[1, 2, 3]$, among them the two largest will be $2$ and $3$.</p><p>For the third test case, all divisors less than $33$ are equal to $[1, 3, 11]$, among them the two largest will be $3$ and $11$.</p><p>For the fifth test case, all divisors less than $20$ are equal to $[1, 2, 4, 5, 10]$, among them the two largest will be $5$ and $10$.</p><p>For the sixth test case, all divisors less than $12$ are equal to $[1, 2, 3, 4, 6]$, among them the two largest will be $4$ and $6$.</p>
