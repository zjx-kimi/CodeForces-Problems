## Description

<div><p>You are given an array $a$ of length $n$ consisting of non-negative integers.</p><p>You have to calculate the value of $\sum_{l=1}^{n} \sum_{r=l}^{n} f(l, r) \cdot (r - l + 1)$, where $f(l, r)$ is $a_l \oplus a_{l+1} \oplus \dots \oplus a_{r-1} \oplus a_r$ (the character $\oplus$ denotes bitwise XOR).</p><p>Since the answer can be very large, print it modulo $998244353$.</p></div><div class="input-specification"><p>The first line contains one integer $n$ ($1 \le n \le 3 \cdot 10^5$)&nbsp;— the length of the array $a$.</p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($0 \le a_i \le 10^9)$.</p></div><div class="output-specification"><p>Print the one integer&nbsp;— the value of $\sum_{l=1}^{n} \sum_{r=l}^{n} f(l, r) \cdot (r - l + 1)$, taken modulo $998244353$.</p></div>

## Input

<p>The first line contains one integer $n$ ($1 \le n \le 3 \cdot 10^5$)&nbsp;— the length of the array $a$.</p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($0 \le a_i \le 10^9)$.</p>

## Output

<p>Print the one integer&nbsp;— the value of $\sum_{l=1}^{n} \sum_{r=l}^{n} f(l, r) \cdot (r - l + 1)$, taken modulo $998244353$.</p>





```input1
3
1 3 2
```




```input2
4
39 68 31 80
```




```input3
7
313539461 779847196 221612534 488613315 633203958 394620685 761188160
```




```output1
12
```




```output2
1337
```




```output3
257421502
```



## Note

<p>In the first example, the answer is equal to $f(1, 1) + 2 \cdot f(1, 2) + 3 \cdot f(1, 3) + f(2, 2) + 2 \cdot f(2, 3) + f(3, 3) = $ $= 1 + 2 \cdot 2 + 3 \cdot 0 + 3 + 2 \cdot 1 + 2 = 12$.</p>
