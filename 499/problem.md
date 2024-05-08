## Description

<div><p><span class="tex-font-style-bf">The only difference between this problem and the hard version is the constraints on $t$ and $n$.</span></p><p>You are given an array of $n$ positive integers $a_1,\dots,a_n$, and a (possibly negative) integer $c$.</p><p>Across all permutations $b_1,\dots,b_n$ of the array $a_1,\dots,a_n$, consider the minimum possible value of $$\sum_{i=1}^{n-1} |b_{i+1}-b_i-c|.$$ Find the lexicographically smallest permutation $b$ of the array $a$ that achieves this minimum.</p><p>A sequence $x$ is lexicographically smaller than a sequence $y$ if and only if one of the following holds:</p><ul><li> $x$ is a prefix of $y$, but $x \ne y$;</li><li> in the first position where $x$ and $y$ differ, the sequence $x$ has a smaller element than the corresponding element in $y$.</li></ul></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^3$). The description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $c$ ($1 \le n \le 5 \cdot 10^3$, $-10^9 \le c \le 10^9$).</p><p>The second line of each test case contains $n$ integers $a_1,\dots,a_n$ ($1 \le a_i \le 10^9$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $5 \cdot 10^3$.</p></div><div class="output-specification"><p>For each test case, output $n$ integers $b_1,\dots,b_n$, the lexicographically smallest permutation of $a$ that achieves the minimum $\sum\limits_{i=1}^{n-1} |b_{i+1}-b_i-c|$.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^3$). The description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $c$ ($1 \le n \le 5 \cdot 10^3$, $-10^9 \le c \le 10^9$).</p><p>The second line of each test case contains $n$ integers $a_1,\dots,a_n$ ($1 \le a_i \le 10^9$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $5 \cdot 10^3$.</p>

## Output

<p>For each test case, output $n$ integers $b_1,\dots,b_n$, the lexicographically smallest permutation of $a$ that achieves the minimum $\sum\limits_{i=1}^{n-1} |b_{i+1}-b_i-c|$.</p>





```input1|2,3,6,7
3
6 -7
3 1 4 1 5 9
3 2
1 3 5
1 2718
2818
```




```output1
9 3 1 4 5 1
1 3 5
2818
```



## Note

<p>In the first test case, it can be proven that the minimum possible value of $\sum\limits_{i=1}^{n-1} |b_{i+1}-b_i-c|$ is $27$, and the permutation $b = [9,3,1,4,5,1]$ is the lexicographically smallest permutation of $a$ that achieves this minimum: $|3-9-(-7)|+|1-3-(-7)|+|4-1-(-7)|+|5-4-(-7)|+|1-5-(-7)| = 1+5+10+8+3 = 27$.</p><p>In the second test case, the minimum possible value of $\sum\limits_{i=1}^{n-1} |b_{i+1}-b_i-c|$ is $0$, and $b = [1,3,5]$ is the lexicographically smallest permutation of $a$ that achieves this.</p><p>In the third test case, there is only one permutation $b$.</p>
