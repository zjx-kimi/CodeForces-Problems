## Description

<div><p>You are given an array $b_1, b_2, \ldots, b_n$.</p><p>An anonymous informant has told you that the array $b$ was obtained as follows: initially, there existed an array $a_1, a_2, \ldots, a_n$, after which the following two-component operation was performed $k$ times:</p><ol><li> A fixed point$^{\dagger}$ $x$ of the array $a$ was chosen.</li><li> Then, the array $a$ was cyclically shifted to the left$^{\ddagger}$ exactly $x$ times.</li></ol><p>As a result of $k$ such operations, the array $b_1, b_2, \ldots, b_n$ was obtained. You want to check if the words of the anonymous informant can be true or if they are guaranteed to be false.</p><p>$^{\dagger}$A number $x$ is called a fixed point of the array $a_1, a_2, \ldots, a_n$ if $1 \leq x \leq n$ and $a_x = x$.</p><p>$^{\ddagger}$A cyclic left shift of the array $a_1, a_2, \ldots, a_n$ is the array $a_2, \ldots, a_n, a_1$.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains an integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains two integers $n, k$ ($1 \le n \le 2 \cdot 10^5$, $1 \le k \le 10^9$)&nbsp;— the length of the array $b$ and the number of operations performed.</p><p>The second line of each test case contains $n$ integers $b_1, b_2, \ldots, b_n$ ($1 \le b_i \le 10^9$)&nbsp;— the elements of the array $b$.</p><p>It is guaranteed that the sum of the values of $n$ for all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output "<span class="tex-font-style-tt">Yes</span>" if the words of the anonymous informant can be true, and "<span class="tex-font-style-tt">No</span>" if they are guaranteed to be false.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains an integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains two integers $n, k$ ($1 \le n \le 2 \cdot 10^5$, $1 \le k \le 10^9$)&nbsp;— the length of the array $b$ and the number of operations performed.</p><p>The second line of each test case contains $n$ integers $b_1, b_2, \ldots, b_n$ ($1 \le b_i \le 10^9$)&nbsp;— the elements of the array $b$.</p><p>It is guaranteed that the sum of the values of $n$ for all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output "<span class="tex-font-style-tt">Yes</span>" if the words of the anonymous informant can be true, and "<span class="tex-font-style-tt">No</span>" if they are guaranteed to be false.</p>





```input1|2,3,6,7,10,11
6
5 3
4 3 3 2 3
3 100
7 2 1
5 5
6 1 1 1 1
1 1000000000
1
8 48
9 10 11 12 13 14 15 8
2 1
1 42
```




```output1
Yes
Yes
No
Yes
Yes
No
```



## Note

<p>In the first test case, the array $a$ could be equal to $[3, 2, 3, 4, 3]$. In the first operation, a fixed point $x = 2$ was chosen, and after $2$ left shifts, the array became $[3, 4, 3, 3, 2]$. In the second operation, a fixed point $x = 3$ was chosen, and after $3$ left shifts, the array became $[3, 2, 3, 4, 3]$. In the third operation, a fixed point $x = 3$ was chosen again, and after $3$ left shifts, the array became $[4, 3, 3, 2, 3]$, which is equal to the array $b$.</p><p>In the second test case, the array $a$ could be equal to $[7, 2, 1]$. After the operation with a fixed point $x = 2$, the array became $[1, 7, 2]$. Then, after the operation with a fixed point $x = 1$, the array returned to its initial state $[7, 2, 1]$. These same $2$ operations (with $x = 2$, and $x = 1$) were repeated $49$ times. So, after $100$ operations, the array returned to $[7, 2, 1]$.</p><p>In the third test case, it can be shown that there is no solution.</p>
