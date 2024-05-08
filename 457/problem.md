## Description

<div><p>Lisa was kidnapped by martians! It okay, because she has watched a lot of TV shows about aliens, so she knows what awaits her. Let's call integer <span class="tex-font-style-it">martian</span> if it is <span class="tex-font-style-bf">a non-negative integer</span> and <span class="tex-font-style-bf">strictly less than</span> $2^k$, for example, when $k = 12$, the numbers $51$, $1960$, $0$ are <span class="tex-font-style-it">martian</span>, and the numbers $\pi$, $-1$, $\frac{21}{8}$, $4096$ are not.</p><p>The aliens will give Lisa $n$ <span class="tex-font-style-it">martian</span> numbers $a_1, a_2, \ldots, a_n$. Then they will ask her to name any <span class="tex-font-style-it">martian</span> number $x$. After that, Lisa will select a pair of numbers $a_i, a_j$ ($i \neq j$) in the given sequence and count $(a_i \oplus x) \&amp; (a_j \oplus x)$. The operation $\oplus$ means <a href="http://tiny.cc/xor_wiki">Bitwise exclusive OR</a>, the operation $\&amp;$ means <a href="http://tiny.cc/and_wiki ">Bitwise And</a>. For example, $(5 \oplus 17) \&amp; (23 \oplus 17) = (00101_2 \oplus 10001_2) \&amp; (10111_2 \oplus 10001_2) = 10100_2 \&amp; 00110_2 = 00100_2 = 4$.</p><p>Lisa is sure that the higher the calculated value, the higher her chances of returning home. Help the girl choose such $i, j, x$ that maximize the calculated value.</p></div><div class="input-specification"><p>The first line contains an integer $t$ ($1 \le t \le 10^4$)&nbsp;— number of testcases.</p><p>Each testcase is described by two lines.</p><p>The first line contains integers $n, k$ ($2 \le n \le 2 \cdot 10^5$, $1 \le k \le 30$)&nbsp;— the length of the sequence of <span class="tex-font-style-it">martian</span> numbers and the value of $k$.</p><p>The second line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($0 \le a_i &lt; 2^k$)&nbsp;— a sequence of <span class="tex-font-style-it">martian</span> numbers.</p><p>It is guaranteed that the sum of $n$ over all testcases <span class="tex-font-style-bf">does not exceed</span> $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each testcase, print three integers $i, j, x$ ($1 \le i, j \le n$, $i \neq j$, $0 \le x &lt; 2^k$). The value of $(a_i \oplus x) \&amp; (a_j \oplus x)$ should be the maximum possible.</p><p>If there are several solutions, you can print any one.</p></div>

## Input

<p>The first line contains an integer $t$ ($1 \le t \le 10^4$)&nbsp;— number of testcases.</p><p>Each testcase is described by two lines.</p><p>The first line contains integers $n, k$ ($2 \le n \le 2 \cdot 10^5$, $1 \le k \le 30$)&nbsp;— the length of the sequence of <span class="tex-font-style-it">martian</span> numbers and the value of $k$.</p><p>The second line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($0 \le a_i &lt; 2^k$)&nbsp;— a sequence of <span class="tex-font-style-it">martian</span> numbers.</p><p>It is guaranteed that the sum of $n$ over all testcases <span class="tex-font-style-bf">does not exceed</span> $2 \cdot 10^5$.</p>

## Output

<p>For each testcase, print three integers $i, j, x$ ($1 \le i, j \le n$, $i \neq j$, $0 \le x &lt; 2^k$). The value of $(a_i \oplus x) \&amp; (a_j \oplus x)$ should be the maximum possible.</p><p>If there are several solutions, you can print any one.</p>





```input1|2,3,6,7,10,11,14,15,18,19
10
5 4
3 9 1 4 13
3 1
1 0 1
6 12
144 1580 1024 100 9 13
4 3
7 3 0 4
3 2
0 0 1
2 4
12 2
9 4
6 14 9 4 4 4 5 10 2
2 1
1 0
2 4
11 4
9 4
2 11 10 1 6 9 11 0 5
```




```output1
1 3 14
1 3 0
5 6 4082
2 3 7
1 2 3
1 2 15
4 5 11
1 2 0
1 2 0
2 7 4
```



## Note

<p>First testcase: $(3 \oplus 14) \&amp; (1 \oplus 14) = (0011_2 \oplus 1110_2) \&amp; (0001_2 \oplus 1110_2) = 1101_2 = 1101_2 \&amp; 1111_2 = 1101_2 = 13$.</p><p>Second testcase: $(1 \oplus 0) \&amp; (1 \oplus 0) = 1$.</p><p>Third testcase: $(9 \oplus 4082) \&amp; (13 \oplus 4082) = 4091$.</p><p>Fourth testcase: $(3 \oplus 7) \&amp; (0 \oplus 7) = 4$.</p>
