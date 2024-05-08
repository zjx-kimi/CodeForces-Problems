## Description

<div><p>There is a string $a$ (unknown to you), consisting of lowercase Latin letters, encrypted according to the following rule into string $s$:</p><ul> <li> after each character of string $a$, an arbitrary (possibly zero) number of any lowercase Latin letters, different from the character itself, is added; </li><li> after each such addition, the character that we supplemented is added. </li></ul><p>You are given string $s$, and you need to output the initial string $a$. In other words, you need to decrypt string $s$.</p><p>Note that each string encrypted in this way is decrypted <span class="tex-font-style-bf">uniquely</span>.</p></div><div class="input-specification"><p>The first line of the input contains a single integer $t$ ($1 \le t \le 1000$)&nbsp;— the number of test cases.</p><p>The descriptions of the test cases follow.</p><p>The first line of each test case contains a single integer $n$ ($2 \le n \le 100$)&nbsp;— the length of the encrypted message.</p><p>The second line of each test case contains a string $s$ of length $n$&nbsp;— the encrypted message obtained from some string $a$.</p></div><div class="output-specification"><p>For each test case, output the decrypted message $a$ on a separate line.</p></div>

## Input

<p>The first line of the input contains a single integer $t$ ($1 \le t \le 1000$)&nbsp;— the number of test cases.</p><p>The descriptions of the test cases follow.</p><p>The first line of each test case contains a single integer $n$ ($2 \le n \le 100$)&nbsp;— the length of the encrypted message.</p><p>The second line of each test case contains a string $s$ of length $n$&nbsp;— the encrypted message obtained from some string $a$.</p>

## Output

<p>For each test case, output the decrypted message $a$ on a separate line.</p>





```input1|2,3,6,7
3
8
abacabac
5
qzxcq
20
ccooddeeffoorrcceess
```




```output1
ac
q
codeforces
```



## Note

<p>In the first encrypted message, the letter $a$ is encrypted as $aba$, and the letter $c$ is encrypted as $cabac$.</p><p>In the second encrypted message, only one letter $q$ is encrypted as $qzxcq$.</p><p>In the third encrypted message, zero characters are added to each letter.</p>
