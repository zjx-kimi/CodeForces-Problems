## Description

<div><p>Alex got a new game called "GCD permutations" as a birthday present. Each round of this game proceeds as follows:</p><ul> <li> First, Alex chooses a permutation$^{\dagger}$ $a_1, a_2, \ldots, a_n$ of integers from $1$ to $n$. </li><li> Then, for each $i$ from $1$ to $n$, an integer $d_i = \gcd(a_i, a_{(i \bmod n) + 1})$ is calculated. </li><li> The <span class="tex-font-style-it">score</span> of the round is the number of distinct numbers among $d_1, d_2, \ldots, d_n$. </li></ul><p>Alex has already played several rounds so he decided to find a permutation $a_1, a_2, \ldots, a_n$ such that its score is as large as possible.</p><p>Recall that $\gcd(x, y)$ denotes the <a href="https://en.wikipedia.org/wiki/Greatest_common_divisor">greatest common divisor (GCD)</a> of numbers $x$ and $y$, and $x \bmod y$ denotes the remainder of dividing $x$ by $y$.</p><p>$^{\dagger}$A permutation of length $n$ is an array consisting of $n$ distinct integers from $1$ to $n$ in arbitrary order. For example, $[2,3,1,5,4]$ is a permutation, but $[1,2,2]$ is not a permutation ($2$ appears twice in the array), and $[1,3,4]$ is also not a permutation ($n=3$ but there is $4$ in the array).</p></div><div class="input-specification"><p>The first line of the input contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>Each test case consists of one line containing a single integer $n$ ($2 \le n \le 10^5$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p></div><div class="output-specification"><p>For each test case print $n$ distinct integers $a_{1},a_{2},\ldots,a_{n}$ ($1 \le a_i \le n$)&nbsp;— the permutation with the largest possible score.</p><p>If there are several permutations with the maximum possible score, you can print any one of them.</p></div>

## Input

<p>The first line of the input contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>Each test case consists of one line containing a single integer $n$ ($2 \le n \le 10^5$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p>

## Output

<p>For each test case print $n$ distinct integers $a_{1},a_{2},\ldots,a_{n}$ ($1 \le a_i \le n$)&nbsp;— the permutation with the largest possible score.</p><p>If there are several permutations with the maximum possible score, you can print any one of them.</p>





```input1|2,4
4
5
2
7
10
```




```output1
1 2 4 3 5 
1 2 
1 2 3 6 4 5 7 
1 2 3 4 8 5 10 6 9 7
```



## Note

<p>In the first test case, Alex wants to find a permutation of integers from $1$ to $5$. For the permutation $a=[1,2,4,3,5]$, the array $d$ is equal to $[1,2,1,1,1]$. It contains $2$ distinct integers. It can be shown that there is no permutation of length $5$ with a higher score.</p><p>In the second test case, Alex wants to find a permutation of integers from $1$ to $2$. There are only two such permutations: $a=[1,2]$ and $a=[2,1]$. In both cases, the array $d$ is equal to $[1,1]$, so both permutations are correct.</p><p>In the third test case, Alex wants to find a permutation of integers from $1$ to $7$. For the permutation $a=[1,2,3,6,4,5,7]$, the array $d$ is equal to $[1,1,3,2,1,1,1]$. It contains $3$ distinct integers so its score is equal to $3$. It can be shown that there is no permutation of integers from $1$ to $7$ with a score higher than $3$.</p>
