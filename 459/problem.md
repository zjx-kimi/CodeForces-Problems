## Description

<div><p>Your friends have an array of $n$ elements, calculated its array of prefix sums and passed it to you, accidentally losing one element during the transfer. Your task is to find out if the given array can matches <span class="tex-font-style-bf">permutation</span>.</p><p>A permutation of $n$ elements is an array of $n$ numbers from $1$ to $n$ such that each number occurs exactly <span class="tex-font-style-bf">one</span> times in it.</p><p>The array of prefix sums of the array $a$ — is such an array $b$ that $b_i = \sum_{j=1}^i a_j, 1 \le i \le n$.</p><p>For example, the original permutation was $[1, 5, 2, 4, 3]$. Its array of prefix sums — $[1, 6, 8, 12, 15]$. Having lost one element, you can get, for example, arrays $[6, 8, 12, 15]$ or $[1, 6, 8, 15]$.</p><p>It can also be shown that the array $[1, 2, 100]$ does not correspond to any permutation.</p></div><div class="input-specification"><p>The first line contains a positive number $t$ ($1 \le t \le 10^4$) — the number of test cases. The description of the test cases follows.</p><p>The first line of the description of each test case contains a positive number $n$ ($2 \le n \le 2 \cdot 10^5$) — the size of the initial array.</p><p>The second line of the description of each test case contains $n - 1$ positive number $a_i$ ($1 \le a_i \le 10^{18}$), $a_{i-1} &lt; a_i$ — elements of the array of prefix sums.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output "<span class="tex-font-style-tt">YES</span>" if such a permutation exists, and "<span class="tex-font-style-tt">NO</span>" otherwise.</p><p>You can output "<span class="tex-font-style-tt">YES</span>" and "<span class="tex-font-style-tt">NO</span>" in any case (for example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>" and "<span class="tex-font-style-tt">Yes</span>" will be recognized as a positive response).</p></div>

## Input

<p>The first line contains a positive number $t$ ($1 \le t \le 10^4$) — the number of test cases. The description of the test cases follows.</p><p>The first line of the description of each test case contains a positive number $n$ ($2 \le n \le 2 \cdot 10^5$) — the size of the initial array.</p><p>The second line of the description of each test case contains $n - 1$ positive number $a_i$ ($1 \le a_i \le 10^{18}$), $a_{i-1} &lt; a_i$ — elements of the array of prefix sums.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output "<span class="tex-font-style-tt">YES</span>" if such a permutation exists, and "<span class="tex-font-style-tt">NO</span>" otherwise.</p><p>You can output "<span class="tex-font-style-tt">YES</span>" and "<span class="tex-font-style-tt">NO</span>" in any case (for example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>" and "<span class="tex-font-style-tt">Yes</span>" will be recognized as a positive response).</p>





```input1|2,3,6,7,10,11,14,15,18,19,22,23
12
5
6 8 12 15
5
1 6 8 15
4
1 2 100
4
1 3 6
2
2
3
1 2
4
3 7 10
5
5 44 46 50
4
1 9 10
5
13 21 36 42
5
1 2 3 1000000000000000000
9
9 11 12 20 25 28 30 33
```




```output1
YES
YES
NO
YES
YES
NO
YES
NO
NO
NO
NO
NO
```



## Note

<p>In the fourth example, for example, the permutation $[1, 2, 3, 4]$ is suitable. In the fifth example, for example, the permutation $[2, 1]$ is suitable. In the seventh example, for example, the permutation $[1, 2, 4, 3]$ is suitable.</p>
