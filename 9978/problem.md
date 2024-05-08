## Description

<div><p>Nikita had a word consisting of exactly $3$ lowercase Latin letters. The letters in the Latin alphabet are numbered from $1$ to $26$, where the letter "<span class="tex-font-style-tt">a</span>" has the index $1$, and the letter "<span class="tex-font-style-tt">z</span>" has the index $26$.</p><p>He encoded this word as the sum of the positions of all the characters in the alphabet. For example, the word "<span class="tex-font-style-tt">cat</span>" he would encode as the integer $3 + 1 + 20 = 24$, because the letter "<span class="tex-font-style-tt">c</span>" has the index $3$ in the alphabet, the letter "<span class="tex-font-style-tt">a</span>" has the index $1$, and the letter "<span class="tex-font-style-tt">t</span>" has the index $20$.</p><p>However, this encoding turned out to be ambiguous! For example, when encoding the word "<span class="tex-font-style-tt">ava</span>", the integer $1 + 22 + 1 = 24$ is also obtained.</p><p>Determine the lexicographically smallest word of $3$ letters that could have been encoded.</p><p>A string $a$ is lexicographically smaller than a string $b$ if and only if one of the following holds:</p><ul><li> $a$ is a prefix of $b$, but $a \ne b$;</li><li> in the first position where $a$ and $b$ differ, the string $a$ has a letter that appears earlier in the alphabet than the corresponding letter in $b$.</li></ul></div><div class="input-specification"><p>The first line of the input contains a single integer $t$ ($1 \le t \le 100$)&nbsp;— the number of test cases in the test.</p><p>This is followed by the descriptions of the test cases.</p><p>The first and only line of each test case contains an integer $n$ ($3 \le n \le 78$) — the encoded word.</p></div><div class="output-specification"><p>For each test case, output the lexicographically smallest three-letter word that could have been encoded on a separate line.</p></div>

## Input

<p>The first line of the input contains a single integer $t$ ($1 \le t \le 100$)&nbsp;— the number of test cases in the test.</p><p>This is followed by the descriptions of the test cases.</p><p>The first and only line of each test case contains an integer $n$ ($3 \le n \le 78$) — the encoded word.</p>

## Output

<p>For each test case, output the lexicographically smallest three-letter word that could have been encoded on a separate line.</p>





```input1|2,4,6
5
24
70
3
55
48
```




```output1
aav
rzz
aaa
czz
auz
```


