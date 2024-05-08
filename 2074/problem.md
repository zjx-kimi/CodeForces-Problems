## Description

<div><div class="epigraph"><div class="epigraph-text"><span class="tex-font-size-small"> Frodo was caught by Saruman. He tore a pouch from Frodo's neck, shook out its contents&nbsp;—there was a pile of different rings: gold and silver...<p>"How am I to tell which is the One?!" the mage howled.</p><p>"Throw them one by one into the Cracks of Doom and watch when Mordor falls!" </p></span></div></div><p>Somewhere in a parallel Middle-earth, when Saruman caught Frodo, he only found $n$ rings. And the $i$-th ring was either gold or silver. For convenience Saruman wrote down a binary string $s$ of $n$ characters, where the $i$-th character was <span class="tex-font-style-tt">0</span> if the $i$-th ring was gold, and <span class="tex-font-style-tt">1</span> if it was silver.</p><p>Saruman has a magic function $f$, which takes a binary string and returns a number obtained by converting the string into a binary number and then converting the binary number into a decimal number. For example, $f(001010) = 10, f(111) = 7, f(11011101) = 221$.</p><p>Saruman, however, thinks that the order of the rings plays some important role. He wants to find $2$ pairs of integers $(l_1, r_1), (l_2, r_2)$, such that:</p><ul><li> $1 \le l_1 \le n$, $1 \le r_1 \le n$, $r_1-l_1+1\ge \lfloor \frac{n}{2} \rfloor$ </li><li> $1 \le l_2 \le n$, $1 \le r_2 \le n$, $r_2-l_2+1\ge \lfloor \frac{n}{2} \rfloor$ </li><li> Pairs $(l_1, r_1)$ and $(l_2, r_2)$ are distinct. That is, at least one of $l_1 \neq l_2$ and $r_1 \neq r_2$ must hold.</li><li> Let $t$ be the substring $s[l_1:r_1]$ of $s$, and $w$ be the substring $s[l_2:r_2]$ of $s$. Then <span class="tex-font-style-bf">there exists non-negative integer $k$, such that $f(t) = f(w) \cdot k$.</span></li></ul><p>Here substring $s[l:r]$ denotes $s_ls_{l+1}\ldots s_{r-1}s_r$, and $\lfloor x \rfloor$ denotes rounding the number down to the nearest integer.</p><p>Help Saruman solve this problem! It is guaranteed that under the constraints of the problem at least one solution exists.</p></div><div class="input-specification"><p>Each test contains multiple test cases.</p><p>The first line contains one positive integer $t$ ($1 \le t \le 10^3$), denoting the number of test cases. Description of the test cases follows.</p><p>The first line of each test case contains one positive integer $n$ ($2 \le n \le 2 \cdot 10^4$)&nbsp;— length of the string.</p><p>The second line of each test case contains a non-empty binary string of length $n$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p></div><div class="output-specification"><p>For every test case print four integers $l_1$, $r_1$, $l_2$, $r_2$, which denote the beginning of the first substring, the end of the first substring, the beginning of the second substring, and the end of the second substring, respectively.</p><p>If there are multiple solutions, print any.</p></div>

## Input

<p>Each test contains multiple test cases.</p><p>The first line contains one positive integer $t$ ($1 \le t \le 10^3$), denoting the number of test cases. Description of the test cases follows.</p><p>The first line of each test case contains one positive integer $n$ ($2 \le n \le 2 \cdot 10^4$)&nbsp;— length of the string.</p><p>The second line of each test case contains a non-empty binary string of length $n$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p>

## Output

<p>For every test case print four integers $l_1$, $r_1$, $l_2$, $r_2$, which denote the beginning of the first substring, the end of the first substring, the beginning of the second substring, and the end of the second substring, respectively.</p><p>If there are multiple solutions, print any.</p>





```input1
7
6
101111
9
111000111
8
10000000
5
11011
6
001111
3
101
30
100000000000000100000000000000
```




```output1
3 6 1 3
1 9 4 9
5 8 1 4
1 5 3 5
1 6 2 4
1 2 2 3
1 15 16 30
```



## Note

<p>In the first testcase $f(t) = f(1111) = 15$, $f(w) = f(101) = 5$.</p><p>In the second testcase $f(t) = f(111000111) = 455$, $f(w) = f(000111) = 7$.</p><p>In the third testcase $f(t) = f(0000) = 0$, $f(w) = f(1000) = 8$.</p><p>In the fourth testcase $f(t) = f(11011) = 27$, $f(w) = f(011) = 3$.</p><p>In the fifth testcase $f(t) = f(001111) = 15$, $f(w) = f(011) = 3$.</p>
