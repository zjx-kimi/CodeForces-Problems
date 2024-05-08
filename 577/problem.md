## Description

<div><p>A palindrome is a string that reads the same from left to right as from right to left. For example, <span class="tex-font-style-tt">abacaba</span>, <span class="tex-font-style-tt">aaaa</span>, <span class="tex-font-style-tt">abba</span>, <span class="tex-font-style-tt">racecar</span> are palindromes.</p><p>You are given a string $s$ consisting of lowercase Latin letters. The string $s$ is a palindrome.</p><p>You have to check whether it is possible to rearrange the letters in it to get <span class="tex-font-style-bf">another</span> palindrome (not equal to the given string $s$).</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 1000$)&nbsp;— the number of test cases.</p><p>The only line of each test case contains a string $s$ ($2 \le |s| \le 50$) consisting of lowercase Latin letters. This string is a palindrome.</p></div><div class="output-specification"><p>For each test case, print <span class="tex-font-style-tt">YES</span> if it is possible to rearrange the letters in the given string to get <span class="tex-font-style-bf">another</span> palindrome. Otherwise, print <span class="tex-font-style-tt">NO</span>. </p><p>You may print each letter in any case (<span class="tex-font-style-tt">YES</span>, <span class="tex-font-style-tt">yes</span>, <span class="tex-font-style-tt">Yes</span> will all be recognized as positive answer, <span class="tex-font-style-tt">NO</span>, <span class="tex-font-style-tt">no</span> and <span class="tex-font-style-tt">nO</span> will all be recognized as negative answer).</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 1000$)&nbsp;— the number of test cases.</p><p>The only line of each test case contains a string $s$ ($2 \le |s| \le 50$) consisting of lowercase Latin letters. This string is a palindrome.</p>

## Output

<p>For each test case, print <span class="tex-font-style-tt">YES</span> if it is possible to rearrange the letters in the given string to get <span class="tex-font-style-bf">another</span> palindrome. Otherwise, print <span class="tex-font-style-tt">NO</span>. </p><p>You may print each letter in any case (<span class="tex-font-style-tt">YES</span>, <span class="tex-font-style-tt">yes</span>, <span class="tex-font-style-tt">Yes</span> will all be recognized as positive answer, <span class="tex-font-style-tt">NO</span>, <span class="tex-font-style-tt">no</span> and <span class="tex-font-style-tt">nO</span> will all be recognized as negative answer).</p>





```input1|2,4
3
codedoc
gg
aabaa
```




```output1
YES
NO
NO
```



## Note

<p>In the first test case, it is possible to rearrange the letters in the palindrome <span class="tex-font-style-tt">codedoc</span> to obtain the string <span class="tex-font-style-tt">ocdedco</span>, which is different from the given string, but also a palindrome.</p>
