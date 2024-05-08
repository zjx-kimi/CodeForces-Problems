## Description

<div><p>You are given an array $[a_1, a_2, \dots, a_n]$, consisting of positive integers.</p><p>For every $i$ from $1$ to $n$, calculate $\sum \limits_{j=1}^{n} F(a_i + a_j)$, where $F(x)$ is the sum of digits of $x$.</p></div><div class="input-specification"><p>The first line contains one integer $n$ ($2 \le n \le 2 \cdot 10^5$).</p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i &lt; 10^9$).</p></div><div class="output-specification"><p>Print $n$ integers. The $i$-th of them should be equal to $\sum \limits_{j=1}^{n} F(a_i + a_j)$.</p></div>

## Input

<p>The first line contains one integer $n$ ($2 \le n \le 2 \cdot 10^5$).</p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i &lt; 10^9$).</p>

## Output

<p>Print $n$ integers. The $i$-th of them should be equal to $\sum \limits_{j=1}^{n} F(a_i + a_j)$.</p>





```input1
4
1 3 3 7
```




```input2
3
42 1337 999
```




```output1
18 17 17 15
```




```output2
38 53 47
```


