## Description

<div><p>Let's call a triple of positive integers ($a, b, n$) <span class="tex-font-style-it">strange</span> if the equality $\frac{an}{nb} = \frac{a}{b}$ holds, where $an$ is the concatenation of $a$ and $n$ and $nb$ is the concatenation of $n$ and $b$. For the purpose of concatenation, the integers are considered without leading zeroes.</p><p>For example, if $a = 1$, $b = 5$ and $n = 9$, then the triple is strange, because $\frac{19}{95} = \frac{1}{5}$. But $a = 7$, $b = 3$ and $n = 11$ is not strange, because $\frac{711}{113} \ne \frac{7}{3}$.</p><p>You are given three integers $A$, $B$ and $N$. Calculate the number of strange triples $(a, b, n$), such that $1 \le a &lt; A$, $1 \le b &lt; B$ and $1 \le n &lt; N$.</p></div><div class="input-specification"><p>The only line contains three integers $A$, $B$ and $N$ ($1 \le A, B \le 10^5$; $1 \le N \le 10^9$).</p></div><div class="output-specification"><p>Print one integer&nbsp;— the number of strange triples $(a, b, n$) such that $1 \le a &lt; A$, $1 \le b &lt; B$ and $1 \le n &lt; N$.</p></div>

## Input

<p>The only line contains three integers $A$, $B$ and $N$ ($1 \le A, B \le 10^5$; $1 \le N \le 10^9$).</p>

## Output

<p>Print one integer&nbsp;— the number of strange triples $(a, b, n$) such that $1 \le a &lt; A$, $1 \le b &lt; B$ and $1 \le n &lt; N$.</p>





```input1
5 6 10
```




```input2
10 10 100
```




```input3
1 10 25
```




```input4
4242 6969 133333337
```




```input5
94841 47471 581818184
```




```output1
7
```




```output2
29
```




```output3
0
```




```output4
19536
```




```output5
98715
```



## Note

<p>In the first example, there are $7$ strange triples: $(1, 1, 1$), ($1, 4, 6$), ($1, 5, 9$), ($2, 2, 2$), ($2, 5, 6$), ($3, 3, 3$) and ($4, 4, 4$).</p>
