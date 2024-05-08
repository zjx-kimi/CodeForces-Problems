## Description

<div><p>You are given a string $s$, consisting of lowercase Latin letters.</p><p>In one operation, you can select several (one or more) positions in it such that no two selected positions are adjacent to each other. Then you remove the letters on the selected positions from the string. The resulting parts are concatenated without changing their order.</p><p>What is the smallest number of operations required to make all the letters in $s$ the same?</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of testcases.</p><p>The only line of each testcase contains a string $s$, consisting of lowercase Latin letters. Its length is from $1$ to $2 \cdot 10^5$.</p><p>The total length of the strings over all testcases doesn't exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each testcase, print a single integer&nbsp;— the smallest number of operations required to make all the letters in the given string $s$ the same.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of testcases.</p><p>The only line of each testcase contains a string $s$, consisting of lowercase Latin letters. Its length is from $1$ to $2 \cdot 10^5$.</p><p>The total length of the strings over all testcases doesn't exceed $2 \cdot 10^5$.</p>

## Output

<p>For each testcase, print a single integer&nbsp;— the smallest number of operations required to make all the letters in the given string $s$ the same.</p>





```input1|2,4,6
5
abacaba
codeforces
oooooooo
abcdef
mewheniseearulhiiarul
```




```output1
1
3
0
2
4
```



## Note

<p>In the first testcase, you can select positions $2, 4$ and $6$ and remove the corresponding letters 'b', 'c' and 'b'.</p><p>In the third testcase, the letters in the string are already the same, so you don't have to make any operations.</p><p>In the fourth testcase, one of the possible solutions in $2$ operations is the following. You can select positions $1, 4, 6$ first. The string becomes "bce". Then select positions $1$ and $3$. The string becomes "c". All letters in it are the same, since it's just one letter.</p>
