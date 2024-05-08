## Description

<div><p>You have an array $a$ of $n$ non-negative integers. Let's define $f(a, x) = [a_1 \bmod x, a_2 \bmod x, \dots, a_n \bmod x]$ for some positive integer $x$. Find the biggest $x$, such that $f(a, x)$ is a palindrome.</p><p>Here, $a \bmod x$ is the remainder of the integer division of $a$ by $x$.</p><p>An array is a palindrome if it reads the same backward as forward. More formally, an array $a$ of length $n$ is a palindrome if for every $i$ ($1 \leq i \leq n$) $a_i = a_{n - i + 1}$.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \leq t \leq 10^5$) — the number of test cases.</p><p>The first line of each test case contains a single integer $n$ ($1 \leq n \leq 10^5$).</p><p>The second line of each test case contains $n$ integers $a_i$ ($0 \leq a_i \leq 10^9$).</p><p>It's guaranteed that the sum of all $n$ does not exceed $10^5$.</p></div><div class="output-specification"><p>For each test case output the biggest $x$, such that $f(a, x)$ is a palindrome. If $x$ can be infinitely large, output $0$ instead.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \leq t \leq 10^5$) — the number of test cases.</p><p>The first line of each test case contains a single integer $n$ ($1 \leq n \leq 10^5$).</p><p>The second line of each test case contains $n$ integers $a_i$ ($0 \leq a_i \leq 10^9$).</p><p>It's guaranteed that the sum of all $n$ does not exceed $10^5$.</p>

## Output

<p>For each test case output the biggest $x$, such that $f(a, x)$ is a palindrome. If $x$ can be infinitely large, output $0$ instead.</p>





```input1|2,3,6,7
4
2
1 2
8
3 0 1 2 0 3 2 1
1
0
3
100 1 1000000000
```




```output1
1
2
0
999999900
```



## Note

<p>In the first example, $f(a, x = 1) = [0, 0]$ which is a palindrome.</p><p>In the second example, $f(a, x = 2) = [1, 0, 1, 0, 0, 1, 0, 1]$ which is a palindrome.</p><p>It can be proven that in the first two examples, no larger $x$ satisfies the condition.</p><p>In the third example, $f(a, x) = [0]$ for any $x$, so we can choose it infinitely large, so the answer is $0$.</p>
