## Description

<div><p>Vlad found a string $s$ consisting of $n$ lowercase Latin letters, and he wants to make it as short as possible.</p><p>To do this, he can remove <span class="tex-font-style-bf">any</span> pair of adjacent characters from $s$ any number of times, provided they are <span class="tex-font-style-bf">different</span>. For example, if $s$=<span class="tex-font-style-tt">racoon</span>, then by removing one pair of characters he can obtain the strings <span class="tex-font-style-tt">coon</span>, <span class="tex-font-style-tt">roon</span>, <span class="tex-font-style-tt">raon</span>, and <span class="tex-font-style-tt">raco</span>, but he cannot obtain <span class="tex-font-style-tt">racn</span> (because the removed letters were the same) or <span class="tex-font-style-tt">rcon</span> (because the removed letters were not adjacent).</p><p>What is the minimum length Vlad can achieve by applying any number of deletions?</p></div><div class="input-specification"><p>The first line of the input contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. Descriptions of the test cases follow.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$)&nbsp;— the length of the string $s$.</p><p>The second line of each test case contains the string $s$ consisting of $n$ lowercase Latin letters.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output a single number—the minimum length of the string $s$, after removing pairs of adjacent characters with different values.</p></div>

## Input

<p>The first line of the input contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. Descriptions of the test cases follow.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$)&nbsp;— the length of the string $s$.</p><p>The second line of each test case contains the string $s$ consisting of $n$ lowercase Latin letters.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output a single number—the minimum length of the string $s$, after removing pairs of adjacent characters with different values.</p>





```input1|2,3,6,7,10,11,14,15,18,19
10
4
aabc
5
abaca
10
avbvvcvvvd
7
abcdefg
5
dabbb
8
aacebeaa
7
bbbbacc
6
dacfcc
6
fdfcdc
9
dbdcfbbdc
```




```output1
0
1
2
1
1
0
1
0
0
1
```



## Note

<p>In the first test case of the example, you need to act as follows: "<span class="tex-font-style-tt">aabc</span>" $\rightarrow$ "<span class="tex-font-style-tt">ac</span>" $\rightarrow$ "". Note that with a different order of deletions, the string will not become empty.</p>
