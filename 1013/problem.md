## Description

<div><p>An array $b$ is <span class="tex-font-style-it">good</span> if the sum of elements of $b$ is even. </p><p>You are given an array $a$ consisting of $n$ positive integers. In one operation, you can select an index $i$ and change $a_i := \lfloor \frac{a_i}{2} \rfloor$. $^\dagger$</p><p>Find the minimum number of operations (possibly $0$) needed to make $a$ good. It can be proven that it is <span class="tex-font-style-bf">always</span> possible to make $a$ good.</p><p>$^\dagger$ $\lfloor x \rfloor$ denotes the floor function — the largest integer less than or equal to $x$. For example, $\lfloor 2.7 \rfloor = 2$, $\lfloor \pi \rfloor = 3$ and $\lfloor 5 \rfloor =5$.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 1000$) — the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \leq n \leq 50$) — the length of the array $a$.</p><p>The second line of each test case contains $n$ space-separated integers $a_1,a_2,\ldots,a_n$ ($1 \leq a_i \leq 10^6$) — representing the array $a$.</p><p>Do note that the sum of $n$ over all test cases is not bounded.</p></div><div class="output-specification"><p>For each test case, output the minimum number of operations needed to make $a$ good.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 1000$) — the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \leq n \leq 50$) — the length of the array $a$.</p><p>The second line of each test case contains $n$ space-separated integers $a_1,a_2,\ldots,a_n$ ($1 \leq a_i \leq 10^6$) — representing the array $a$.</p><p>Do note that the sum of $n$ over all test cases is not bounded.</p>

## Output

<p>For each test case, output the minimum number of operations needed to make $a$ good.</p>





```input1|2,3,6,7
4
4
1 1 1 1
2
7 4
3
1 2 4
1
15
```




```output1
0
2
1
4
```



## Note

<p>In the first test case, array $a$ is already <span class="tex-font-style-it">good</span>.</p><p>In the second test case, we can perform on index $2$ twice. After the first operation, array $a$ becomes $[7,2]$. After performing on index $2$ again, $a$ becomes $[7,1]$, which is <span class="tex-font-style-it">good</span>. It can be proved that it is not possible to make $a$ <span class="tex-font-style-it">good</span> in less number of operations.</p><p>In the third test case, $a$ becomes $[0,2,4]$ if we perform the operation on index $1$ once. As $[0,2,4]$ is <span class="tex-font-style-it">good</span>, answer is $1$.</p><p>In the fourth test case, we need to perform the operation on index $1$ four times. After all operations, $a$ becomes $[0]$. It can be proved that it is not possible to make $a$ <span class="tex-font-style-it">good</span> in less number of operations.</p>
