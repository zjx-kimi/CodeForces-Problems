## Description

<div><p>You are given a string $s$, consisting of lowercase Latin letters and/or question marks.</p><p>A <span class="tex-font-style-it">tandem repeat</span> is a string of an even length such that its first half is equal to its second half.</p><p>A string $a$ is a substring of a string $b$ if $a$ can be obtained from $b$ by the deletion of several (possibly, zero or all) characters from the beginning and several (possibly, zero or all) characters from the end.</p><p>Your goal is to replace each question mark with some lowercase Latin letter in such a way that the length of the longest substring that is a tandem repeat is maximum possible.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 1000$)&nbsp;— the number of testcases.</p><p>The only line of each testcase contains a string $s$ ($1 \le |s| \le 5000$), consisting only of lowercase Latin letters and/or question marks.</p><p>The total length of the strings over all testcases doesn't exceed $5000$. </p></div><div class="output-specification"><p>For each testcase, print a single integer&nbsp;— the maximum length of the longest substring that is a tandem repeat after you replace each question mark in the string with some lowercase Latin letter.</p><p>If it's impossible to make any tandem repeat substrings in the string, print $0$.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 1000$)&nbsp;— the number of testcases.</p><p>The only line of each testcase contains a string $s$ ($1 \le |s| \le 5000$), consisting only of lowercase Latin letters and/or question marks.</p><p>The total length of the strings over all testcases doesn't exceed $5000$. </p>

## Output

<p>For each testcase, print a single integer&nbsp;— the maximum length of the longest substring that is a tandem repeat after you replace each question mark in the string with some lowercase Latin letter.</p><p>If it's impossible to make any tandem repeat substrings in the string, print $0$.</p>





```input1|2,4
4
zaabaabz
?????
code?????s
codeforces
```




```output1
6
4
10
0
```


