## Description

<div><p>LuoTianyi gives you <span class="tex-font-style-bf">a palindrome</span>$^{\dagger}$ string $s$, and she wants you to find out the length of the longest non-empty subsequence$^{\ddagger}$ of $s$ which is not a palindrome string. If there is no such subsequence, output $-1$ instead.</p><p>$^{\dagger}$ A palindrome is a string that reads the same backward as forward. For example, strings "<span class="tex-font-style-tt">z</span>", "<span class="tex-font-style-tt">aaa</span>", "<span class="tex-font-style-tt">aba</span>", "<span class="tex-font-style-tt">abccba</span>" are palindromes, but strings "<span class="tex-font-style-tt">codeforces</span>", "<span class="tex-font-style-tt">reality</span>", "<span class="tex-font-style-tt">ab</span>" are not.</p><p>$^{\ddagger}$ A string $a$ is a subsequence of a string $b$ if $a$ can be obtained from $b$ by deletion of several (possibly, zero or all) characters from $b$. For example, strings "<span class="tex-font-style-tt">a</span>", "<span class="tex-font-style-tt">aaa</span>", "<span class="tex-font-style-tt">bab</span>" are subsequences of string "<span class="tex-font-style-tt">abaab</span>", but strings "<span class="tex-font-style-tt">codeforces</span>", "<span class="tex-font-style-tt">bbb</span>", "<span class="tex-font-style-tt">h</span>" are not.</p></div><div class="input-specification"><p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 1000$) — the number of test cases. The description of test cases follows.</p><p>The first and the only line of each test case contains a single string $s$ ($1 \le |s| \le 50$) consisting of lowercase English letters — the string that LuoTianyi gives you. It's guaranteed that $s$ is a palindrome string.</p></div><div class="output-specification"><p>For each test case, output a single integer — the length of the longest non-empty subsequence which is not a palindrome string. If there is no such subsequence, output $-1$.</p></div>

## Input

<p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 1000$) — the number of test cases. The description of test cases follows.</p><p>The first and the only line of each test case contains a single string $s$ ($1 \le |s| \le 50$) consisting of lowercase English letters — the string that LuoTianyi gives you. It's guaranteed that $s$ is a palindrome string.</p>

## Output

<p>For each test case, output a single integer — the length of the longest non-empty subsequence which is not a palindrome string. If there is no such subsequence, output $-1$.</p>





```input1|2,4
4
abacaba
aaa
codeforcesecrofedoc
lol
```




```output1
6
-1
18
2
```



## Note

<p>In the first test case, "<span class="tex-font-style-tt">abcaba</span>" is a subsequence of "<span class="tex-font-style-tt">abacaba</span>" as we can delete the third letter of "<span class="tex-font-style-tt">abacaba</span>" to get "<span class="tex-font-style-tt">abcaba</span>", and "<span class="tex-font-style-tt">abcaba</span>" is not a palindrome string. We can prove that "<span class="tex-font-style-tt">abcaba</span>" is an example of the longest subsequences of "<span class="tex-font-style-tt">abacaba</span>" that isn't palindrome, so that the answer is $6$.</p><p>In the second test case, we can only get "<span class="tex-font-style-tt">a</span>" and "<span class="tex-font-style-tt">aa</span>", but they are all palindrome strings, so the answer is $-1$.</p>
