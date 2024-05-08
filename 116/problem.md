## Description

<div><p>Consider the following problem.</p><p>You are given a string $s$, consisting of $n$ lowercase Latin letters, and an integer $k$ ($n$ is not divisible by $k$). Each letter is one of the first $c$ letters of the alphabet.</p><p>You apply the following operation until the length of the string is less than $k$: choose a contiguous substring of the string of length exactly $k$, remove it from the string and glue the resulting parts together without changing the order.</p><p>Let the resulting string of length smaller than $k$ be $t$. What is lexicographically smallest string $t$ that can obtained?</p><p>You are asked the inverse of this problem. Given two integers $n$ and $k$ ($n$ is not divisible by $k$) and a string $t$, consisting of ($n \bmod k$) lowercase Latin letters, count the number of strings $s$ that produce $t$ as the lexicographically smallest solution.</p><p>Print that number modulo $998\,244\,353$.</p></div><div class="input-specification"><p>The first line contains three integers $n, k$ and $c$ ($1 \le n \le 10^6$; $2 \le k \le 10^6$; $1 \le c \le 26$; $n$ is not divisible by $k$)&nbsp;— the length of string $s$, the length of the substring that is being removed and the number of first letters from the alphabet.</p><p>The second line contains string $t$, consisting of exactly ($n \bmod k$) lowercase Latin letters. Each letter is one of the first $c$ letters of the alphabet.</p></div><div class="output-specification"><p>Print a single integer&nbsp;— the number of strings $s$ that produce $t$ as the lexicographically smallest solution.</p></div>

## Input

<p>The first line contains three integers $n, k$ and $c$ ($1 \le n \le 10^6$; $2 \le k \le 10^6$; $1 \le c \le 26$; $n$ is not divisible by $k$)&nbsp;— the length of string $s$, the length of the substring that is being removed and the number of first letters from the alphabet.</p><p>The second line contains string $t$, consisting of exactly ($n \bmod k$) lowercase Latin letters. Each letter is one of the first $c$ letters of the alphabet.</p>

## Output

<p>Print a single integer&nbsp;— the number of strings $s$ that produce $t$ as the lexicographically smallest solution.</p>





```input1
3 2 2
a
```




```input2
5 3 3
bc
```




```input3
34 12 26
codeforces
```




```input4
5 3 1
aa
```




```output1
6
```




```output2
15
```




```output3
988024123
```




```output4
1
```



## Note

<p>The strings $s$ in the first example: "<span class="tex-font-style-tt">aaa</span>", "<span class="tex-font-style-tt">aab</span>", "<span class="tex-font-style-tt">aba</span>", "<span class="tex-font-style-tt">abb</span>", "<span class="tex-font-style-tt">baa</span>", "<span class="tex-font-style-tt">bba</span>".</p><p>The strings $s$ in the second example: "<span class="tex-font-style-tt">bcabc</span>", "<span class="tex-font-style-tt">bcacc</span>", "<span class="tex-font-style-tt">bcbbc</span>", "<span class="tex-font-style-tt">bcbcc</span>", "<span class="tex-font-style-tt">bccbc</span>", "<span class="tex-font-style-tt">bcccc</span>", "<span class="tex-font-style-tt">caabc</span>", "<span class="tex-font-style-tt">cabbc</span>", "<span class="tex-font-style-tt">cacbc</span>", "<span class="tex-font-style-tt">cbabc</span>", "<span class="tex-font-style-tt">cbbbc</span>", "<span class="tex-font-style-tt">cbcbc</span>", "<span class="tex-font-style-tt">ccabc</span>", "<span class="tex-font-style-tt">ccbbc</span>", "<span class="tex-font-style-tt">cccbc</span>".</p>
