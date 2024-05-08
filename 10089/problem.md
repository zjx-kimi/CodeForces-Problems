## Description

<div><p>You are given $n$ positive integers $x_1, x_2, \ldots, x_n$ and three positive integers $n_a, n_b, n_c$ satisfying $n_a+n_b+n_c = n$. </p><p>You want to split the $n$ positive integers into three groups, so that:</p><ul><li> The first group contains $n_a$ numbers, the second group contains $n_b$ numbers, the third group contains $n_c$ numbers.</li><li> Let $s_a$ be the sum of the numbers in the first group, $s_b$ be the sum in the second group, and $s_c$ be the sum in the third group. Then $s_a, s_b, s_c$ are the sides of a triangle with positive area.</li></ul><p>Determine if this is possible. If this is possible, find one way to do so.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains an integer $t$ ($1\le t\le 100\,000$)&nbsp;— the number of test cases. The descriptions of the $t$ test cases follow.</p><p>The first line of each test case contains the integers $n, n_a, n_b, n_c$ ($3 \leq n \leq 200\,000, 1\leq n_a,n_b,n_c \leq n-2, n_a+n_b+n_c = n$)&nbsp;— the number of integers to split into three groups, and the desired sizes of the three groups.</p><p>The second line of each test case contains $n$ integers $x_1, x_2, \ldots, x_n$ ($1 \leq x_i \leq 10^{9}$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $200\,000$.</p></div><div class="output-specification"><p>For each test case, print $\texttt{YES}$ if it is possible to split the numbers into three groups satisfying all the conditions. Otherwise, print $\texttt{NO}$.</p><p>If such a split exists, then describe the three groups as follows.</p><p>On the next line, print $n_a$ integers $a_1, a_2, \ldots, a_{n_a}$&nbsp;— the numbers in the first group.</p><p>On the next line, print $n_b$ integers $b_1, b_2, \ldots, b_{n_b}$&nbsp;— the numbers in the second group.</p><p>On the next line, print $n_c$ integers $c_1, c_2, \ldots, c_{n_c}$&nbsp;— the numbers in the third group.</p><p>These $n_a+n_b+n_c=n$ integers should be a permutation of $x_1, x_2, \ldots, x_n$, and they should satisfy the conditions from the statement.</p><p>If there are multiple solutions, print any of them.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains an integer $t$ ($1\le t\le 100\,000$)&nbsp;— the number of test cases. The descriptions of the $t$ test cases follow.</p><p>The first line of each test case contains the integers $n, n_a, n_b, n_c$ ($3 \leq n \leq 200\,000, 1\leq n_a,n_b,n_c \leq n-2, n_a+n_b+n_c = n$)&nbsp;— the number of integers to split into three groups, and the desired sizes of the three groups.</p><p>The second line of each test case contains $n$ integers $x_1, x_2, \ldots, x_n$ ($1 \leq x_i \leq 10^{9}$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $200\,000$.</p>

## Output

<p>For each test case, print $\texttt{YES}$ if it is possible to split the numbers into three groups satisfying all the conditions. Otherwise, print $\texttt{NO}$.</p><p>If such a split exists, then describe the three groups as follows.</p><p>On the next line, print $n_a$ integers $a_1, a_2, \ldots, a_{n_a}$&nbsp;— the numbers in the first group.</p><p>On the next line, print $n_b$ integers $b_1, b_2, \ldots, b_{n_b}$&nbsp;— the numbers in the second group.</p><p>On the next line, print $n_c$ integers $c_1, c_2, \ldots, c_{n_c}$&nbsp;— the numbers in the third group.</p><p>These $n_a+n_b+n_c=n$ integers should be a permutation of $x_1, x_2, \ldots, x_n$, and they should satisfy the conditions from the statement.</p><p>If there are multiple solutions, print any of them.</p>





```input1|2,3,6,7
4
6 2 2 2
1 1 1 1 1 1
5 3 1 1
1 1 1 1 1
6 2 2 2
1 1 1 1 1 3
8 1 2 5
16 1 1 1 1 1 1 12
```




```output1
YES
1 1 
1 1 
1 1 
NO
NO
YES
16 
12 1 
1 1 1 1 1
```



## Note

<p>In the <span class="tex-font-style-bf">first test case</span>, we can put two $1$s into each group: the sum in each group would be $2$, and there exists a triangle with positive area and sides $2$, $2$, $2$.</p><p>In the <span class="tex-font-style-bf">second and third test cases</span>, it can be shown that there is no such way to split numbers into groups.</p><p>In the <span class="tex-font-style-bf">fourth test case</span>, we can put number $16$ into the first group, with sum $16$, numbers $12$ and $1$ into the second group, with sum $13$, and the remaining five $1$s into the third group, with sum $5$, as there exists a triangle with positive area and sides $16, 13, 5$.</p>
