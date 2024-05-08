## Description

<div><div class="epigraph"><div class="epigraph-text">Quantum entanglement is when two particles link together in a certain way no matter how far apart they are in space.</div></div><p>You are given a string $s$. A pair of its non-empty substrings $(a, b)$ is called <span class="tex-font-style-it">entangled</span> if there is a (possibly empty) link string $c$ such that:</p><ul> <li> Every occurrence of $a$ in $s$ is immediately followed by $cb$; </li><li> Every occurrence of $b$ in $s$ is immediately preceded by $ac$. </li></ul><p>In other words, $a$ and $b$ occur in $s$ only as substrings of $acb$. Compute the total number of entangled pairs of substrings of $s$.</p><p>A string $a$ is a substring of a string $b$ if $a$ can be obtained from $b$ by the deletion of several (possibly zero or all) characters from the beginning and several (possibly zero or all) characters from the end.</p></div><div class="input-specification"><p>The first and only line contains a string $s$ of lowercase English letters ($1 \leq |s| \leq 10^5$) — the string for which you should count pairs of entangled substrings.</p></div><div class="output-specification"><p>Output a single integer, the number of entangled pairs of substrings of $s$.</p></div>

## Input

<p>The first and only line contains a string $s$ of lowercase English letters ($1 \leq |s| \leq 10^5$) — the string for which you should count pairs of entangled substrings.</p>

## Output

<p>Output a single integer, the number of entangled pairs of substrings of $s$.</p>





```input1
abba
```




```input2
abacaba
```




```input3
abcabcabcabc
```




```input4
adamant
```




```output1
1
```




```output2
0
```




```output3
5
```




```output4
82
```



## Note

<p>In the first example, the only entangled pair is (<span class="tex-font-style-tt">ab,ba</span>). For this pair, the corresponding link string $c$ is empty, as they only occur as substrings of the whole string <span class="tex-font-style-tt">abba</span>, which doesn't have any characters between <span class="tex-font-style-tt">ab</span> and <span class="tex-font-style-tt">ba</span>.</p><p>In the second example, there are no entangled pairs.</p><p>In the third example, the entangled pairs are (<span class="tex-font-style-tt">a,b</span>), (<span class="tex-font-style-tt">b,c</span>), (<span class="tex-font-style-tt">a,c</span>), (<span class="tex-font-style-tt">a,bc</span>), and (<span class="tex-font-style-tt">ab,c</span>). For most pairs, the corresponding link string $c$ is empty, except for the pair (<span class="tex-font-style-tt">a,c</span>), for which the link string $c$ is <span class="tex-font-style-tt">b</span>, as <span class="tex-font-style-tt">a</span> and <span class="tex-font-style-tt">c</span> only occur as substrings of the string <span class="tex-font-style-tt">abc</span>.</p>
