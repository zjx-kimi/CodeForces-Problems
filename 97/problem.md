## Description

<div><p>You are given a string $s$ of length $n$, consisting of lowercase Latin letters.</p><p>You are allowed to replace at most one character in the string with an arbitrary lowercase Latin letter.</p><p>Print the lexicographically minimal string that can be obtained from the original string and contains the maximum number of palindromes as substrings. Note that if a palindrome appears more than once as a substring, it is counted the same number of times it appears.</p><p>The string $a$ is lexicographically smaller than the string $b$ if and only if one of the following holds: </p><ul> <li> $a$ is a prefix of $b$, but $a \ne b$; </li><li> in the first position where $a$ and $b$ are different, the string $a$ contains a letter that appears earlier in the alphabet than the corresponding letter in $b$. </li></ul></div><div class="input-specification"><p>The first line contains one integer $n$ ($1 \leq n \leq 3 \cdot 10^5$)&nbsp;— the number of characters in the string.</p><p>The second line contains the string $s$ itself, consisting of exactly $n$ lowercase Latin letters.</p></div><div class="output-specification"><p>In the first line, print one integer — the maximum number of palindromic substrings that can be obtained using the operation described in the statement at most once.</p><p>In the second line, print the string that can be obtained from $s$ and has the maximum possible number of palindromic substrings. If there are multiple answers, print the lexicographically smallest one.</p></div>

## Input

<p>The first line contains one integer $n$ ($1 \leq n \leq 3 \cdot 10^5$)&nbsp;— the number of characters in the string.</p><p>The second line contains the string $s$ itself, consisting of exactly $n$ lowercase Latin letters.</p>

## Output

<p>In the first line, print one integer — the maximum number of palindromic substrings that can be obtained using the operation described in the statement at most once.</p><p>In the second line, print the string that can be obtained from $s$ and has the maximum possible number of palindromic substrings. If there are multiple answers, print the lexicographically smallest one.</p>





```input1|
5
aabaa
```




```input2|
5
aaaaa
```




```input3|
4
awoo
```




```output1
15
aaaaa
```




```output2
15
aaaaa
```




```output3
7
aooo
```


