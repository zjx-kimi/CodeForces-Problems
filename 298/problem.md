## Description

<div><p>You are given an array $a$ consisting of $n$ positive integers. You can perform the following operation on it: </p><ol> <li> Choose a pair of elements $a_i$ and $a_j$ ($1 \le i, j \le n$ and $i \neq j$); </li><li> Choose one of the divisors of the integer $a_i$, i.e., an integer $x$ such that $a_i \bmod x = 0$; </li><li> Replace $a_i$ with $\frac{a_i}{x}$ and $a_j$ with $a_j \cdot x$. </li></ol> Determine whether it is possible to make all elements in the array the same by applying the operation a certain number of times (possibly zero).<p>For example, let's consider the array $a$ = [$100, 2, 50, 10, 1$] with $5$ elements. Perform two operations on it: </p><ol> <li> Choose $a_3 = 50$ and $a_2 = 2$, $x = 5$. Replace $a_3$ with $\frac{a_3}{x} = \frac{50}{5} = 10$, and $a_2$ with $a_2 \cdot x = 2 \cdot 5 = 10$. The resulting array is $a$ = [$100, 10, 10, 10, 1$]; </li><li> Choose $a_1 = 100$ and $a_5 = 1$, $x = 10$. Replace $a_1$ with $\frac{a_1}{x} = \frac{100}{10} = 10$, and $a_5$ with $a_5 \cdot x = 1 \cdot 10 = 10$. The resulting array is $a$ = [$10, 10, 10, 10, 10$]. </li></ol> After performing these operations, all elements in the array $a$ become equal to $10$.</div><div class="input-specification"><p>The first line of the input contains a single integer $t$ ($1 \le t \le 2000$)&nbsp;— the number of test cases.</p><p>Then follows the description of each test case.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 10^4$) — the number of elements in the array $a$.</p><p>The second line of each test case contains exactly $n$ integers $a_i$ ($1 \le a_i \le 10^6$) — the elements of the array $a$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^4$.</p></div><div class="output-specification"><p>For each test case, output a single line: </p><ul> <li> "<span class="tex-font-style-tt">YES</span>" if it is possible to make all elements in the array equal by applying the operation a certain (possibly zero) number of times; </li><li> "<span class="tex-font-style-tt">NO</span>" otherwise. </li></ul><p>You can output the answer in any case (for example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will all be recognized as a positive answer).</p></div>

## Input

<p>The first line of the input contains a single integer $t$ ($1 \le t \le 2000$)&nbsp;— the number of test cases.</p><p>Then follows the description of each test case.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 10^4$) — the number of elements in the array $a$.</p><p>The second line of each test case contains exactly $n$ integers $a_i$ ($1 \le a_i \le 10^6$) — the elements of the array $a$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^4$.</p>

## Output

<p>For each test case, output a single line: </p><ul> <li> "<span class="tex-font-style-tt">YES</span>" if it is possible to make all elements in the array equal by applying the operation a certain (possibly zero) number of times; </li><li> "<span class="tex-font-style-tt">NO</span>" otherwise. </li></ul><p>You can output the answer in any case (for example, the strings "<span class="tex-font-style-tt">yEs</span>", "<span class="tex-font-style-tt">yes</span>", "<span class="tex-font-style-tt">Yes</span>", and "<span class="tex-font-style-tt">YES</span>" will all be recognized as a positive answer).</p>





```input1|2,3,6,7,10,11,14,15
7
5
100 2 50 10 1
3
1 1 1
4
8 2 4 2
4
30 50 27 20
2
75 40
2
4 4
3
2 3 1
```




```output1
YES
YES
NO
YES
NO
YES
NO
```



## Note

<p>The first test case is explained in the problem statement.</p>
