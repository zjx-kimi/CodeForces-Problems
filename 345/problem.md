## Description

<div><p>You are given $3$ integers&nbsp;— $n$, $x$, $y$. Let's call the <span class="tex-font-style-it">score</span> of a permutation$^\dagger$ $p_1, \ldots, p_n$ the following value:</p><p><span>$$(p_{1 \cdot x} + p_{2 \cdot x} + \ldots + p_{\lfloor \frac{n}{x} \rfloor \cdot x}) - (p_{1 \cdot y} + p_{2 \cdot y} + \ldots + p_{\lfloor \frac{n}{y} \rfloor \cdot y})$$</span></p><p>In other words, the <span class="tex-font-style-it">score</span> of a permutation is the sum of $p_i$ for all indices $i$ divisible by $x$, minus the sum of $p_i$ for all indices $i$ divisible by $y$.</p><p>You need to find the maximum possible <span class="tex-font-style-it">score</span> among all permutations of length $n$.</p><p>For example, if $n = 7$, $x = 2$, $y = 3$, the maximum <span class="tex-font-style-it">score</span> is achieved by the permutation $[2,\color{red}{\underline{\color{black}{6}}},\color{blue}{\underline{\color{black}{1}}},\color{red}{\underline{\color{black}{7}}},5,\color{blue}{\underline{\color{red}{\underline{\color{black}{4}}}}},3]$ and is equal to $(6 + 7 + 4) - (1 + 4) = 17 - 5 = 12$.</p><p>$^\dagger$ A permutation of length $n$ is an array consisting of $n$ distinct integers from $1$ to $n$ in any order. For example, $[2,3,1,5,4]$ is a permutation, but $[1,2,2]$ is not a permutation (the number $2$ appears twice in the array) and $[1,3,4]$ is also not a permutation ($n=3$, but the array contains $4$).</p></div><div class="input-specification"><p>The first line of input contains an integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>Then follows the description of each test case.</p><p>The only line of each test case description contains $3$ integers $n$, $x$, $y$ ($1 \le n \le 10^9$, $1 \le x, y \le n$).</p></div><div class="output-specification"><p>For each test case, output a single integer&nbsp;— the maximum <span class="tex-font-style-it">score</span> among all permutations of length $n$.</p></div>

## Input

<p>The first line of input contains an integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>Then follows the description of each test case.</p><p>The only line of each test case description contains $3$ integers $n$, $x$, $y$ ($1 \le n \le 10^9$, $1 \le x, y \le n$).</p>

## Output

<p>For each test case, output a single integer&nbsp;— the maximum <span class="tex-font-style-it">score</span> among all permutations of length $n$.</p>





```input1|2,4,6,8
8
7 2 3
12 6 3
9 1 9
2 2 2
100 20 50
24 4 6
1000000000 5575 25450
4 4 1
```




```output1
12
-3
44
0
393
87
179179179436104
-6
```



## Note

<p>The first test case is explained in the problem statement above.</p><p>In the second test case, one of the optimal permutations will be $[12,11,\color{blue}{\underline{\color{black}{2}}},4,8,\color{blue}{\underline{\color{red}{\underline{\color{black}{9}}}}},10,6,\color{blue}{\underline{\color{black}{1}}},5,3,\color{blue}{\underline{\color{red}{\underline{\color{black}{7}}}}}]$. The <span class="tex-font-style-it">score</span> of this permutation is $(9 + 7) - (2 + 9 + 1 + 7) = -3$. It can be shown that a <span class="tex-font-style-it">score</span> greater than $-3$ can not be achieved. Note that the answer to the problem can be negative.</p><p>In the third test case, the <span class="tex-font-style-it">score</span> of the permutation will be $(p_1 + p_2 + \ldots + p_9) - p_9$. One of the optimal permutations for this case is $[9, 8, 7, 6, 5, 4, 3, 2, 1]$, and its <span class="tex-font-style-it">score</span> is $44$. It can be shown that a <span class="tex-font-style-it">score</span> greater than $44$ can not be achieved.</p><p>In the fourth test case, $x = y$, so the <span class="tex-font-style-it">score</span> of any permutation will be $0$.</p>
