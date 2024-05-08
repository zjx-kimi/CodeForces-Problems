## Description

<div><p>You are given an integer $n$ and three strings $a, b, c$, each consisting of $n$ lowercase Latin letters.</p><p>Let a template be a string $t$ consisting of $n$ lowercase and/or uppercase Latin letters. The string $s$ matches the template $t$ if the following conditions hold for all $i$ from $1$ to $n$: </p><ul> <li> if the $i$-th letter of the template is <span class="tex-font-style-bf">lowercase</span>, then $s_i$ must be <span class="tex-font-style-bf">the same</span> as $t_i$; </li><li> if the $i$-th letter of the template is <span class="tex-font-style-bf">uppercase</span>, then $s_i$ must be <span class="tex-font-style-bf">different</span> from the <span class="tex-font-style-bf">lowercase version</span> of $t_i$. For example, if there is a letter 'A' in the template, you cannot use the letter 'a' in the corresponding position of the string. </li></ul><p>Accordingly, the string doesn't match the template if the condition doesn't hold for at least one $i$.</p><p>Determine whether there exists a template $t$ such that the strings $a$ and $b$ match it, while the string $c$ does not.</p></div><div class="input-specification"><p>The first line contains an integer $t$ ($1 \le t \le 1000$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains an integer $n$ ($1 \le n \le 20$)&nbsp;— the length of the given strings.</p><p>The next three lines contain the strings $a, b$ and $c$. Each string consists of exactly $n$ lowercase Latin letters.</p></div><div class="output-specification"><p>For each testcase, print "<span class="tex-font-style-tt">YES</span>" if there exists a template $t$ such that the strings $a$ and $b$ match it, while the string $c$ does not. Otherwise, print "<span class="tex-font-style-tt">NO</span>".</p></div>

## Input

<p>The first line contains an integer $t$ ($1 \le t \le 1000$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains an integer $n$ ($1 \le n \le 20$)&nbsp;— the length of the given strings.</p><p>The next three lines contain the strings $a, b$ and $c$. Each string consists of exactly $n$ lowercase Latin letters.</p>

## Output

<p>For each testcase, print "<span class="tex-font-style-tt">YES</span>" if there exists a template $t$ such that the strings $a$ and $b$ match it, while the string $c$ does not. Otherwise, print "<span class="tex-font-style-tt">NO</span>".</p>





```input1|2,3,4,5,10,11,12,13
4
1
a
b
c
2
aa
bb
aa
10
mathforces
luckforces
adhoccoder
3
acc
abd
abc
```




```output1
YES
NO
YES
NO
```



## Note

<p>In the first test case, you can use the template "<span class="tex-font-style-tt">C</span>". The first letter of strings $a$ and $b$ differ from '<span class="tex-font-style-tt">c</span>', so they match the template. The first letter of string $c$ equals '<span class="tex-font-style-tt">c</span>', so it doesn't match.</p><p>In the third test case, you can use the template "<span class="tex-font-style-tt">CODEforces</span>".</p>
