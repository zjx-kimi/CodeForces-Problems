## Description

<div><p>Given a string $x$ of length $n$ and a string $s$ of length $m$ ($n \cdot m \le 25$), consisting of lowercase Latin letters, you can apply any number of operations to the string $x$.</p><p>In one operation, you append the current value of $x$ to the end of the string $x$. Note that the value of $x$ will change after this.</p><p>For example, if $x =$"<span class="tex-font-style-tt">aba</span>", then after applying operations, $x$ will change as follows: "<span class="tex-font-style-tt">aba</span>" $\rightarrow$ "<span class="tex-font-style-tt">abaaba</span>" $\rightarrow$ "<span class="tex-font-style-tt">abaabaabaaba</span>".</p><p>After what <span class="tex-font-style-bf">minimum</span> number of operations $s$ will appear in $x$ as a substring? A substring of a string is defined as a <span class="tex-font-style-bf">contiguous</span> segment of it.</p></div><div class="input-specification"><p>The first line of the input contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains two numbers $n$ and $m$ ($1 \le n \cdot m \le 25$)&nbsp;— the lengths of strings $x$ and $s$, respectively.</p><p>The second line of each test case contains the string $x$ of length $n$.</p><p>The third line of each test case contains the string $s$ of length $m$.</p></div><div class="output-specification"><p>For each test case, output a single number&nbsp;— the <span class="tex-font-style-bf">minimum</span> number of operations after which $s$ will appear in $x$ as a substring. If this is not possible, output $-1$.</p></div>

## Input

<p>The first line of the input contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains two numbers $n$ and $m$ ($1 \le n \cdot m \le 25$)&nbsp;— the lengths of strings $x$ and $s$, respectively.</p><p>The second line of each test case contains the string $x$ of length $n$.</p><p>The third line of each test case contains the string $s$ of length $m$.</p>

## Output

<p>For each test case, output a single number&nbsp;— the <span class="tex-font-style-bf">minimum</span> number of operations after which $s$ will appear in $x$ as a substring. If this is not possible, output $-1$.</p>





```input1|2,3,4,8,9,10,14,15,16,20,21,22,26,27,28,32,33,34
12
1 5
a
aaaaa
5 5
eforc
force
2 5
ab
ababa
3 5
aba
ababa
4 3
babb
bbb
5 1
aaaaa
a
4 2
aabb
ba
2 8
bk
kbkbkbkb
12 2
fjdgmujlcont
tf
2 2
aa
aa
3 5
abb
babba
1 19
m
mmmmmmmmmmmmmmmmmmm
```




```output1
3
1
2
-1
1
0
1
3
1
0
2
5
```



## Note

<p>In the first test case of the example, after $2$ operations, the string will become "<span class="tex-font-style-tt">aaaa</span>", and after $3$ operations, it will become "<span class="tex-font-style-tt">aaaaaaaa</span>", so the answer is $3$.</p><p>In the second test case of the example, after applying $1$ operation, the string will become "$\text{e}\color{red}{\text{force}}\text{forc}$", where the substring is highlighted in red.</p><p>In the fourth test case of the example, it can be shown that it is impossible to obtain the desired string as a substring.</p>
