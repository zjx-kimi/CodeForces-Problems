## Description

<div><p>There is an array $a$ consisting of non-negative integers. You can choose an integer $x$ and denote $b_i=a_i \oplus x$ for all $1 \le i \le n$, where $\oplus$ denotes the <a href="https://en.wikipedia.org/wiki/Bitwise_operation#XOR">bitwise XOR operation</a>. Is it possible to choose such a number $x$ that the value of the expression $b_1 \oplus b_2 \oplus \ldots \oplus b_n$ equals $0$?</p><p>It can be shown that if a valid number $x$ exists, then there also exists $x$ such that ($0 \le x &lt; 2^8$).</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 1000$). The description of the test cases follows.</p><p>The first line of the test case contains one integer $n$ ($1 \le n \le 10^3$)&nbsp;— the length of the array $a$.</p><p>The second line of the test case contains $n$ integers&nbsp;— array $a$ ($0 \le a_i &lt; 2^8$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^3$.</p></div><div class="output-specification"><p>For each set test case, print the integer $x$ ($0 \le x &lt; 2^8$) if it exists, or $-1$ otherwise.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 1000$). The description of the test cases follows.</p><p>The first line of the test case contains one integer $n$ ($1 \le n \le 10^3$)&nbsp;— the length of the array $a$.</p><p>The second line of the test case contains $n$ integers&nbsp;— array $a$ ($0 \le a_i &lt; 2^8$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^3$.</p>

## Output

<p>For each set test case, print the integer $x$ ($0 \le x &lt; 2^8$) if it exists, or $-1$ otherwise.</p>





```input1|2,3,6,7,10,11
5
3
1 2 5
3
1 2 3
4
0 1 2 3
4
1 2 2 3
1
1
```




```output1
6
0
3
-1
1
```



## Note

<p>In the first test case, after applying the operation with the number $6$ the array $b$ becomes $[7, 4, 3]$, $7 \oplus 4 \oplus 3 = 0$.</p><p>There are other answers in the third test case, such as the number $0$. </p>
