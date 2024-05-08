## Description

<div><p>You are given a sequence $a_{1}, a_{2}, \ldots, a_{n}$. A sequence $b_{1}, b_{2}, \ldots, b_{n}$ is called <span class="tex-font-style-it">good</span>, if it satisfies all of the following conditions: </p><ul> <li> $b_{i}$ is a positive integer for $i = 1, 2, \ldots, n$; </li><li> $b_{i} \neq a_{i}$ for $i = 1, 2, \ldots, n$; </li><li> $b_{1} &lt; b_{2} &lt; \ldots &lt; b_{n}$. </li></ul> Find the minimum value of $b_{n}$ among all good sequences $b_{1}, b_{2}, \ldots, b_{n}$.</div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 100$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 100$).</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le 10^{9}$).</p></div><div class="output-specification"><p>For each test case, print a single integer&nbsp;— the minimum value of $b_{n}$ among all good sequences $b$.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 100$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 100$).</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le 10^{9}$).</p>

## Output

<p>For each test case, print a single integer&nbsp;— the minimum value of $b_{n}$ among all good sequences $b$.</p>





```input1|2,3,6,7
3
5
1 3 2 6 7
4
2 3 4 5
1
1
```




```output1
8
4
2
```



## Note

<p>In the first test case, $b = [2, 4, 5, 7, 8]$ is a good sequence. It can be proved that there is no good $b$ with $b_{5} &lt; 8$.</p><p>In the second test case, $b = [1, 2, 3, 4]$ is an optimal good sequence.</p><p>In the third test case, $b = [2]$ is an optimal good sequence.</p>
