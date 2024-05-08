## Description

<div><p>Kristina had an array $a$ of length $n$ consisting of non-negative integers.</p><p>She built a new array $b$ of length $n-1$, such that $b_i = \max(a_i, a_{i+1})$ ($1 \le i \le n-1$).</p><p>For example, suppose Kristina had an array $a$ = [$3, 0, 4, 0, 5$] of length $5$. Then she did the following: </p><ol> <li> Calculated $b_1 = \max(a_1, a_2) = \max(3, 0) = 3$; </li><li> Calculated $b_2 = \max(a_2, a_3) = \max(0, 4) = 4$; </li><li> Calculated $b_3 = \max(a_3, a_4) = \max(4, 0) = 4$; </li><li> Calculated $b_4 = \max(a_4, a_5) = \max(0, 5) = 5$. </li></ol> As a result, she got an array $b$ = [$3, 4, 4, 5$] of length $4$.<p>You only know the array $b$. Find any matching array $a$ that Kristina may have originally had.</p></div><div class="input-specification"><p>The first line of input data contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The description of the test cases follows.</p><p>The first line of each test case contains one integer $n$ ($2 \le n \le 2 \cdot 10^5$) — the number of elements in the array $a$ that Kristina originally had.</p><p>The second line of each test case contains exactly $n-1$ non-negative integer — elements of array $b$ ($0 \le b_i \le 10^9$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$, and that array $b$ was built correctly from some array $a$.</p></div><div class="output-specification"><p>For each test case on a separate line, print exactly $n$ non-negative integers — the elements of the array $a$ that Kristina originally had.</p><p>If there are several possible answers — output any of them.</p></div>

## Input

<p>The first line of input data contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The description of the test cases follows.</p><p>The first line of each test case contains one integer $n$ ($2 \le n \le 2 \cdot 10^5$) — the number of elements in the array $a$ that Kristina originally had.</p><p>The second line of each test case contains exactly $n-1$ non-negative integer — elements of array $b$ ($0 \le b_i \le 10^9$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$, and that array $b$ was built correctly from some array $a$.</p>

## Output

<p>For each test case on a separate line, print exactly $n$ non-negative integers — the elements of the array $a$ that Kristina originally had.</p><p>If there are several possible answers — output any of them.</p>





```input1|2,3,6,7,10,11,14,15,18,19,22,23
11
5
3 4 4 5
4
2 2 1
5
0 0 0 0
6
0 3 4 4 3
2
10
4
3 3 3
5
4 2 5 5
4
3 3 3
4
2 1 0
3
4 4
6
8 1 3 5 10
```




```output1
3 0 4 0 5
2 2 1 1
0 0 0 0 0
0 0 3 4 3 3
10 10
3 3 3 1
4 2 2 5 5
3 3 3 3
2 1 0 0
2 4 4
8 1 1 3 5 10
```



## Note

<p>The first test case is explained in the problem statement.</p><p>In the second test case, we can get array $b$ = [$2, 2, 1$] from the array $a$ = [$2, 2, 1, 1$]: </p><ul> <li> $b_1 = \max(a_1, a_2) = \max(2, 2) = 2$; </li><li> $b_2 = \max(a_2, a_3) = \max(2, 1) = 2$; </li><li> $b_3 = \max(a_3, a_4) = \max(1, 1) = 1$. </li></ul><p>In the third test case, all elements of the array $b$ are zeros. Since each $b_i$ is the maximum of two adjacent elements of array $a$, array $a$ can only consist entirely of zeros.</p><p>In the fourth test case, we can get array $b$ = [$0, 3, 4, 4, 3$] from the array $a$ = [$0, 0, 3, 4, 3, 3$] : </p><ul> <li> $b_1 = \max(a_1, a_2) = \max(0, 0) = 0$; </li><li> $b_2 = \max(a_2, a_3) = \max(0, 3) = 3$; </li><li> $b_3 = \max(a_3, a_4) = \max(3, 4) = 4$; </li><li> $b_4 = \max(a_4, a_5) = \max(4, 3) = 4$; </li><li> $b_5 = \max(a_5, a_6) = \max(3, 3) = 3$. </li></ul>
