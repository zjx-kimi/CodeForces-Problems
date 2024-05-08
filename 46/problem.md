## Description

<div><p>Allen has an array $a_1, a_2,\ldots,a_n$. For every positive integer $k$ that is a divisor of $n$, Allen does the following:</p><ul> <li> He partitions the array into $\frac{n}{k}$ disjoint subarrays of length $k$. In other words, he partitions the array into the following subarrays: $$[a_1,a_2,\ldots,a_k],[a_{k+1}, a_{k+2},\ldots,a_{2k}],\ldots,[a_{n-k+1},a_{n-k+2},\ldots,a_{n}]$$ </li><li> Allen earns one point if there exists some positive integer $m$ ($m \geq 2$) such that if he replaces every element in the array with its remainder when divided by $m$, then all subarrays will be identical. </li></ul><p>Help Allen find the number of points he will earn.</p></div><div class="input-specification"><p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 10^4$) — the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \leq n \leq 2\cdot10^5$) — the length of the array $a$.</p><p>The second line of each test case contains $n$ integers $a_1, a_2,\ldots, a_n$ ($1 \leq a_i \leq n$) — the elements of the array $a$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$. </p></div><div class="output-specification"><p>For each test case, output a single integer — the number of points Allen will earn.</p></div>

## Input

<p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 10^4$) — the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \leq n \leq 2\cdot10^5$) — the length of the array $a$.</p><p>The second line of each test case contains $n$ integers $a_1, a_2,\ldots, a_n$ ($1 \leq a_i \leq n$) — the elements of the array $a$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$. </p>

## Output

<p>For each test case, output a single integer — the number of points Allen will earn.</p>





```input1|2,3,6,7,10,11,14,15
8
4
1 2 1 4
3
1 2 3
5
1 1 1 1 1
6
1 3 1 1 3 1
6
6 2 6 2 2 2
6
2 6 3 6 6 6
10
1 7 5 1 4 3 1 3 1 4
1
1
```




```output1
2
1
2
4
4
1
2
1
```



## Note

<p>In the first test case, $k=2$ earns a point since Allen can pick $m = 2$ and both subarrays will be equal to $[1, 0]$. $k=4$ also earns a point, since no matter what $m$ Allen chooses, there will be only one subarray and thus all subarrays are equal.</p><p>In the second test case, Allen earns $1$ point for $k=3$, where his choice for $m$ does not matter.</p>
