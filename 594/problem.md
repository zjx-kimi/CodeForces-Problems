## Description

<div><p>You are given a positive integer $n$. Please find an array $a_1, a_2, \ldots, a_n$ that is perfect.</p><p>A perfect array $a_1, a_2, \ldots, a_n$ satisfies the following criteria: </p><ul> <li> $1 \le a_i \le 1000$ for all $1 \le i \le n$. </li><li> $a_i$ is divisible by $i$ for all $1 \le i \le n$. </li><li> $a_1 + a_2 + \ldots + a_n$ is divisible by $n$. </li></ul></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 200$). The description of the test cases follows.</p><p>The only line of each test case contains a single positive integer $n$ ($1 \le n \le 200$)&nbsp;— the length of the array $a$.</p></div><div class="output-specification"><p>For each test case, output an array $a_1, a_2, \ldots, a_n$ that is perfect.</p><p>We can show that an answer always exists. If there are multiple solutions, print any.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 200$). The description of the test cases follows.</p><p>The only line of each test case contains a single positive integer $n$ ($1 \le n \le 200$)&nbsp;— the length of the array $a$.</p>

## Output

<p>For each test case, output an array $a_1, a_2, \ldots, a_n$ that is perfect.</p><p>We can show that an answer always exists. If there are multiple solutions, print any.</p>





```input1|2,4,6,8
7
1
2
3
4
5
6
7
```




```output1
1
2 4
1 2 3
2 8 6 4
3 4 9 4 5
1 10 18 8 5 36
3 6 21 24 10 6 14
```



## Note

<p>In the third test case: </p><ul> <li> $a_1 = 1$ is divisible by $1$. </li><li> $a_2 = 2$ is divisible by $2$. </li><li> $a_3 = 3$ is divisible by $3$. </li><li> $a_1 + a_2 + a_3 = 1 + 2 + 3 = 6$ is divisible by $3$. </li></ul><p>In the fifth test case: </p><ul> <li> $a_1 = 3$ is divisible by $1$. </li><li> $a_2 = 4$ is divisible by $2$. </li><li> $a_3 = 9$ is divisible by $3$. </li><li> $a_4 = 4$ is divisible by $4$. </li><li> $a_5 = 5$ is divisible by $5$. </li><li> $a_1 + a_2 + a_3 + a_4 + a_5 = 3 + 4 + 9 + 4 + 5 = 25$ is divisible by $5$. </li></ul>
