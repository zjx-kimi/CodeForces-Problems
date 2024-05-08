## Description

<div><p>You are given a string $s$. You can apply this operation to the string exactly once: choose index $i$ and move character $s_i$ to the beginning of the string (removing it at the old position). For example, if you apply the operation with index $i=4$ to the string "<span class="tex-font-style-tt">abaacd</span>" with numbering from $1$, you get the string "<span class="tex-font-style-tt">aabacd</span>". What is the lexicographically minimal$^{\dagger}$ string you can obtain by this operation?</p><p>$^{\dagger}$A string $a$ is lexicographically smaller than a string $b$ of the same length if and only if the following holds: </p><ul> <li> in the first position where $a$ and $b$ differ, the string $a$ has a letter that appears earlier in the alphabet than the corresponding letter in $b$. </li></ul></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^4$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 10 ^ 5$)&nbsp;— the length of the string.</p><p>The second line of each test case contains the string $s$ of length $n$, consisting of lowercase English letters.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10 ^ 5$.</p></div><div class="output-specification"><p>For each test case, on a separate line print the lexicographically smallest string that can be obtained after applying the operation to the original string exactly once.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^4$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 10 ^ 5$)&nbsp;— the length of the string.</p><p>The second line of each test case contains the string $s$ of length $n$, consisting of lowercase English letters.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10 ^ 5$.</p>

## Output

<p>For each test case, on a separate line print the lexicographically smallest string that can be obtained after applying the operation to the original string exactly once.</p>





```input1|2,3,6,7
4
3
cba
4
acac
5
abbcb
4
aaba
```




```output1
acb
aacc
abbcb
aaab
```



## Note

<p>In the first test case, you need to move the last character to the beginning.</p><p>In the second case, you need to move the second letter "<span class="tex-font-style-tt">a</span>".</p><p>In the third set you need to apply the operation with $i=1$, then the string will not change.</p>
