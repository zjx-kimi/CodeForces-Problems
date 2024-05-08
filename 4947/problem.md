## Description

<div><p>The prime factorization of a positive integer $m$ is the unique way to write it as $\displaystyle m=p_1^{e_1}\cdot p_2^{e_2}\cdot \ldots \cdot p_k^{e_k}$, where $p_1, p_2, \ldots, p_k$ are prime numbers, $p_1 &lt; p_2 &lt; \ldots &lt; p_k$ and $e_1, e_2, \ldots, e_k$ are positive integers. </p><p>For each positive integer $m$, $f(m)$ is defined as the multiset of all numbers in its prime factorization, that is $f(m)=\{p_1,e_1,p_2,e_2,\ldots,p_k,e_k\}$. </p><p>For example, $f(24)=\{2,3,3,1\}$, $f(5)=\{1,5\}$ and $f(1)=\{\}$.</p><p>You are given a list consisting of $2n$ integers $a_1, a_2, \ldots, a_{2n}$. Count how many positive integers $m$ satisfy that $f(m)=\{a_1, a_2, \ldots, a_{2n}\}$. Since this value may be large, print it modulo $998\,244\,353$.</p></div><div class="input-specification"><p>The first line contains one integer $n$ ($1\le n \le 2022$).</p><p>The second line contains $2n$ integers $a_1, a_2, \ldots, a_{2n}$ ($1\le a_i\le 10^6$) &nbsp;— the given list.</p></div><div class="output-specification"><p>Print one integer, the number of positive integers $m$ satisfying $f(m)=\{a_1, a_2, \ldots, a_{2n}\}$ modulo $998\,244\,353$.</p></div>

## Input

<p>The first line contains one integer $n$ ($1\le n \le 2022$).</p><p>The second line contains $2n$ integers $a_1, a_2, \ldots, a_{2n}$ ($1\le a_i\le 10^6$) &nbsp;— the given list.</p>

## Output

<p>Print one integer, the number of positive integers $m$ satisfying $f(m)=\{a_1, a_2, \ldots, a_{2n}\}$ modulo $998\,244\,353$.</p>





```input1
2
1 3 2 3
```




```input2
2
2 2 3 5
```




```input3
1
1 4
```




```output1
2
```




```output2
5
```




```output3
0
```



## Note

<p>In the first sample, the two values of $m$ such that $f(m)=\{1,2,3,3\}$ are $m=24$ and $m=54$. Their prime factorizations are $24=2^3\cdot 3^1$ and $54=2^1\cdot 3^3$.</p><p>In the second sample, the five values of $m$ such that $f(m)=\{2,2,3,5\}$ are $200, 225, 288, 500$ and $972$.</p><p>In the third sample, there is no value of $m$ such that $f(m)=\{1,4\}$. Neither $1^4$ nor $4^1$ are prime factorizations because $1$ and $4$ are <span class="tex-font-style-bf">not</span> primes.</p>
