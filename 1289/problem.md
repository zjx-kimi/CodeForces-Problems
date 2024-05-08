## Description

<div><p>A transformation of an array of positive integers $a_1,a_2,\dots,a_n$ is defined by replacing $a$ with the array $b_1,b_2,\dots,b_n$ given by $b_i=a_i\oplus a_{(i\bmod n)+1}$, where $\oplus$ denotes the bitwise XOR operation.</p><p>You are given integers $n$, $t$, and $w$. We consider an array $c_1,c_2,\dots,c_n$ ($0 \le c_i \le 2^w-1$) to be <span class="tex-font-style-it">bugaboo</span> if and only if there exists an array $a_1,a_2,\dots,a_n$ such that after transforming $a$ for $t$ times, $a$ becomes $c$.</p><p>For example, when $n=6$, $t=2$, $w=2$, then the array $[3,2,1,0,2,2]$ is bugaboo because it can be given by transforming the array $[2,3,1,1,0,1]$ for $2$ times:</p><p>$$ [2,3,1,1,0,1]\to [2\oplus 3,3\oplus 1,1\oplus 1,1\oplus 0,0\oplus 1,1\oplus 2]=[1,2,0,1,1,3]; \\ [1,2,0,1,1,3]\to [1\oplus 2,2\oplus 0,0\oplus 1,1\oplus 1,1\oplus 3,3\oplus 1]=[3,2,1,0,2,2]. $$</p><p>And the array $[4,4,4,4,0,0]$ is not bugaboo because $4 &gt; 2^2 - 1$. The array $[2,3,3,3,3,3]$ is also not bugaboo because it can't be given by transforming one array for $2$ times.</p><p>You are given an array $c$ with some positions lost (only $m$ positions are known at first and the remaining positions are lost). And there are $q$ modifications, where each modification is changing a position of $c$. A modification can possibly change whether the position is lost or known, and it can possibly redefine a position that is already given.</p><p>You need to calculate how many possible arrays $c$ (with arbitrary elements on the lost positions) are bugaboos after each modification. Output the $i$-th answer modulo $p_i$ ($p_i$ is a given array consisting of $q$ elements).</p></div><div class="input-specification"><p>The first line contains four integers $n$, $m$, $t$ and $w$ ($2\le n\le 10^7$, $0\le m\le \min(n, 10^5)$, $1\le t\le 10^9$, $1\le w\le 30$).</p><p>The $i$-th line of the following $m$ lines contains two integers $d_i$ and $e_i$ ($1\le d_i\le n$, $0\le e_i&lt; 2^w$). It means the position $d_i$ of the array $c$ is given and $c_{d_i}=e_i$. It is guaranteed that $1\le d_1&lt;d_2&lt;\ldots&lt;d_m\le n$.</p><p>The next line contains only one number $q$ ($1\le q\le 10^5$)&nbsp;— the number of modifications.</p><p>The $i$-th line of the following $q$ lines contains three integers $f_i$, $g_i$, $p_i$ ($1\le f_i\le n$, $-1\le g_i&lt; 2^w$, $11\le p_i\le 10^9+7$). The value $g_i=-1$ means changing the position $f_i$ of the array $c$ to a lost position, otherwise it means changing the position $f_i$ of the array $c$ to a known position, and $c_{f_i}=g_i$. The value $p_i$ means you need to output the $i$-th answer modulo $p_i$.</p></div><div class="output-specification"><p>The output contains $q$ lines, denoting your answers.</p></div>

## Input

<p>The first line contains four integers $n$, $m$, $t$ and $w$ ($2\le n\le 10^7$, $0\le m\le \min(n, 10^5)$, $1\le t\le 10^9$, $1\le w\le 30$).</p><p>The $i$-th line of the following $m$ lines contains two integers $d_i$ and $e_i$ ($1\le d_i\le n$, $0\le e_i&lt; 2^w$). It means the position $d_i$ of the array $c$ is given and $c_{d_i}=e_i$. It is guaranteed that $1\le d_1&lt;d_2&lt;\ldots&lt;d_m\le n$.</p><p>The next line contains only one number $q$ ($1\le q\le 10^5$)&nbsp;— the number of modifications.</p><p>The $i$-th line of the following $q$ lines contains three integers $f_i$, $g_i$, $p_i$ ($1\le f_i\le n$, $-1\le g_i&lt; 2^w$, $11\le p_i\le 10^9+7$). The value $g_i=-1$ means changing the position $f_i$ of the array $c$ to a lost position, otherwise it means changing the position $f_i$ of the array $c$ to a known position, and $c_{f_i}=g_i$. The value $p_i$ means you need to output the $i$-th answer modulo $p_i$.</p>

## Output

<p>The output contains $q$ lines, denoting your answers.</p>





```input1
3 2 1 1
1 1
3 1
4
2 0 123456789
2 1 111111111
1 -1 987654321
3 -1 555555555
```




```input2
24 8 5 4
4 4
6 12
8 12
15 11
16 7
20 2
21 9
22 12
13
2 13 11
3 15 12
5 7 13
9 3 14
10 5 15
11 15 16
13 14 17
14 1 18
18 9 19
19 6 20
23 10 21
24 8 22
21 13 23
```




```output1
1
0
1
2
```




```output2
1
4
9
2
1
0
1
10
11
16
16
0
16
```



## Note

<p>In the first example, $n=3$, $t=1$, and $w=1$. Let $?$ denote a lost position of $c$.</p><p>In the first query, $c=[1,0,1]$. The only possible array $[1,0,1]$ is bugaboo because it can be given by transforming $[0,1,1]$ once. So the answer is $1\bmod 123\,456\,789 = 1$.</p><p>In the second query, $c=[1,1,1]$. The only possible array $[1,1,1]$ is not bugaboo. So the answer is $0\bmod 111\,111\,111 = 0$.</p><p>In the third query, $c=[?,1,1]$. There are two possible arrays $[1,1,1]$ and $[0,1,1]$. Only $[0,1,1]$ is bugaboo because it can be given by transforming $[1,1,0]$ once. So the answer is $1\bmod 987\,654\,321=1$.</p><p>In the fourth query, $c=[?,1,?]$. There are four possible arrays. $[0,1,1]$ and $[1,1,0]$ are bugaboos. $[1,1,0]$ can be given by performing $[1,0,1]$ once. So the answer is $2\bmod 555\,555\,555=2$.</p>
