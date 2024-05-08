## Description

<div><p>You are given a positive integer $n$.</p><p>Let $S(x)$ be sum of digits in base 10 representation of $x$, for example, $S(123) = 1 + 2 + 3 = 6$, $S(0) = 0$.</p><p>Your task is to find two integers $a, b$, such that $0 \leq a, b \leq n$, $a + b = n$ and $S(a) + S(b)$ is the largest possible among all such pairs.</p></div><div class="input-specification"><p>The only line of input contains an integer $n$ $(1 \leq n \leq 10^{12})$.</p></div><div class="output-specification"><p>Print largest $S(a) + S(b)$ among all pairs of integers $a, b$, such that $0 \leq a, b \leq n$ and $a + b = n$.</p></div>

## Input

<p>The only line of input contains an integer $n$ $(1 \leq n \leq 10^{12})$.</p>

## Output

<p>Print largest $S(a) + S(b)$ among all pairs of integers $a, b$, such that $0 \leq a, b \leq n$ and $a + b = n$.</p>





```input1
35

```




```input2
10000000000

```




```output1
17

```




```output2
91

```



## Note

<p>In the first example, you can choose, for example, $a = 17$ and $b = 18$, so that $S(17) + S(18) = 1 + 7 + 1 + 8 = 17$. It can be shown that it is impossible to get a larger answer.</p><p>In the second test example, you can choose, for example, $a = 5000000001$ and $b = 4999999999$, with $S(5000000001) + S(4999999999) = 91$. It can be shown that it is impossible to get a larger answer.</p>
