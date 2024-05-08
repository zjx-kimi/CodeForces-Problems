## Description

<div><p>You are given an array $a$ of $n$ integers. You are allowed to perform the following operation on it as many times as you want (0 or more times): </p><ul> <li> Choose $2$ indices $i$,$j$ where $1 \le i &lt; j \le n$ and replace $a_k$ for all $i \leq k \leq j$ with $|a_i - a_j|$ </li></ul><p>Print the maximum sum of all the elements of the final array that you can obtain in such a way.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^5$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains a single integer $n$ ($2 \le n \le 2 \cdot 10^5$)&nbsp;— the length of the array $a$.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le 10^9$)&nbsp;— the elements of array $a$.</p><p>It's guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, print the sum of the final array.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^5$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains a single integer $n$ ($2 \le n \le 2 \cdot 10^5$)&nbsp;— the length of the array $a$.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le 10^9$)&nbsp;— the elements of array $a$.</p><p>It's guaranteed that the sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, print the sum of the final array.</p>





```input1|2,3,6,7
3
3
1 1 1
2
9 1
3
4 9 5
```




```output1
3
16
18
```



## Note

<p>In the first test case, it is not possible to achieve a sum $&gt; 3$ by using these operations, therefore the maximum sum is $3$.</p><p>In the second test case, it can be shown that the maximum sum achievable is $16$. By using operation $(1,2)$ we transform the array from $[9,1]$ into $[8,8]$, thus the sum of the final array is $16$. </p><p>In the third test case, it can be shown that it is not possible to achieve a sum $&gt; 18$ by using these operations, therefore the maximum sum is $18$.</p>
