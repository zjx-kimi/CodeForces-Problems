## Description

<div><p>Bogocubic is playing a game with amenotiomoi. First, Bogocubic fixed an integer $n$, and then he gave amenotiomoi an integer $x$ which is initially equal to $1$.</p><p>In one move amenotiomoi performs <span class="tex-font-style-bf">one</span> of the following operations with the same probability:</p><ul> <li> increase $x$ by $1$; </li><li> multiply $x$ by $2$. </li></ul><p>Bogocubic wants to find the expected number of moves amenotiomoi has to do to make $x$ greater than or equal to $n$. Help him find this number modulo $998\,244\,353$.</p><p>Formally, let $M = 998\,244\,353$. It can be shown that the answer can be expressed as an irreducible fraction $\frac{p}{q}$, where $p$ and $q$ are integers and $q \not \equiv 0 \pmod{M}$. Output the integer equal to $p \cdot q^{-1} \bmod M$. In other words, output such an integer $y$ that $0 \le y &lt; M$ and $y \cdot q \equiv p \pmod{M}$.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 100$). The description of the test cases follows.</p><p>The only line of each test case contains one integer $n$ ($1 \le n \le 10^{18}$).</p></div><div class="output-specification"><p>For each test case, output a single integer&nbsp;— the expected number of moves modulo $998\,244\,353$.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 100$). The description of the test cases follows.</p><p>The only line of each test case contains one integer $n$ ($1 \le n \le 10^{18}$).</p>

## Output

<p>For each test case, output a single integer&nbsp;— the expected number of moves modulo $998\,244\,353$.</p>





```input1|2,4,6,8
7
1
4
8
15
998244353
296574916252563317
494288321850420024
```




```output1
0
499122179
717488133
900515847
93715054
44488799
520723508
```



## Note

<p>In the first test case, $n\le x$ without any operations, so the answer is $0$.</p><p>In the second test case, for $n = 4$, here is the list of all possible sequences of operations and their probabilities:</p><ul> <li> $1\stackrel{+1}{\longrightarrow}2\stackrel{+1}{\longrightarrow}3\stackrel{+1}{\longrightarrow}4$, the probability is $\frac{1}{8}$; </li><li> $1\stackrel{\times 2}{\longrightarrow}2\stackrel{+1}{\longrightarrow}3\stackrel{+1}{\longrightarrow}4$, the probability is $\frac{1}{8}$; </li><li> $1\stackrel{+1}{\longrightarrow}2\stackrel{+1}{\longrightarrow}3\stackrel{\times 2}{\longrightarrow}6$, the probability is $\frac{1}{8}$; </li><li> $1\stackrel{\times 2}{\longrightarrow}2\stackrel{+1}{\longrightarrow}3\stackrel{\times 2}{\longrightarrow}6$, the probability is $\frac{1}{8}$; </li><li> $1\stackrel{+1}{\longrightarrow}2\stackrel{\times 2}{\longrightarrow}4$, the probability is $\frac{1}{4}$; </li><li> $1\stackrel{\times 2}{\longrightarrow}2\stackrel{\times 2}{\longrightarrow}4$, the probability is $\frac{1}{4}$. </li></ul><p>So the expected number of moves is $4 \cdot \left(3 \cdot \frac{1}{8}\right) + 2 \cdot \left(2 \cdot \frac{1}{4} \right) =\frac{5}{2} \equiv 499122179 \pmod{998244353}$. </p><p>In the third test case, for $n = 8$, the expected number of moves is $\frac{137}{32}\equiv 717488133\pmod{998244353}$. </p><p>In the fourth test case, for $n = 15$, the expected number of moves is $\frac{24977}{4096} \equiv 900515847 \pmod{998244353}$. </p>
