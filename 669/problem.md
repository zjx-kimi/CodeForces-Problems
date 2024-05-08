## Description

<div><p>$$f(n) = \left\{ \begin{array}{ll} \frac{n}{2} &amp; n \equiv 0 \pmod{2}\\ 3n+1 &amp; n \equiv 1 \pmod{2}\\ \end{array} \right.$$</p><p>Find an integer $n$ so that none of the first $k$ terms of the sequence $n, f(n), f(f(n)), f(f(f(n))), \dots$ are equal to $1$.</p></div><div class="input-specification"><p>The only line contains an integer $k$ ($1 \leq k \leq \min(\textbf{[REDACTED]}, 10^{18})$).</p></div><div class="output-specification"><p>Output a single integer $n$ such that none of the first $k$ terms of the sequence $n, f(n), f(f(n)), f(f(f(n))), \dots$ are equal to $1$.</p><p>Integer $n$ should have at most $10^3$ digits.</p></div>

## Input

<p>The only line contains an integer $k$ ($1 \leq k \leq \min(\textbf{[REDACTED]}, 10^{18})$).</p>

## Output

<p>Output a single integer $n$ such that none of the first $k$ terms of the sequence $n, f(n), f(f(n)), f(f(f(n))), \dots$ are equal to $1$.</p><p>Integer $n$ should have at most $10^3$ digits.</p>





```input1
1
```




```input2
5
```




```output1
5
```




```output2
6
```



## Note

<p>In the first test, the sequence created with $n = 5$ looks like $5, 16, 8, 4, 2, 1, 4, \dots$, and none of the first $k=1$ terms are equal to $1$.</p><p>In the second test, the sequence created with $n = 6$ looks like $6, 3, 10, 5, 16, 8, 4, \dots$, and none of the first $k=5$ terms are equal to $1$.</p>
