## Description

<div><p>Ezzat has an array of $n$ integers <span class="tex-font-style-bf">(maybe negative)</span>. He wants to split it into two <span class="tex-font-style-bf">non-empty</span> subsequences $a$ and $b$, such that every element from the array belongs to exactly one subsequence, and the value of $f(a) + f(b)$ is the maximum possible value, where $f(x)$ is the average of the subsequence $x$. </p><p>A sequence $x$ is a subsequence of a sequence $y$ if $x$ can be obtained from $y$ by deletion of several (possibly, zero or all) elements.</p><p>The average of a subsequence is the sum of the numbers of this subsequence divided by the size of the subsequence.</p><p>For example, the average of $[1,5,6]$ is $(1+5+6)/3 = 12/3 = 4$, so $f([1,5,6]) = 4$.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^3$)— the number of test cases. Each test case consists of two lines.</p><p>The first line contains a single integer $n$ ($2 \le n \le 10^5$).</p><p>The second line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($-10^9 \le a_i \le 10^9$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $3\cdot10^5$.</p></div><div class="output-specification"><p>For each test case, print a single value — the maximum value that Ezzat can achieve.</p><p>Your answer is considered correct if its absolute or relative error does not exceed $10^{-6}$.</p><p>Formally, let your answer be $a$, and the jury's answer be $b$. Your answer is accepted if and only if $\frac{|a - b|}{\max{(1, |b|)}} \le 10^{-6}$.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^3$)— the number of test cases. Each test case consists of two lines.</p><p>The first line contains a single integer $n$ ($2 \le n \le 10^5$).</p><p>The second line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($-10^9 \le a_i \le 10^9$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $3\cdot10^5$.</p>

## Output

<p>For each test case, print a single value — the maximum value that Ezzat can achieve.</p><p>Your answer is considered correct if its absolute or relative error does not exceed $10^{-6}$.</p><p>Formally, let your answer be $a$, and the jury's answer be $b$. Your answer is accepted if and only if $\frac{|a - b|}{\max{(1, |b|)}} \le 10^{-6}$.</p>





```input1
4
3
3 1 2
3
-7 -6 -6
3
2 2 2
4
17 3 5 -3
```




```output1
4.500000000
-12.500000000
4.000000000
18.666666667
```



## Note

<p>In the first test case, the array is $[3, 1, 2]$. These are all the possible ways to split this array: </p><ul> <li> $a = [3]$, $b = [1,2]$, so the value of $f(a) + f(b) = 3 + 1.5 = 4.5$. </li><li> $a = [3,1]$, $b = [2]$, so the value of $f(a) + f(b) = 2 + 2 = 4$. </li><li> $a = [3,2]$, $b = [1]$, so the value of $f(a) + f(b) = 2.5 + 1 = 3.5$. </li></ul> Therefore, the maximum possible value $4.5$.<p>In the second test case, the array is $[-7, -6, -6]$. These are all the possible ways to split this array: </p><ul> <li> $a = [-7]$, $b = [-6,-6]$, so the value of $f(a) + f(b) = (-7) + (-6) = -13$. </li><li> $a = [-7,-6]$, $b = [-6]$, so the value of $f(a) + f(b) = (-6.5) + (-6) = -12.5$. </li></ul> Therefore, the maximum possible value $-12.5$.
