## Description

<div><p>Consider a string $s$ of $n$ lowercase English letters. Let $t_i$ be the string obtained by replacing the $i$-th character of $s$ with an asterisk character <span class="tex-font-style-tt">*</span>. For example, when $s = \mathtt{abc}$, we have $t_1 = \tt{*bc}$, $t_2 = \tt{a*c}$, and $t_3 = \tt{ab*}$.</p><p>Given a string $s$, count the number of distinct strings of lowercase English letters and asterisks that occur as a substring of at least one string in the set $\{s, t_1, \ldots, t_n \}$. The empty string should be counted.</p><p>Note that <span class="tex-font-style-tt">*</span>'s are just characters and do not play any special role as in, for example, regex matching.</p></div><div class="input-specification"><p>The only line contains a string $s$ of $n$ lowercase English letters ($1 \leq n \leq 10^5$).</p></div><div class="output-specification"><p>Print a single integer&nbsp;— the number of distinct strings of $s, t_1, \ldots, t_n$.</p></div>

## Input

<p>The only line contains a string $s$ of $n$ lowercase English letters ($1 \leq n \leq 10^5$).</p>

## Output

<p>Print a single integer&nbsp;— the number of distinct strings of $s, t_1, \ldots, t_n$.</p>





```input1
abc
```




```output1
15
```



## Note

<p>For the sample case, the distinct substrings are (empty string), <span class="tex-font-style-tt">a</span>, <span class="tex-font-style-tt">b</span>, <span class="tex-font-style-tt">c</span>, <span class="tex-font-style-tt">*</span>, <span class="tex-font-style-tt">ab</span>, <span class="tex-font-style-tt">a*</span>, <span class="tex-font-style-tt">bc</span>, <span class="tex-font-style-tt">b*</span>, <span class="tex-font-style-tt">*b</span>, <span class="tex-font-style-tt">*c</span>, <span class="tex-font-style-tt">abc</span>, <span class="tex-font-style-tt">ab*</span>, <span class="tex-font-style-tt">a*c</span>, <span class="tex-font-style-tt">*bc</span>.</p>
