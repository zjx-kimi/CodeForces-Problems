## Description

<div><p>Rudolf has a string $s$ of length $n$. Rudolf considers the string $s$ to be ugly if it contains the substring$^\dagger$ "<span class="tex-font-style-tt">pie</span>" or the substring "<span class="tex-font-style-tt">map</span>", otherwise the string $s$ will be considered beautiful.</p><p>For example, "<span class="tex-font-style-tt">ppiee</span>", "<span class="tex-font-style-tt">mmap</span>", "<span class="tex-font-style-tt">dfpiefghmap</span>" are ugly strings, while "<span class="tex-font-style-tt">mathp</span>", "<span class="tex-font-style-tt">ppiiee</span>" are beautiful strings.</p><p>Rudolf wants to shorten the string $s$ by removing some characters to make it beautiful.</p><p>The main character doesn't like to strain, so he asks you to make the string beautiful by removing the minimum number of characters. He can remove characters from <span class="tex-font-style-bf">any</span> positions in the string (not just from the beginning or end of the string).</p><p>$^\dagger$ String $a$ is a substring of $b$ if there exists a <span class="tex-font-style-bf">consecutive</span> segment of characters in string $b$ equal to $a$.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. The descriptions of the test cases follow.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 10^6$) — the length of the string $s$.</p><p>The next line of each test case contains the string $s$ of length $n$. The string $s$ consists of lowercase Latin letters.</p><p>The sum of $n$ over all test cases does not exceed $10^6$.</p></div><div class="output-specification"><p>For each test case, output a single integer — the minimum number of characters that need to be deleted to make the string $s$ beautiful. If the string is initially beautiful, then output $0$.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. The descriptions of the test cases follow.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 10^6$) — the length of the string $s$.</p><p>The next line of each test case contains the string $s$ of length $n$. The string $s$ consists of lowercase Latin letters.</p><p>The sum of $n$ over all test cases does not exceed $10^6$.</p>

## Output

<p>For each test case, output a single integer — the minimum number of characters that need to be deleted to make the string $s$ beautiful. If the string is initially beautiful, then output $0$.</p>





```input1|2,3,6,7,10,11
6
9
mmapnapie
9
azabazapi
8
mappppie
18
mapmapmapmapmapmap
1
p
11
pppiepieeee
```




```output1
2
0
2
6
0
2
```



## Note

<p>In the first test case, for example, you can delete the $4$th and $9$th characters to make the string beautiful.</p><p>In the second test case, the string is already beautiful.</p>
