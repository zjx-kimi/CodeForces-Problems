## Description

<div><p>You are given two strings $a$ and $b$, consisting of lowercase Latin letters.</p><p>A template $t$ is string, consisting of lowercase Latin letters and asterisks (character '*'). A template is called <span class="tex-font-style-it">asterisk-minor</span> if the number of asterisks in it is less than or equal to the number of letters in it.</p><p>A string $s$ is said to be matching a template $t$ if you can replace each asterisk in $t$ with a string of lowercase Latin letters (possibly, an empty string) so that it becomes equal to $s$.</p><p>Find an <span class="tex-font-style-it">asterisk-minor</span> template such that both $a$ and $b$ match it, or report that such a template doesn't exist. If there are multiple answers, print any of them.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of testcases.</p><p>The first line of each testcase contains a string $a$ ($1 \le |a| \le 50$, where $|a|$ is the length of $a$), consisting of lowercase Latin letters.</p><p>The second line contains a string $b$ ($1 \le |b| \le 50$), consisting of lowercase Latin letters.</p></div><div class="output-specification"><p>For each testcase, output "<span class="tex-font-style-tt">NO</span>", if there doesn't exist an <span class="tex-font-style-it">asterisk-minor</span> template that both $a$ and $b$ match. Otherwise, print "<span class="tex-font-style-tt">YES</span>" in the first line and the template in the second line. If there are multiple answers, print any of them.</p><p>A template should consist only of lowercase Latin letters and asterisks (character '*'). The number of asterisks should be less than or equal to the number of letters.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of testcases.</p><p>The first line of each testcase contains a string $a$ ($1 \le |a| \le 50$, where $|a|$ is the length of $a$), consisting of lowercase Latin letters.</p><p>The second line contains a string $b$ ($1 \le |b| \le 50$), consisting of lowercase Latin letters.</p>

## Output

<p>For each testcase, output "<span class="tex-font-style-tt">NO</span>", if there doesn't exist an <span class="tex-font-style-it">asterisk-minor</span> template that both $a$ and $b$ match. Otherwise, print "<span class="tex-font-style-tt">YES</span>" in the first line and the template in the second line. If there are multiple answers, print any of them.</p><p>A template should consist only of lowercase Latin letters and asterisks (character '*'). The number of asterisks should be less than or equal to the number of letters.</p>





```input1|2,3,6,7,10,11
6
aaab
zzzb
codeforces
atcoder
codeforces
tokitlx
aaaa
aaaaaa
abcd
abcd
c
f
```




```output1
YES
*b
YES
*co*
NO
YES
a*a*a*a
YES
abcd
NO
```



## Note

<p>In the first testcase, for a template "<span class="tex-font-style-tt">*b</span>", you can replace the only asterisk with "<span class="tex-font-style-tt">aaa</span>" to get "<span class="tex-font-style-tt">aaab</span>" (which is equal to $a$) or with "<span class="tex-font-style-tt">zzz</span>" to get "<span class="tex-font-style-tt">zzzb</span>" (which is equal to $b$).</p><p>In the third testcase, a template "<span class="tex-font-style-tt">*o*</span>" is not <span class="tex-font-style-it">asterisk-minor</span>, as it contains more asterisks than letters. There are no <span class="tex-font-style-it">asterisk-minor</span> templates that both $a$ and $b$ match.</p><p>In the fourth testcase, for a template "<span class="tex-font-style-tt">a*a*a*a</span>", you can replace all asterisks with empty strings to get "<span class="tex-font-style-tt">aaaa</span>" (which is equal to $a$) or two of them with "<span class="tex-font-style-tt">a</span>" and two of them with an empty string to get "<span class="tex-font-style-tt">aaaaaa</span>" (which is equal to $b$).</p><p>In the fifth testcase, there are no asterisks in a template "<span class="tex-font-style-tt">abcd</span>", so only "<span class="tex-font-style-tt">abcd</span>" can match it (which is coincidentally both $a$ and $b$).</p>
