## Description

<div><p>A polynomial $A(x)$ of degree $d$ is an expression of the form $A(x) = a_0 + a_1 x + a_2 x^2 + \dots + a_d x^d$, where $a_i$ are integers, and $a_d \neq 0$. Two polynomials $A(x)$ and $B(x)$ are called similar if there is an integer $s$ such that for any integer $x$ it holds that</p><p>$$ B(x) \equiv A(x+s) \pmod{10^9+7}. $$</p><p>For two similar polynomials $A(x)$ and $B(x)$ of degree $d$, you're given their values in the points $x=0,1,\dots, d$ modulo $10^9+7$.</p><p>Find a value $s$ such that $B(x) \equiv A(x+s) \pmod{10^9+7}$ for all integers $x$.</p></div><div class="input-specification"><p>The first line contains a single integer $d$ ($1 \le d \le 2\,500\,000$).</p><p>The second line contains $d+1$ integers $A(0), A(1), \ldots, A(d)$ ($0 \le A(i) &lt; 10^9+7$) — the values of the polynomial $A(x)$.</p><p>The third line contains $d+1$ integers $B(0), B(1), \ldots, B(d)$ ($0 \le B(i) &lt; 10^9+7$) — the values of the polynomial $B(x)$.</p><p>It is guaranteed that $A(x)$ and $B(x)$ are similar and that the leading coefficients (i.e., the coefficients in front of $x^d$) of $A(x)$ and $B(x)$ are not divisible by $10^9+7$.</p></div><div class="output-specification"><p>Print a single integer $s$ ($0 \leq s &lt; 10^9+7$) such that $B(x) \equiv A(x+s) \pmod{10^9+7}$ for all integers $x$.</p><p>If there are multiple solutions, print any.</p></div>

## Input

<p>The first line contains a single integer $d$ ($1 \le d \le 2\,500\,000$).</p><p>The second line contains $d+1$ integers $A(0), A(1), \ldots, A(d)$ ($0 \le A(i) &lt; 10^9+7$) — the values of the polynomial $A(x)$.</p><p>The third line contains $d+1$ integers $B(0), B(1), \ldots, B(d)$ ($0 \le B(i) &lt; 10^9+7$) — the values of the polynomial $B(x)$.</p><p>It is guaranteed that $A(x)$ and $B(x)$ are similar and that the leading coefficients (i.e., the coefficients in front of $x^d$) of $A(x)$ and $B(x)$ are not divisible by $10^9+7$.</p>

## Output

<p>Print a single integer $s$ ($0 \leq s &lt; 10^9+7$) such that $B(x) \equiv A(x+s) \pmod{10^9+7}$ for all integers $x$.</p><p>If there are multiple solutions, print any.</p>





```input1
1
1000000006 0
2 3
```




```input2
2
1 4 9
100 121 144
```




```output1
3
```




```output2
9
```



## Note

<p>In the first example, $A(x) \equiv x-1 \pmod{10^9+7}$ and $B(x)\equiv x+2 \pmod{10^9+7}$. They're similar because $$B(x) \equiv A(x+3) \pmod{10^9+7}.$$</p><p>In the second example, $A(x) \equiv (x+1)^2 \pmod{10^9+7}$ and $B(x) \equiv (x+10)^2 \pmod{10^9+7}$, hence $$B(x) \equiv A(x+9) \pmod{10^9+7}.$$</p>
