## Description

<div><p>You have $n$ sticks, numbered from $1$ to $n$. The length of the $i$-th stick is $2^{a_i}$.</p><p>You want to choose <span class="tex-font-style-bf">exactly</span> $3$ sticks out of the given $n$ sticks, and form a <span class="tex-font-style-bf">non-degenerate</span> triangle out of them, using the sticks as the sides of the triangle. A triangle is called non-degenerate if its area is <span class="tex-font-style-bf">strictly</span> greater than $0$.</p><p>You have to calculate the number of ways to choose exactly $3$ sticks so that a triangle can be formed out of them. Note that the order of choosing sticks does not matter (for example, choosing the $1$-st, $2$-nd and $4$-th stick is the same as choosing the $2$-nd, $4$-th and $1$-st stick). </p></div><div class="input-specification"><p>The first line contains one integer $t$ ($1 \le t \le 10^4$) — the number of test cases.</p><p>Each test case consists of two lines:</p><ul> <li> the first line contains one integer $n$ ($1 \le n \le 3 \cdot 10^5$); </li><li> the second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($0 \le a_i \le n$). </li></ul><p>Additional constraint on the input: the sum of $n$ over all test cases does not exceed $3 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, print one integer — the number of ways to choose exactly $3$ sticks so that a triangle can be formed out of them.</p></div>

## Input

<p>The first line contains one integer $t$ ($1 \le t \le 10^4$) — the number of test cases.</p><p>Each test case consists of two lines:</p><ul> <li> the first line contains one integer $n$ ($1 \le n \le 3 \cdot 10^5$); </li><li> the second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($0 \le a_i \le n$). </li></ul><p>Additional constraint on the input: the sum of $n$ over all test cases does not exceed $3 \cdot 10^5$.</p>

## Output

<p>For each test case, print one integer — the number of ways to choose exactly $3$ sticks so that a triangle can be formed out of them.</p>





```input1|2,3,6,7
4
7
1 1 1 1 1 1 1
4
3 2 1 3
3
1 2 3
1
1
```




```output1
35
2
0
0
```



## Note

<p>In the first test case of the example, any three sticks out of the given $7$ can be chosen.</p><p>In the second test case of the example, you can choose the $1$-st, $2$-nd and $4$-th stick, or the $1$-st, $3$-rd and $4$-th stick.</p><p>In the third test case of the example, you cannot form a triangle out of the given sticks with lengths $2$, $4$ and $8$.</p>
