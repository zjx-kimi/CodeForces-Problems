## Description

<div><p>You are given an integer $k$ and a string $s$ that consists only of characters 'a' (a lowercase Latin letter) and '*' (an asterisk).</p><p>Each asterisk should be replaced with several (from $0$ to $k$ inclusive) lowercase Latin letters 'b'. Different asterisk can be replaced with different counts of letter 'b'.</p><p>The result of the replacement is called a <span class="tex-font-style-it">BA-string</span>.</p><p>Two strings $a$ and $b$ are different if they either have different lengths or there exists such a position $i$ that $a_i \neq b_i$.</p><p>A string $a$ is lexicographically smaller than a string $b$ if and only if one of the following holds: </p><ul> <li> $a$ is a prefix of $b$, but $a \ne b$; </li><li> in the first position where $a$ and $b$ differ, the string $a$ has a letter that appears earlier in the alphabet than the corresponding letter in $b$. </li></ul><p>Now consider all different BA-strings and find the $x$-th lexicographically smallest of them.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 2000$)&nbsp;— the number of testcases.</p><p>The first line of each testcase contains three integers $n$, $k$ and $x$ ($1 \le n \le 2000$; $0 \le k \le 2000$; $1 \le x \le 10^{18}$). $n$ is the length of string $s$.</p><p>The second line of each testcase is a string $s$. It consists of $n$ characters, each of them is either 'a' (a lowercase Latin letter) or '*' (an asterisk).</p><p>The sum of $n$ over all testcases doesn't exceed $2000$. <span class="tex-font-style-bf">For each testcase $x$ doesn't exceed the total number of different BA-strings.</span> String $s$ contains at least one character 'a'.</p></div><div class="output-specification"><p>For each testcase, print a single string, consisting only of characters 'b' and 'a' (lowercase Latin letters)&nbsp;— the $x$-th lexicographically smallest BA-string.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 2000$)&nbsp;— the number of testcases.</p><p>The first line of each testcase contains three integers $n$, $k$ and $x$ ($1 \le n \le 2000$; $0 \le k \le 2000$; $1 \le x \le 10^{18}$). $n$ is the length of string $s$.</p><p>The second line of each testcase is a string $s$. It consists of $n$ characters, each of them is either 'a' (a lowercase Latin letter) or '*' (an asterisk).</p><p>The sum of $n$ over all testcases doesn't exceed $2000$. <span class="tex-font-style-bf">For each testcase $x$ doesn't exceed the total number of different BA-strings.</span> String $s$ contains at least one character 'a'.</p>

## Output

<p>For each testcase, print a single string, consisting only of characters 'b' and 'a' (lowercase Latin letters)&nbsp;— the $x$-th lexicographically smallest BA-string.</p>





```input1
3
2 4 3
a*
4 1 3
a**a
6 3 20
**a***
```




```output1
abb
abba
babbbbbbbbb
```



## Note

<p>In the first testcase of the example, BA-strings ordered lexicographically are: </p><ol> <li> <span class="tex-font-style-tt">a</span> </li><li> <span class="tex-font-style-tt">ab</span> </li><li> <span class="tex-font-style-tt">abb</span> </li><li> <span class="tex-font-style-tt">abbb</span> </li><li> <span class="tex-font-style-tt">abbbb</span> </li></ol><p>In the second testcase of the example, BA-strings ordered lexicographically are: </p><ol> <li> <span class="tex-font-style-tt">aa</span> </li><li> <span class="tex-font-style-tt">aba</span> </li><li> <span class="tex-font-style-tt">abba</span> </li></ol><p>Note that string "<span class="tex-font-style-tt">aba</span>" is only counted once, even though there are two ways to replace asterisks with characters 'b' to get it.</p>
