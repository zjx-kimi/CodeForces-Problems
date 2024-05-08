## Description

<div><p>Recall that string $a$ is lexicographically smaller than string $b$ if $a$ is a prefix of $b$ (and $a \ne b$), or there exists an index $i$ ($1 \le i \le \min(|a|, |b|)$) such that $a_i &lt; b_i$, and for any index $j$ ($1 \le j &lt; i$) $a_j = b_j$.</p><p>Consider a sequence of strings $s_1, s_2, \dots, s_n$, each consisting of lowercase Latin letters. String $s_1$ is given explicitly, and all other strings are generated according to the following rule: to obtain the string $s_i$, a character is removed from string $s_{i-1}$ in such a way that string $s_i$ is lexicographically minimal.</p><p>For example, if $s_1 = \mathrm{dacb}$, then string $s_2 = \mathrm{acb}$, string $s_3 = \mathrm{ab}$, string $s_4 = \mathrm{a}$.</p><p>After that, we obtain the string $S = s_1 + s_2 + \dots + s_n$ ($S$ is the concatenation of all strings $s_1, s_2, \dots, s_n$).</p><p>You need to output the character in position $pos$ of the string $S$ (i. e. the character $S_{pos}$).</p></div><div class="input-specification"><p>The first line contains one integer $t$ — the number of test cases ($1 \le t \le 10^4$).</p><p>Each test case consists of two lines. The first line contains the string $s_1$ ($1 \le |s_1| \le 10^6$), consisting of lowercase Latin letters. The second line contains the integer $pos$ ($1 \le pos \le \frac{|s_1| \cdot (|s_1| +1)}{2}$). You may assume that $n$ is equal to the length of the given string ($n = |s_1|$).</p><p>Additional constraint on the input: the sum of $|s_1|$ over all test cases does not exceed $10^6$.</p></div><div class="output-specification"><p>For each test case, print the answer — the character that is at position $pos$ in string $S$. <span class="tex-font-style-bf">Note that the answers between different test cases are not separated by spaces or line breaks</span>.</p></div>

## Input

<p>The first line contains one integer $t$ — the number of test cases ($1 \le t \le 10^4$).</p><p>Each test case consists of two lines. The first line contains the string $s_1$ ($1 \le |s_1| \le 10^6$), consisting of lowercase Latin letters. The second line contains the integer $pos$ ($1 \le pos \le \frac{|s_1| \cdot (|s_1| +1)}{2}$). You may assume that $n$ is equal to the length of the given string ($n = |s_1|$).</p><p>Additional constraint on the input: the sum of $|s_1|$ over all test cases does not exceed $10^6$.</p>

## Output

<p>For each test case, print the answer — the character that is at position $pos$ in string $S$. <span class="tex-font-style-bf">Note that the answers between different test cases are not separated by spaces or line breaks</span>.</p>





```input1|2,3,6,7
3
cab
6
abcd
9
x
1
```




```output1
abx
```


