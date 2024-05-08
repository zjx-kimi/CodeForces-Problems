## Description

<div><p>You are given an array $a$ of length $2n$, consisting of each integer from $1$ to $n$ exactly <span class="tex-font-style-bf">twice</span>.</p><p>You are also given an integer $k$ ($1 \leq k \leq \lfloor \frac{n}{2} \rfloor $).</p><p>You need to find two arrays $l$ and $r$ each of length $\mathbf{2k}$ such that: </p><ul> <li> $l$ is a subset$^\dagger$ of $[a_1, a_2, \ldots a_n]$ </li><li> $r$ is a subset of $[a_{n+1}, a_{n+2}, \ldots a_{2n}]$ </li><li> <a href="https://en.wikipedia.org/wiki/Bitwise_operation#XOR">bitwise XOR</a> of elements of $l$ is equal to the bitwise XOR of elements of $r$; in other words, $l_1 \oplus l_2 \oplus \ldots \oplus l_{2k} = r_1 \oplus r_2 \oplus \ldots \oplus r_{2k}$ </li></ul><p>It can be proved that at least one pair of $l$ and $r$ always exists. If there are multiple solutions, you may output any one of them.</p><p>$^\dagger$ A sequence $x$ is a subset of a sequence $y$ if $x$ can be obtained by deleting several (possibly none or all) elements of $y$ and rearranging the elements in any order. For example, $[3,1,2,1]$, $[1, 2, 3]$, $[1, 1]$ and $[3, 2]$ are subsets of $[1, 1, 2, 3]$ but $[4]$ and $[2, 2]$ are not subsets of $[1, 1, 2, 3]$.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 5000$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains $2$ integers $n$ and $k$ ($2 \le n \le 5 \cdot 10^4$, $1 \leq k \leq \lfloor \frac{n}{2} \rfloor $).</p><p>The second line contains $2n$ integers $a_1, a_2, \ldots, a_{2n}$ ($1 \le a_i \le n$). It is guaranteed that every integer from $1$ to $n$ occurs exactly twice in $a$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $5 \cdot 10^4$.</p></div><div class="output-specification"><p>For each test case, output two lines. </p><p>On the first line of output, output $2k$ integers $l_1, l_2, \ldots, l_{2k}$.</p><p>On the second line of output, output $2k$ integers $r_1, r_2, \ldots r_{2k}$.</p><p>If there are multiple solutions, you may output any one of them.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 5000$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains $2$ integers $n$ and $k$ ($2 \le n \le 5 \cdot 10^4$, $1 \leq k \leq \lfloor \frac{n}{2} \rfloor $).</p><p>The second line contains $2n$ integers $a_1, a_2, \ldots, a_{2n}$ ($1 \le a_i \le n$). It is guaranteed that every integer from $1$ to $n$ occurs exactly twice in $a$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $5 \cdot 10^4$.</p>

## Output

<p>For each test case, output two lines. </p><p>On the first line of output, output $2k$ integers $l_1, l_2, \ldots, l_{2k}$.</p><p>On the second line of output, output $2k$ integers $r_1, r_2, \ldots r_{2k}$.</p><p>If there are multiple solutions, you may output any one of them.</p>





```input1|2,3,6,7
4
2 1
1 2 2 1
6 1
6 4 2 1 2 3 1 6 3 5 5 4
4 1
1 2 3 4 1 2 3 4
6 2
5 1 3 3 5 1 2 6 4 6 4 2
```




```output1
2 1
2 1
6 4
1 3
1 2
1 2
5 1 3 3
6 4 2 4
```



## Note

<p>In the first test case, we choose $l=[2,1]$ and $r=[2,1]$. $[2, 1]$ is a subset of $[a_1, a_2]$ and $[2, 1]$ is a subset of $[a_3, a_4]$, and $2 \oplus 1 = 2 \oplus 1 = 3$.</p><p>In the second test case, $6 \oplus 4 = 1 \oplus 3 = 2$.</p>
