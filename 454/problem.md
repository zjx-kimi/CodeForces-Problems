## Description

<div><p>Ntarsis has come up with an array $a$ of $n$ non-negative integers.</p><p>Call an array $b$ of $n$ integers <span class="tex-font-style-it">imbalanced</span> if it satisfies the following: </p><ul> <li> $-n\le b_i\le n$, $b_i \ne 0$, </li><li> there are no two indices $(i, j)$ ($1 \le i, j \le n$) such that $b_i + b_j = 0$, </li><li> for each $1 \leq i \leq n$, there are <span class="tex-font-style-bf">exactly</span> $a_i$ indices $j$ ($1 \le j \le n$) such that $b_i+b_j&gt;0$, where $i$ and $j$ are not necessarily distinct. </li></ul><p>Given the array $a$, Ntarsis wants you to construct some imbalanced array. Help him solve this task, or determine it is impossible.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^5$). The description of the test cases follows.</p><p>The first line of each test case has a single integer $n$ ($1 \leq n \leq 10^5$).</p><p>The next line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($0 \leq a_i \leq n$).</p><p>It is guaranteed that the sum of $n$ across all test cases does not exceed $10^5$.</p></div><div class="output-specification"><p>For each test case, output "<span class="tex-font-style-tt">NO</span>" if there exists no imbalanced array. </p><p>Otherwise, output "<span class="tex-font-style-tt">YES</span>". Then, on the next line, output $n$ integers $b_1, b_2, \ldots, b_n$ where $b_i \neq 0$ for all $1 \leq i \leq n$&nbsp;— an imbalanced array.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^5$). The description of the test cases follows.</p><p>The first line of each test case has a single integer $n$ ($1 \leq n \leq 10^5$).</p><p>The next line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($0 \leq a_i \leq n$).</p><p>It is guaranteed that the sum of $n$ across all test cases does not exceed $10^5$.</p>

## Output

<p>For each test case, output "<span class="tex-font-style-tt">NO</span>" if there exists no imbalanced array. </p><p>Otherwise, output "<span class="tex-font-style-tt">YES</span>". Then, on the next line, output $n$ integers $b_1, b_2, \ldots, b_n$ where $b_i \neq 0$ for all $1 \leq i \leq n$&nbsp;— an imbalanced array.</p>





```input1|2,3,6,7,10,11
5
1
1
4
1 4 3 4
3
0 1 0
4
4 3 2 1
3
1 3 1
```




```output1
YES
1 
NO
YES
-3 1 -2 
YES
4 2 -1 -3 
YES
-1 3 -1
```



## Note

<p>For the first test case, $b = [1]$ is an imbalanced array. This is because for $i = 1$, there is exactly one $j$ ($j = 1$) where $b_1 + b_j &gt; 0$.</p><p>For the second test case, it can be shown that there exists no imbalanced array.</p><p>For the third test case, $a = [0, 1, 0]$. The array $b = [-3, 1, -2]$ is an imbalanced array. </p><ul> <li> For $i = 1$ and $i = 3$, there exists no index $j$ such that $b_i + b_j &gt; 0$. </li><li> For $i = 2$, there is only one index $j = 2$ such that $b_i + b_j &gt; 0$ ($b_2 + b_2 = 1 + 1 = 2$). </li></ul> Another possible output for the third test case could be $b = [-2, 1, -3]$.
