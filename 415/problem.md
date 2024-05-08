## Description

<div><p>You are given two strings $a$ and $b$ of equal length, consisting of only characters <span class="tex-font-style-tt">0</span> and/or <span class="tex-font-style-tt">1</span>; both strings start with character <span class="tex-font-style-tt">0</span> and end with character <span class="tex-font-style-tt">1</span>. </p><p>You can perform the following operation any number of times (possibly zero): </p><ul> <li> choose one of the strings and two <span class="tex-font-style-bf">equal</span> characters in it; then turn all characters between them into those characters. </li></ul><p>Formally, you choose one of these two strings (let the chosen string be $s$), then pick two integers $l$ and $r$ such that $1 \le l &lt; r \le |s|$ and $s_l = s_r$, then replace every character $s_i$ such that $l &lt; i &lt; r$ with $s_l$.</p><p>For example, if the chosen string is <span class="tex-font-style-tt">010101</span>, you can transform it into one of the following strings by applying one operation:</p><ul> <li> <span class="tex-font-style-tt">000101</span> if you choose $l = 1$ and $r = 3$; </li><li> <span class="tex-font-style-tt">000001</span> if you choose $l = 1$ and $r = 5$; </li><li> <span class="tex-font-style-tt">010001</span> if you choose $l = 3$ and $r = 5$; </li><li> <span class="tex-font-style-tt">010111</span> if you choose $l = 4$ and $r = 6$; </li><li> <span class="tex-font-style-tt">011111</span> if you choose $l = 2$ and $r = 6$; </li><li> <span class="tex-font-style-tt">011101</span> if you choose $l = 2$ and $r = 4$. </li></ul><p>You have to determine if it's possible to make the given strings equal by applying this operation any number of times.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 2000$) &nbsp;— the number of test cases.</p><p>Each test case consists of two lines: </p><ul> <li> the first line contains the string $a$ ($2 \le |a| \le 5000$), consisting of only characters <span class="tex-font-style-tt">0</span> and/or <span class="tex-font-style-tt">1</span>. </li><li> the second line contains the string $b$ ($2 \le |b| \le 5000$), consisting of only characters <span class="tex-font-style-tt">0</span> and/or <span class="tex-font-style-tt">1</span>. </li></ul><p>Additional constraints on the input: </p><ul> <li> in each test case, $|a| = |b|$ (the strings have equal length); </li><li> in each test case, both strings start with <span class="tex-font-style-tt">0</span> and end with <span class="tex-font-style-tt">1</span>; </li><li> the total length of all strings $a$ in all test cases does not exceed $5000$. </li></ul></div><div class="output-specification"><p>For each test case, print <span class="tex-font-style-tt">YES</span> if it is possible to make the strings equal. Otherwise, print <span class="tex-font-style-tt">NO</span>. You can print each letter in any register.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 2000$) &nbsp;— the number of test cases.</p><p>Each test case consists of two lines: </p><ul> <li> the first line contains the string $a$ ($2 \le |a| \le 5000$), consisting of only characters <span class="tex-font-style-tt">0</span> and/or <span class="tex-font-style-tt">1</span>. </li><li> the second line contains the string $b$ ($2 \le |b| \le 5000$), consisting of only characters <span class="tex-font-style-tt">0</span> and/or <span class="tex-font-style-tt">1</span>. </li></ul><p>Additional constraints on the input: </p><ul> <li> in each test case, $|a| = |b|$ (the strings have equal length); </li><li> in each test case, both strings start with <span class="tex-font-style-tt">0</span> and end with <span class="tex-font-style-tt">1</span>; </li><li> the total length of all strings $a$ in all test cases does not exceed $5000$. </li></ul>

## Output

<p>For each test case, print <span class="tex-font-style-tt">YES</span> if it is possible to make the strings equal. Otherwise, print <span class="tex-font-style-tt">NO</span>. You can print each letter in any register.</p>





```input1|2,3,6,7,10,11,14,15
7
01010001
01110101
01001
01001
000101
010111
00001
01111
011
001
001001
011011
010001
011011
```




```output1
YES
YES
YES
NO
NO
NO
YES
```



## Note

<p>In the first test case, we can perform the following operations: </p><ol> <li> choose the string $a$, $l = 2$, $r = 4$; after this operation, $a$ is <span class="tex-font-style-tt">01110001</span>, $b$ is <span class="tex-font-style-tt">01110101</span>; </li><li> choose the string $b$, $l = 5$, $r = 7$; after this operation, $a$ is <span class="tex-font-style-tt">01110001</span>, $b$ is <span class="tex-font-style-tt">01110001</span>. </li></ol><p>In the second test case, the strings are already equal.</p><p>In the third test case, we can perform the following operations: </p><ol> <li> choose the string $a$, $l = 4$, $r = 6$; after this operation, $a$ is <span class="tex-font-style-tt">000111</span>, $b$ is <span class="tex-font-style-tt">010111</span>; </li><li> choose the string $b$, $l = 1$, $r = 3$; after this operation, $a$ is <span class="tex-font-style-tt">000111</span>, $b$ is <span class="tex-font-style-tt">000111</span>; </li></ol><p>In the fourth and fifth test cases, it's impossible to make the given strings equal.</p>
