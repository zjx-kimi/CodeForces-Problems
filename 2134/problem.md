## Description

<div><p>A string $s$ of length $n$, consisting of lowercase letters of the English alphabet, is given.</p><p>You must choose some number $k$ between $0$ and $n$. Then, you select $k$ characters of $s$ and permute them however you want. In this process, the positions of the other $n-k$ characters remain unchanged. You have to perform this operation exactly once.</p><p>For example, if $s=\texttt{"andrea"}$, you can choose the $k=4$ characters $\texttt{"a_d_ea"}$ and permute them into $\texttt{"d_e_aa"}$ so that after the operation the string becomes $\texttt{"dneraa"}$.</p><p>Determine the minimum $k$ so that it is possible to sort $s$ alphabetically (that is, after the operation its characters appear in alphabetical order).</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 1000$) — the number of test cases. Then $t$ test cases follow.</p><p>The first line of each test case contains one integer $n$ ($1 \le n \le 40$) — the length of the string.</p><p>The second line of each test case contains the string $s$. It is guaranteed that $s$ contains only lowercase letters of the English alphabet.</p></div><div class="output-specification"><p>For each test case, output the minimum $k$ that allows you to obtain a string sorted alphabetically, through the operation described above.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 1000$) — the number of test cases. Then $t$ test cases follow.</p><p>The first line of each test case contains one integer $n$ ($1 \le n \le 40$) — the length of the string.</p><p>The second line of each test case contains the string $s$. It is guaranteed that $s$ contains only lowercase letters of the English alphabet.</p>

## Output

<p>For each test case, output the minimum $k$ that allows you to obtain a string sorted alphabetically, through the operation described above.</p>





```input1
4
3
lol
10
codeforces
5
aaaaa
4
dcba
```




```output1
2
6
0
4
```



## Note

<p>In the <span class="tex-font-style-bf">first test case</span>, we can choose the $k=2$ characters $\texttt{"_ol"}$ and rearrange them as $\texttt{"_lo"}$ (so the resulting string is $\texttt{"llo"}$). It is not possible to sort the string choosing strictly less than $2$ characters.</p><p>In the <span class="tex-font-style-bf">second test case</span>, one possible way to sort $s$ is to consider the $k=6$ characters $\texttt{"_o__force_"}$ and rearrange them as $\texttt{"_c__efoor_"}$ (so the resulting string is $\texttt{"ccdeefoors"}$). One can show that it is not possible to sort the string choosing strictly less than $6$ characters.</p><p>In the <span class="tex-font-style-bf">third test case</span>, string $s$ is already sorted (so we can choose $k=0$ characters).</p><p>In the <span class="tex-font-style-bf">fourth test case</span>, we can choose all $k=4$ characters $\texttt{"dcba"}$ and reverse the whole string (so the resulting string is $\texttt{"abcd"}$).</p>
