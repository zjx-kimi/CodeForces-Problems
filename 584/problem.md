## Description

<div><p>You are given two arrays $a$ and $b$, both of length $n$.</p><p>Your task is to count the number of pairs of integers $(i,j)$ such that $1 \leq i &lt; j \leq n$ and $a_i \cdot a_j = b_i+b_j$.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line of input contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2 \le n \le 2 \cdot 10^5$)&nbsp;— the length of the arrays.</p><p>The second line of each test case contains $n$ integers $a_1,a_2,\ldots,a_n$ ($1 \le a_i \le n$)&nbsp;— the elements of array $a$.</p><p>The third line of each test case contains $n$ integers $b_1,b_2,\ldots,b_n$ ($1 \le b_i \le n$)&nbsp;— the elements of array $b$.</p><p>It is guaranteed that the sum of $n$ across all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output the number of good pairs.</p></div>

## Input

<p>Each test contains multiple test cases. The first line of input contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2 \le n \le 2 \cdot 10^5$)&nbsp;— the length of the arrays.</p><p>The second line of each test case contains $n$ integers $a_1,a_2,\ldots,a_n$ ($1 \le a_i \le n$)&nbsp;— the elements of array $a$.</p><p>The third line of each test case contains $n$ integers $b_1,b_2,\ldots,b_n$ ($1 \le b_i \le n$)&nbsp;— the elements of array $b$.</p><p>It is guaranteed that the sum of $n$ across all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output the number of good pairs.</p>





```input1|2,3,4,8,9,10
3
3
2 3 2
3 3 1
8
4 2 8 2 1 2 7 5
3 5 8 8 1 1 6 5
8
4 4 8 8 8 8 8 8
8 8 8 8 8 8 8 8
```




```output1
2
7
1
```



## Note

<p>In the first sample, there are $2$ good pairs:</p><ul> <li> $(1,2)$, </li><li> $(1,3)$. </li></ul><p>In the second sample, there are $7$ good pairs:</p><ul> <li> $(1,2)$, </li><li> $(1,5)$, </li><li> $(2,8)$, </li><li> $(3,4)$, </li><li> $(4,7)$, </li><li> $(5,6)$, </li><li> $(5,7)$. </li></ul>
