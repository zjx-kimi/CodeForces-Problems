## Description

<div><p>You are given an array $a$ of length $n$. You can perform the following operation several (possibly, zero) times:</p><ul> <li> Choose $i$, $j$, $b$: Swap the $b$-th digit in the binary representation of $a_i$ and $a_j$. </li></ul><p>Find the maximum possible value of $\max(a) - \min(a)$.</p><p>In a binary representation, bits are numbered from right (least significant) to left (most significant). Consider that there are an infinite number of leading zero bits at the beginning of any binary representation.</p><p>For example, swap the $0$-th bit for $4=100_2$ and $3=11_2$ will result $101_2=5$ and $10_2=2$. Swap the $2$-nd bit for $4=100_2$ and $3=11_2$ will result $000_2=0_2=0$ and $111_2=7$. </p><p>Here, $\max(a)$ denotes the maximum element of array $a$ and $\min(a)$ denotes the minimum element of array $a$.</p><p>The binary representation of $x$ is $x$ written in base $2$. For example, $9$ and $6$ written in base $2$ are $1001$ and $110$, respectively.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 128$) — the number of testcases.</p><p>The first line of each test case contains a single integer $n$ ($3 \le n \le 512$) — the length of array $a$.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($0 \le a_i &lt; 1024$) — the elements of array $a$.</p><p>It's guaranteed that the sum of $n$ over all testcases does not exceed $512$.</p></div><div class="output-specification"><p>For each testcase, print one integer — the maximum possible value of $\max(a) - \min(a)$.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 128$) — the number of testcases.</p><p>The first line of each test case contains a single integer $n$ ($3 \le n \le 512$) — the length of array $a$.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($0 \le a_i &lt; 1024$) — the elements of array $a$.</p><p>It's guaranteed that the sum of $n$ over all testcases does not exceed $512$.</p>

## Output

<p>For each testcase, print one integer — the maximum possible value of $\max(a) - \min(a)$.</p>





```input1|2,3,6,7
4
3
1 0 1
4
5 5 5 5
5
1 2 3 4 5
7
20 85 100 41 76 49 36
```




```output1
1
0
7
125
```



## Note

<p>In the first example, it can be shown that we do not need to perform any operations — the maximum value of $\max(a) - \min(a)$ is $1 - 0 = 1$.</p><p>In the second example, no operation can change the array — the maximum value of $\max(a) - \min(a)$ is $5 - 5 = 0$.</p><p>In the third example, initially $a = [1, 2, 3, 4, 5]$, we can perform one operation taking $i = 2$, $j = 5$, $b = 1$. The array now becomes $a = [1, 0, 3, 4, 7]$. It can be shown that any further operations do not lead to a better answer — therefore the answer is $\max(a) - \min(a) = 7 - 0 = 7$.</p>
