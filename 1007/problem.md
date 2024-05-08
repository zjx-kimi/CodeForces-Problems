## Description

<div><p>You are given an array $a$ consisting of $n$ positive integers. </p><p>Find any permutation $p$ of $[1,2,\dots,n]$ such that:</p><ul> <li> $p_{i-2} &lt; p_i$ for all $i$, where $3 \leq i \leq n$, and </li><li> $a_{p_{i-1}} \neq a_{p_i}$ for all $i$, where $2 \leq i \leq n$. </li></ul><p>Or report that no such permutation exists.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 10^5$) — the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($3 \leq n \leq 3 \cdot 10^5$) — the length of the array $a$.</p><p>The second line of each test case contains $n$ space-separated integers $a_1,a_2,\ldots,a_n$ ($1 \leq a_i \leq n$) — representing the array $a$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $3 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output "<span class="tex-font-style-tt">NO</span>" if no such permutation exists, otherwise output "<span class="tex-font-style-tt">YES</span>" in the first line and print the permutation $p$ in the next line.</p><p>In case there are multiple permutations, print any one of them.</p><p>You can output "<span class="tex-font-style-tt">YES</span>" and "<span class="tex-font-style-tt">NO</span>" in any case (for example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>" and "<span class="tex-font-style-tt">YES</span>" will be recognized as a positive response).</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 10^5$) — the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($3 \leq n \leq 3 \cdot 10^5$) — the length of the array $a$.</p><p>The second line of each test case contains $n$ space-separated integers $a_1,a_2,\ldots,a_n$ ($1 \leq a_i \leq n$) — representing the array $a$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $3 \cdot 10^5$.</p>

## Output

<p>For each test case, output "<span class="tex-font-style-tt">NO</span>" if no such permutation exists, otherwise output "<span class="tex-font-style-tt">YES</span>" in the first line and print the permutation $p$ in the next line.</p><p>In case there are multiple permutations, print any one of them.</p><p>You can output "<span class="tex-font-style-tt">YES</span>" and "<span class="tex-font-style-tt">NO</span>" in any case (for example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>" and "<span class="tex-font-style-tt">YES</span>" will be recognized as a positive response).</p>





```input1|2,3,6,7
4
3
1 2 1
4
1 2 3 4
3
1 1 1
7
1 2 1 1 3 1 4
```




```output1
YES
1 2 3
YES
3 1 4 2
NO
YES
1 2 3 5 4 7 6
```



## Note

<p>In the first test case, $p=[1,2,3]$ is the only permutation of $[1,2,3]$ that satisfy the given constraints.</p><p>In the second test case, $[1,3,2,4]$, $[2,1,4,3]$ and some other permutations are also acceptable.</p><p>In the third test case, it can be proved that there does not exist any permutation of $[1,2,3]$ satisfying the given constraints.</p>
