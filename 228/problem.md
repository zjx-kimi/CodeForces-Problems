## Description

<div><p>The boy Smilo is learning algorithms with a teacher named Brukhovich.</p><p>Over the course of the year, Brukhovich will administer $n$ exams. For each exam, its difficulty $a_i$ is known, which is a non-negative integer.</p><p>Smilo doesn't like when the greatest common divisor of the difficulties of two consecutive exams is equal to $1$. Therefore, he considers the <span class="tex-font-style-it">sadness</span> of the academic year to be the number of such pairs of exams. More formally, the <span class="tex-font-style-it">sadness</span> is the number of indices $i$ ($1 \leq i \leq n - 1$) such that $gcd(a_i, a_{i+1}) = 1$, where $gcd(x, y)$ is the greatest common divisor of integers $x$ and $y$.</p><p>Brukhovich wants to minimize the sadness of the year of Smilo. To do this, he can set the difficulty of any exam to $0$. However, Brukhovich doesn't want to make his students' lives too easy. Therefore, he will perform this action no more than $k$ times.</p><p>Help Smilo determine the minimum sadness that Brukhovich can achieve if he performs no more than $k$ operations.</p><p>As a reminder, the greatest common divisor (GCD) of two non-negative integers $x$ and $y$ is the maximum integer that is a divisor of both $x$ and $y$ and is denoted as $gcd(x, y)$. In particular, $gcd(x, 0) = gcd(0, x) = x$ for any non-negative integer $x$.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \leq t \leq 10^4$) — the number of test cases. The descriptions of the test cases follow.</p><p>The first line of each test case contains two integers $n$ and $k$ ($1 \leq k \leq n \leq 10^5$) — the total number of exams and the maximum number of exams that can be simplified, respectively. </p><p>The second line of each test case contains $n$ integers $a_1, a_2, a_3, \ldots, a_n$ — the elements of array $a$, which are the difficulties of the exams ($0 \leq a_i \leq 10^9$).</p><p>It is guaranteed that the sum of $n$ across all test cases does not exceed $10^5$.</p></div><div class="output-specification"><p>For each test case, output the minimum possible sadness that can be achieved by performing no more than $k$ operations.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \leq t \leq 10^4$) — the number of test cases. The descriptions of the test cases follow.</p><p>The first line of each test case contains two integers $n$ and $k$ ($1 \leq k \leq n \leq 10^5$) — the total number of exams and the maximum number of exams that can be simplified, respectively. </p><p>The second line of each test case contains $n$ integers $a_1, a_2, a_3, \ldots, a_n$ — the elements of array $a$, which are the difficulties of the exams ($0 \leq a_i \leq 10^9$).</p><p>It is guaranteed that the sum of $n$ across all test cases does not exceed $10^5$.</p>

## Output

<p>For each test case, output the minimum possible sadness that can be achieved by performing no more than $k$ operations.</p>





```input1|2,3,6,7,10,11,14,15,18,19
9
5 2
1 3 5 7 9
5 2
3 5 7 9 11
8 2
17 15 10 1 1 5 14 8
5 3
1 1 1 1 1
5 5
1 1 1 1 1
19 7
1 1 2 3 4 5 5 6 6 7 8 9 10 1 1 1 2 3 1
15 6
2 1 1 1 1 2 1 1 2 1 1 1 2 1 2
5 2
1 1 1 1 2
5 2
1 0 1 0 1
```




```output1
1
0
2
2
0
5
5
2
1
```



## Note

<p>In the first test case, a sadness of $1$ can be achieved. To this, you can simplify the second and fourth exams. After this, there will be only one pair of adjacent exams with a greatest common divisor (GCD) equal to one, which is the first and second exams.</p><p>In the second test case, a sadness of $0$ can be achieved by simplifying the second and fourth exams.</p>
