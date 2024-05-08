## Description

<div><p>Marcos loves strings a lot, so he has a favorite string $s$ consisting of lowercase English letters. For this string, he wrote down all its non-empty prefixes and suffixes (except for $s$) on a piece of paper in arbitrary order. You see all these strings and wonder if Marcos' favorite string is a palindrome or not. So, your task is to decide whether $s$ is a palindrome by just looking at the piece of paper.</p><p>A string $a$ is a prefix of a string $b$ if $a$ can be obtained from $b$ by deletion of several (possibly, zero or all) characters from the end.</p><p>A string $a$ is a suffix of a string $b$ if $a$ can be obtained from $b$ by deletion of several (possibly, zero or all) characters from the beginning.</p><p>A palindrome is a string that reads the same backward as forward, for example, strings "<span class="tex-font-style-tt">gg</span>", "<span class="tex-font-style-tt">ioi</span>", "<span class="tex-font-style-tt">abba</span>", "<span class="tex-font-style-tt">icpci</span>" are palindromes, but strings "<span class="tex-font-style-tt">codeforces</span>", "<span class="tex-font-style-tt">abcd</span>", "<span class="tex-font-style-tt">alt</span>" are not.</p></div><div class="input-specification"><p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 120$)&nbsp;— the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2\le n \le 20$)&nbsp;— the length of the string $s$.</p><p>The second line of each test case contains $2n-2$ strings $a_1, a_2, \cdots, a_{2n-2}$&nbsp;— all non-empty prefixes and suffixes of $s$, not including itself, in arbitrary order.</p><p>It is guaranteed that these strings are all the non-empty prefixes and suffixes of some string consisting of lowercase English letters.</p></div><div class="output-specification"><p>For each test case, output "<span class="tex-font-style-tt">YES</span>" if $s$ is a palindrome, and "<span class="tex-font-style-tt">NO</span>" otherwise.</p><p>You can output the answer in any case (upper or lower). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as positive responses.</p></div>

## Input

<p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 120$)&nbsp;— the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2\le n \le 20$)&nbsp;— the length of the string $s$.</p><p>The second line of each test case contains $2n-2$ strings $a_1, a_2, \cdots, a_{2n-2}$&nbsp;— all non-empty prefixes and suffixes of $s$, not including itself, in arbitrary order.</p><p>It is guaranteed that these strings are all the non-empty prefixes and suffixes of some string consisting of lowercase English letters.</p>

## Output

<p>For each test case, output "<span class="tex-font-style-tt">YES</span>" if $s$ is a palindrome, and "<span class="tex-font-style-tt">NO</span>" otherwise.</p><p>You can output the answer in any case (upper or lower). For example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will be recognized as positive responses.</p>





```input1|2,3,6,7,10,11
5
4
bcd cd a d abc ab
3
i io i oi
2
g g
3
t al lt a
4
bba a ab a abb ba
```




```output1
NO
YES
YES
NO
YES
```



## Note

<p>In the first test case, $s$ is "<span class="tex-font-style-tt">abcd</span>". Its prefixes are "<span class="tex-font-style-tt">a</span>", "<span class="tex-font-style-tt">ab</span>" and "<span class="tex-font-style-tt">abc</span>", and its suffixes are "<span class="tex-font-style-tt">d</span>", "<span class="tex-font-style-tt">cd</span>" and "<span class="tex-font-style-tt">bcd</span>". As the string "<span class="tex-font-style-tt">abcd</span>" is not a palindrome, the answer is <span class="tex-font-style-tt">NO</span>.</p><p>In the second test case, $s$ is "<span class="tex-font-style-tt">ioi</span>". Its prefixes are "<span class="tex-font-style-tt">i</span>" and "<span class="tex-font-style-tt">io</span>", and its suffixes are "<span class="tex-font-style-tt">i</span>" and "<span class="tex-font-style-tt">oi</span>". As the string "<span class="tex-font-style-tt">ioi</span>" is a palindrome, the answer is <span class="tex-font-style-tt">YES</span>.</p><p>In the third test case, $s$ is "<span class="tex-font-style-tt">gg</span>" which is a palindrome.</p><p>In the fourth test case, $s$ is "<span class="tex-font-style-tt">alt</span>" which is not a palindrome.</p>
