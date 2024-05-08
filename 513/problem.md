## Description

<div><div class="epigraph"><div class="epigraph-text"><span class="tex-font-style-it">Yet another random problem.</span></div></div><p>Tenzing has an array $a$ of length $n$ and an integer $v$.</p><p>Tenzing will perform the following operation $m$ times:</p><ol> <li> Choose an integer $i$ such that $1 \leq i \leq n$ uniformly at random. </li><li> For all $j$ such that $i \leq j \leq n$, set $a_j := a_j + v$. </li></ol><p>Tenzing wants to know the expected value of $\prod_{i=1}^n a_i$ after performing the $m$ operations, modulo $10^9+7$.</p><p>Formally, let $M = 10^9+7$. It can be shown that the answer can be expressed as an irreducible fraction $\frac{p}{q}$, where $p$ and $q$ are integers and $q \not \equiv 0 \pmod{M}$. Output the integer equal to $p \cdot q^{-1} \bmod M$. In other words, output the integer $x$ that $0 \le x &lt; M$ and $x \cdot q \equiv p \pmod{M}$.</p></div><div class="input-specification"><p>The first line of input contains three integers $n$, $m$ and $v$ ($1\leq n\leq 5000$, $1\leq m,v\leq 10^9$).</p><p>The second line of input contains $n$ integers $a_1,a_2,\ldots,a_n$ ($1\leq a_i\leq 10^9$).</p></div><div class="output-specification"><p>Output the expected value of $\prod_{i=1}^n a_i$ modulo $10^9+7$.</p></div>

## Input

<p>The first line of input contains three integers $n$, $m$ and $v$ ($1\leq n\leq 5000$, $1\leq m,v\leq 10^9$).</p><p>The second line of input contains $n$ integers $a_1,a_2,\ldots,a_n$ ($1\leq a_i\leq 10^9$).</p>

## Output

<p>Output the expected value of $\prod_{i=1}^n a_i$ modulo $10^9+7$.</p>





```input1
2 2 5
2 2
```




```input2
5 7 9
9 9 8 2 4
```




```output1
84
```




```output2
975544726
```



## Note

<p>There are three types of $a$ after performing all the $m$ operations : </p><p>1. $a_1=2,a_2=12$ with $\frac{1}{4}$ probability.</p><p>2. $a_1=a_2=12$ with $\frac{1}{4}$ probability.</p><p>3. $a_1=7,a_2=12$ with $\frac{1}{2}$ probability.</p><p>So the expected value of $a_1\cdot a_2$ is $\frac{1}{4}\cdot (24+144) + \frac{1}{2}\cdot 84=84$.</p>
