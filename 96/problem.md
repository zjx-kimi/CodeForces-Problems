## Description

<div><p>Monocarp is participating in a programming contest, which features $26$ problems, named from '<span class="tex-font-style-tt">A</span>' to '<span class="tex-font-style-tt">Z</span>'. The problems are sorted by difficulty. Moreover, it's known that Monocarp can solve problem '<span class="tex-font-style-tt">A</span>' in $1$ minute, problem '<span class="tex-font-style-tt">B</span>' in $2$ minutes, ..., problem '<span class="tex-font-style-tt">Z</span>' in $26$ minutes.</p><p>After the contest, you discovered his contest log&nbsp;— a string, consisting of uppercase Latin letters, such that the $i$-th letter tells which problem Monocarp was solving during the $i$-th minute of the contest. If Monocarp had spent enough time in total on a problem to solve it, he solved it. Note that Monocarp could have been thinking about a problem after solving it.</p><p>Given Monocarp's contest log, calculate the number of problems he solved during the contest.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 100$)&nbsp;— the number of testcases.</p><p>The first line of each testcase contains a single integer $n$ ($1 \le n \le 500$)&nbsp;— the duration of the contest, in minutes.</p><p>The second line contains a string of length exactly $n$, consisting only of uppercase Latin letters,&nbsp;— Monocarp's contest log.</p></div><div class="output-specification"><p>For each testcase, print a single integer&nbsp;— the number of problems Monocarp solved during the contest.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 100$)&nbsp;— the number of testcases.</p><p>The first line of each testcase contains a single integer $n$ ($1 \le n \le 500$)&nbsp;— the duration of the contest, in minutes.</p><p>The second line contains a string of length exactly $n$, consisting only of uppercase Latin letters,&nbsp;— Monocarp's contest log.</p>

## Output

<p>For each testcase, print a single integer&nbsp;— the number of problems Monocarp solved during the contest.</p>





```input1|2,3,6,7
3
6
ACBCBC
7
AAAAFPC
22
FEADBBDFFEDFFFDHHHADCC
```




```output1
3
1
4
```


