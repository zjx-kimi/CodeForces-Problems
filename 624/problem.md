## Description

<div><p>You are given a string $s$, consisting of lowercase English letters. In one operation, you are allowed to swap any two characters of the string $s$.</p><p>A string $s$ of length $n$ is called an <span class="tex-font-style-it">anti-palindrome</span>, if $s[i] \ne s[n - i + 1]$ for every $i$ ($1 \le i \le n$). For example, the strings <span class="tex-font-style-tt">"codeforces"</span>, <span class="tex-font-style-tt">"string"</span> are <span class="tex-font-style-it">anti-palindromes</span>, but the strings <span class="tex-font-style-tt">"abacaba"</span>, <span class="tex-font-style-tt">"abc"</span>, <span class="tex-font-style-tt">"test"</span> are not.</p><p>Determine the minimum number of operations required to make the string $s$ an <span class="tex-font-style-it">anti-palindrome</span>, or output $-1$, if this is not possible.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>Each test case consists of two lines. The first line contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$)&nbsp;— the length of the string $s$.</p><p>The second line contains the string $s$, consisting of $n$ lowercase English letters.</p><p>The sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output a single integer&nbsp;— the minimum number of operations required to make the string $s$ an <span class="tex-font-style-it">anti-palindrome</span>, or $-1$ if this is not possible.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>Each test case consists of two lines. The first line contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$)&nbsp;— the length of the string $s$.</p><p>The second line contains the string $s$, consisting of $n$ lowercase English letters.</p><p>The sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output a single integer&nbsp;— the minimum number of operations required to make the string $s$ an <span class="tex-font-style-it">anti-palindrome</span>, or $-1$ if this is not possible.</p>





```input1|2,3,6,7,10,11,14,15,18,19
10
10
codeforces
3
abc
10
taarrrataa
10
dcbdbdcccc
4
wwww
12
cabbaccabaac
10
aadaaaaddc
14
aacdaaaacadcdc
6
abccba
12
dcbcaebacccd
```




```output1
0
-1
1
1
-1
3
-1
2
2
2
```



## Note

<p>In the first test case, the string <span class="tex-font-style-tt">"codeforces"</span> is already an <span class="tex-font-style-it">anti-palindrome</span>, so the answer is $0$.</p><p>In the second test case, it can be shown that the string <span class="tex-font-style-tt">"abc"</span> cannot be transformed into an <span class="tex-font-style-it">anti-palindrome</span> by performing the allowed operations, so the answer is $-1$.</p><p>In the third test case, it is enough to swap the second and the fifth characters of the string <span class="tex-font-style-tt">"taarrrataa"</span>, and the new string <span class="tex-font-style-tt">"trararataa"</span> will be an <span class="tex-font-style-it">anti-palindrome</span>, so the answer is $1$.</p>
