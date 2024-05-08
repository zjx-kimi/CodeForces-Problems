## Description

<div><p>You're going to generate an array $a$ with a length of at most $n$, where each $a_{i}$ equals either $1$ or $-1$.</p><p>You generate this array in the following way. </p><ul> <li> First, you choose some integer $k$ ($1\le k \le n$), which decides the length of $a$. </li><li> Then, for each $i$ ($1\le i \le k$), you set $a_{i} = 1$ with probability $p_{i}$, otherwise set $a_{i} = -1$ (with probability $1 - p_{i}$). </li></ul><p>After the array is generated, you calculate $s_{i} = a_{1} + a_{2} + a_{3}+ \ldots + a_{i}$. Specially, $s_{0} = 0$. Then you let $S$ equal to $\displaystyle \max_{i=0}^{k}{s_{i}}$. That is, $S$ is the maximum prefix sum of the array $a$.</p><p>You are given $n+1$ integers $h_{0} , h_{1}, \ldots ,h_{n}$. The <span class="tex-font-style-it">score</span> of an array $a$ with maximum prefix sum $S$ is $h_{S}$. Now, for each $k$, you want to know the expected score for an array of length $k$ modulo $10^9+7$.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 5000$) — the number of test cases. Their description follows.</p><p>The first line contains an integer $n$ ($1\le n \le 5000$).</p><p>Then for the following $n$ lines, each line contains two integers $x_{i}$ and $y_{i}$ ($0 \le x_{i} &lt; 10^9 + 7$, $1\le y_{i} &lt; 10^9 + 7$, $x_{i} \le y_{i}$), indicating $p_{i} = \frac{x_{i}}{y_{i}}$.</p><p>The next line contains $n+1$ integers $h_{0},h_{1}, \ldots, h_{n}$ ($0 \le h_{i} &lt; 10^9 + 7$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $5000$.</p></div><div class="output-specification"><p>For each test case, output $n$ integers in one single line, the $i$-th of which denotes the expected score for an array of length $i$, modulo $10^9 + 7$.</p><p>Formally, let $M = 10^9 + 7$. It can be shown that the answer can be expressed as an irreducible fraction $\frac{p}{q}$, where $p$ and $q$ are integers and $q \not \equiv 0 \pmod{M}$. Output the integer equal to $p \cdot q^{-1} \bmod M$. In other words, output such an integer $x$ that $0 \le x &lt; M$ and $x \cdot q \equiv p \pmod{M}$.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 5000$) — the number of test cases. Their description follows.</p><p>The first line contains an integer $n$ ($1\le n \le 5000$).</p><p>Then for the following $n$ lines, each line contains two integers $x_{i}$ and $y_{i}$ ($0 \le x_{i} &lt; 10^9 + 7$, $1\le y_{i} &lt; 10^9 + 7$, $x_{i} \le y_{i}$), indicating $p_{i} = \frac{x_{i}}{y_{i}}$.</p><p>The next line contains $n+1$ integers $h_{0},h_{1}, \ldots, h_{n}$ ($0 \le h_{i} &lt; 10^9 + 7$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $5000$.</p>

## Output

<p>For each test case, output $n$ integers in one single line, the $i$-th of which denotes the expected score for an array of length $i$, modulo $10^9 + 7$.</p><p>Formally, let $M = 10^9 + 7$. It can be shown that the answer can be expressed as an irreducible fraction $\frac{p}{q}$, where $p$ and $q$ are integers and $q \not \equiv 0 \pmod{M}$. Output the integer equal to $p \cdot q^{-1} \bmod M$. In other words, output such an integer $x$ that $0 \le x &lt; M$ and $x \cdot q \equiv p \pmod{M}$.</p>





```input1|2,3,4,5,11,12,13,14,15
4
2
1 2
1 2
1 2 3
3
1 3
1 4
5 5
1 1 1 1
3
2 5
4 6
0 2
4 3 2 1
5
5 6
5 7
1 6
1 3
4 7
9 0 4 5 2 4
```




```output1
500000005 750000007 
1 1 1 
200000005 333333339 333333339 
500000005 880952391 801587311 781746041 789304620
```



## Note

<p>In the first test case, if we choose $k=1$, there are $2$ possible arrays with equal probabilities: $[1]$ and $[-1]$. The $S$ values for them are $1$ and $0$. So the expected score is $\frac{1}{2}h_{0} + \frac{1}{2}h_{1} = \frac{3}{2}$. If we choose $k=2$, there are $4$ possible arrays with equal probabilities: $[1,1]$, $[1,-1]$, $[-1,1]$, $[-1,-1]$, and the $S$ values for them are $2,1,0,0$. So the expected score is $\frac{1}{2}h_{0} + \frac{1}{4}h_{1} + \frac{1}{4}h_{2} = \frac{7}{4}$.</p><p>In the second test case, no matter what the $S$ value is, the score is always $1$, so the expected score is always $1$.</p>
