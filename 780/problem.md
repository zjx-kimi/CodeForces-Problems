## Description

<div><p>You are given an array of $n$ positive integers $a_1, a_2, \ldots, a_n$. In one operation, you can choose any number of the array and add $1$ to it. </p><p>Make at most $2n$ operations so that the array satisfies the following property: $a_{i+1}$ is <span class="tex-font-style-bf">not</span> divisible by $a_i$, for each $i = 1, 2, \ldots, n-1$. </p><p>You do <span class="tex-font-style-bf">not</span> need to minimize the number of operations.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^4$). The description of the test cases follows.</p><p>The first line of each test case contains an integer $n$ ($1\le n\le 10^4$)&nbsp;— the length of the given array. </p><p>The second line of each test case contains $n$ integers $a_1,a_2,\ldots,a_n$ ($1\le a_i\leq 10^9$)&nbsp;— the given array.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $5\cdot 10^4$.</p></div><div class="output-specification"><p>For each test case, print the answer on a separate line. </p><p>In the only line, print $n$ integers&nbsp;— the resulting array $a$ after applying at most $2n$ operations. </p><p>We can show that an answer always exists under the given constraints. If there are multiple answers, print any of them.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^4$). The description of the test cases follows.</p><p>The first line of each test case contains an integer $n$ ($1\le n\le 10^4$)&nbsp;— the length of the given array. </p><p>The second line of each test case contains $n$ integers $a_1,a_2,\ldots,a_n$ ($1\le a_i\leq 10^9$)&nbsp;— the given array.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $5\cdot 10^4$.</p>

## Output

<p>For each test case, print the answer on a separate line. </p><p>In the only line, print $n$ integers&nbsp;— the resulting array $a$ after applying at most $2n$ operations. </p><p>We can show that an answer always exists under the given constraints. If there are multiple answers, print any of them.</p>





```input1|2,3,6,7
3
4
2 4 3 6
3
1 2 3
2
4 2
```




```output1
4 5 6 7
3 2 3
4 2
```



## Note

<p>In the first test case, the array $[4, 5, 6, 7]$ can be achieved by applying $2$ operations to the first element, $1$ operation to the second element, $3$ operations to the third element, and $1$ operation to the last element. The total number of operations performed is $7$, which is less than the allowed $8$ operations in this case.</p><p>In the second test case, the array $[3, 2, 3]$ can be achieved by applying two operations to the first element. Another possible resulting array could be $[2, 3, 5]$, because the total number of operations does <span class="tex-font-style-bf">not</span> need to be minimum.</p><p>In the third test case, not applying any operations results in an array that satisfies the statement's property. Observe that it is not mandatory to make operations.</p>
