## Description

<div><p>Recall that the binomial coefficient $\binom{x}{y}$ is calculated as follows ($x$ and $y$ are non-negative integers):</p><ul> <li> if $x &lt; y$, then $\binom{x}{y} = 0$; </li><li> otherwise, $\binom{x}{y} = \frac{x!}{y! \cdot (x-y)!}$. </li></ul><p>You are given an array $a_1, a_2, \dots, a_n$ and an integer $k$. You have to calculate a new array $b_1, b_2, \dots, b_n$, where</p><ul> <li> $b_1 = (\binom{1}{k} \cdot a_1) \bmod 998244353$; </li><li> $b_2 = (\binom{2}{k} \cdot a_1 + \binom{1}{k} \cdot a_2) \bmod 998244353$; </li><li> $b_3 = (\binom{3}{k} \cdot a_1 + \binom{2}{k} \cdot a_2 + \binom{1}{k} \cdot a_3) \bmod 998244353$, and so on. </li></ul><p>Formally, $b_i = (\sum\limits_{j=1}^{i} \binom{i - j + 1}{k} \cdot a_j) \bmod 998244353$.</p><p><span class="tex-font-style-bf">Note that the array is given in a modified way, and you have to output it in a modified way as well</span>.</p></div><div class="input-specification"><p>The only line of the input contains six integers $n$, $a_1$, $x$, $y$, $m$ and $k$ ($1 \le n \le 10^7$; $0 \le a_1, x, y &lt; m$; $2 \le m \le 998244353$; $1 \le k \le 5$).</p><p>The array $[a_1, a_2, \dots, a_n]$ is generated as follows:</p><ul> <li> $a_1$ is given in the input; </li><li> for $2 \le i \le n$, $a_i = (a_{i-1} \cdot x + y) \bmod m$. </li></ul></div><div class="output-specification"><p>Since outputting up to $10^7$ integers might be too slow, you have to do the following:</p><p>Let $c_i = b_i \cdot i$ <span class="tex-font-style-bf">(without taking modulo $998244353$ after the multiplication)</span>. Print the integer $c_1 \oplus c_2 \oplus \dots \oplus c_n$, where $\oplus$ denotes the bitwise XOR operator.</p></div>

## Input

<p>The only line of the input contains six integers $n$, $a_1$, $x$, $y$, $m$ and $k$ ($1 \le n \le 10^7$; $0 \le a_1, x, y &lt; m$; $2 \le m \le 998244353$; $1 \le k \le 5$).</p><p>The array $[a_1, a_2, \dots, a_n]$ is generated as follows:</p><ul> <li> $a_1$ is given in the input; </li><li> for $2 \le i \le n$, $a_i = (a_{i-1} \cdot x + y) \bmod m$. </li></ul>

## Output

<p>Since outputting up to $10^7$ integers might be too slow, you have to do the following:</p><p>Let $c_i = b_i \cdot i$ <span class="tex-font-style-bf">(without taking modulo $998244353$ after the multiplication)</span>. Print the integer $c_1 \oplus c_2 \oplus \dots \oplus c_n$, where $\oplus$ denotes the bitwise XOR operator.</p>





```input1
5 8 2 3 100 2
```




```output1
1283
```


