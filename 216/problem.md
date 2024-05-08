## Description

<div><p>You are given $n-1$ integers $a_1, a_2, \dots, a_{n-1}$.</p><p>Your task is to construct an array $b_1, b_2, \dots, b_n$ such that:</p><ul> <li> every integer from $0$ to $n-1$ appears in $b$ exactly once; </li><li> for every $i$ from $1$ to $n-1$, $b_i \oplus b_{i+1} = a_i$ (where $\oplus$ denotes the bitwise XOR operator). </li></ul></div><div class="input-specification"><p>The first line contains one integer $n$ ($2 \le n \le 2 \cdot 10^5$).</p><p>The second line contains $n-1$ integers $a_1, a_2, \dots, a_{n-1}$ ($0 \le a_i \le 2n$).</p><p>Additional constraint on the input: it's always possible to construct at least one valid array $b$ from the given sequence $a$.</p></div><div class="output-specification"><p>Print $n$ integers $b_1, b_2, \dots, b_n$. If there are multiple such arrays, you may print any of them.</p></div>

## Input

<p>The first line contains one integer $n$ ($2 \le n \le 2 \cdot 10^5$).</p><p>The second line contains $n-1$ integers $a_1, a_2, \dots, a_{n-1}$ ($0 \le a_i \le 2n$).</p><p>Additional constraint on the input: it's always possible to construct at least one valid array $b$ from the given sequence $a$.</p>

## Output

<p>Print $n$ integers $b_1, b_2, \dots, b_n$. If there are multiple such arrays, you may print any of them.</p>





```input1|
4
2 1 2
```




```input2|
6
1 6 1 4 1
```




```output1
0 2 3 1
```




```output2
2 3 5 4 0 1
```


