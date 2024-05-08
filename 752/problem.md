## Description

<div><p>You are given a string $s$. You can reorder the characters to form a string $t$. Define $t_{\mathrm{max}}$ to be the lexicographical maximum of $t$ and $t$ in reverse order.</p><p>Given $s$ determine the lexicographically minimum value of $t_{\mathrm{max}}$ over all reorderings $t$ of $s$.</p><p>A string $a$ is lexicographically smaller than a string $b$ if and only if one of the following holds: </p><ul> <li> $a$ is a prefix of $b$, but $a \ne b$; </li><li> in the first position where $a$ and $b$ differ, the string $a$ has a letter that appears earlier in the alphabet than the corresponding letter in $b$. </li></ul></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \leq t \leq 10^5$) — the number of test cases. Descriptions of test cases follow.</p><p>The first and only line of each test case contains a string $s$ ($1 \leq |s| \leq 10^5$). $s$ consists of only lowercase English letters. </p><p>It is guaranteed that the sum of $|s|$ over all test cases does not exceed $10^5$.</p></div><div class="output-specification"><p>For each test case print the lexicographically minimum value of $t_{\mathrm{max}}$ over all reorderings $t$ of $s$. </p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \leq t \leq 10^5$) — the number of test cases. Descriptions of test cases follow.</p><p>The first and only line of each test case contains a string $s$ ($1 \leq |s| \leq 10^5$). $s$ consists of only lowercase English letters. </p><p>It is guaranteed that the sum of $|s|$ over all test cases does not exceed $10^5$.</p>

## Output

<p>For each test case print the lexicographically minimum value of $t_{\mathrm{max}}$ over all reorderings $t$ of $s$. </p>





```input1|2,4,6,8,10,12
12
a
aab
abb
abc
aabb
aabbb
aaabb
abbb
abbbb
abbcc
eaga
ffcaba
```




```output1
a
aba
bab
bca
abba
abbba
ababa
bbab
bbabb
bbcca
agea
acffba
```



## Note

<p>For the first test case, there is only one reordering of $s$, namely "<span class="tex-font-style-tt">a</span>".</p><p>For the second test case, there are three reorderings of $s$.</p><ul> <li> $t = \mathtt{aab}$: $t_{\mathrm{max}} = \max(\mathtt{aab}, \mathtt{baa}) = \mathtt{baa}$ </li><li> $t = \mathtt{aba}$: $t_{\mathrm{max}} = \max(\mathtt{aba}, \mathtt{aba}) = \mathtt{aba}$ </li><li> $t = \mathtt{baa}$: $t_{\mathrm{max}} = \max(\mathtt{baa}, \mathtt{aab}) = \mathtt{baa}$ </li></ul><p>The lexicographical minimum of $t_{\mathrm{max}}$ over all cases is "<span class="tex-font-style-tt">aba</span>". </p>
