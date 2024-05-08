## Description

<div><p>Serval has a string $s$ that only consists of <span class="tex-font-style-tt">0</span> and <span class="tex-font-style-tt">1</span> of length $n$. The $i$-th character of $s$ is denoted as $s_i$, where $1\leq i\leq n$.</p><p>Serval can perform the following operation called Inversion Magic on the string $s$:</p><ul> <li> Choose an segment $[l, r]$ ($1\leq l\leq r\leq n$). For $l\leq i\leq r$, change $s_i$ into <span class="tex-font-style-tt">1</span> if $s_i$ is <span class="tex-font-style-tt">0</span>, and change $s_i$ into <span class="tex-font-style-tt">0</span> if $s_i$ is <span class="tex-font-style-tt">1</span>. </li></ul><p>For example, let $s$ be <span class="tex-font-style-tt">010100</span> and the segment $[2,5]$ is chosen. The string $s$ will be <span class="tex-font-style-tt">001010</span> after performing the Inversion Magic.</p><p>Serval wants to make $s$ a palindrome after performing Inversion Magic <span class="tex-font-style-bf">exactly once</span>. Help him to determine whether it is possible.</p><p>A string is a palindrome iff it reads the same backwards as forwards. For example, <span class="tex-font-style-tt">010010</span> is a palindrome but <span class="tex-font-style-tt">10111</span> is not.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1\leq t\leq 10^4$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2\leq n\leq 10^5$) — the length of string $s$.</p><p>The second line of each test case contains a binary string $s$ of length $n$. Only characters <span class="tex-font-style-tt">0</span> and <span class="tex-font-style-tt">1</span> can appear in $s$.</p><p>It's guaranteed that the sum of $n$ over all test cases does not exceed $2\cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, print <span class="tex-font-style-tt">Yes</span> if $s$ can be a palindrome after performing Inversion Magic exactly once, and print <span class="tex-font-style-tt">No</span> if not.</p><p>You can output <span class="tex-font-style-tt">Yes</span> and <span class="tex-font-style-tt">No</span> in any case (for example, strings <span class="tex-font-style-tt">yEs</span>, <span class="tex-font-style-tt">yes</span>, <span class="tex-font-style-tt">Yes</span> and <span class="tex-font-style-tt">YES</span> will be recognized as a positive response).</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1\leq t\leq 10^4$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2\leq n\leq 10^5$) — the length of string $s$.</p><p>The second line of each test case contains a binary string $s$ of length $n$. Only characters <span class="tex-font-style-tt">0</span> and <span class="tex-font-style-tt">1</span> can appear in $s$.</p><p>It's guaranteed that the sum of $n$ over all test cases does not exceed $2\cdot 10^5$.</p>

## Output

<p>For each test case, print <span class="tex-font-style-tt">Yes</span> if $s$ can be a palindrome after performing Inversion Magic exactly once, and print <span class="tex-font-style-tt">No</span> if not.</p><p>You can output <span class="tex-font-style-tt">Yes</span> and <span class="tex-font-style-tt">No</span> in any case (for example, strings <span class="tex-font-style-tt">yEs</span>, <span class="tex-font-style-tt">yes</span>, <span class="tex-font-style-tt">Yes</span> and <span class="tex-font-style-tt">YES</span> will be recognized as a positive response).</p>





```input1|2,3,6,7
3
4
1001
5
10010
7
0111011
```




```output1
Yes
Yes
No
```



## Note

<p>In the first test case, Serval can perform Inversion Magic on the segment $[1,4]$. The string $s$ will be <span class="tex-font-style-tt">0110</span> after the magic.</p><p>In the second test case, Serval can perform Inversion Magic on the segment $[1,3]$. The string $s$ will be <span class="tex-font-style-tt">01110</span> after the magic.</p><p>In the third test case, Serval can't make $s$ a palindrome by performing Inversion Magic exactly once.</p>
