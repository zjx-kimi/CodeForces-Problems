## Description

<div><p>You are given a binary string $s$ consisting of only characters <span class="tex-font-style-tt">0</span> and/or <span class="tex-font-style-tt">1</span>.</p><p>You can perform several operations on this string (possibly zero). There are two types of operations: </p><ul> <li> choose two consecutive elements and swap them. In order to perform this operation, you pay $10^{12}$ coins; </li><li> choose any element from the string and remove it. In order to perform this operation, you pay $10^{12}+1$ coins. </li></ul><p>Your task is to calculate the minimum number of coins required to sort the string $s$ in non-decreasing order (i. e. transform $s$ so that $s_1 \le s_2 \le \dots \le s_m$, where $m$ is the length of the string after applying all operations). An empty string is also considered sorted in non-decreasing order.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The only line of each test case contains the string $s$ ($1 \le |s| \le 3 \cdot 10^5$), consisting of only characters <span class="tex-font-style-tt">0</span> and/or <span class="tex-font-style-tt">1</span>.</p><p>The sum of lengths of all given strings doesn't exceed $3 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, print a single integer&nbsp;— the minimum number of coins required to sort the string $s$ in non-decreasing order.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The only line of each test case contains the string $s$ ($1 \le |s| \le 3 \cdot 10^5$), consisting of only characters <span class="tex-font-style-tt">0</span> and/or <span class="tex-font-style-tt">1</span>.</p><p>The sum of lengths of all given strings doesn't exceed $3 \cdot 10^5$.</p>

## Output

<p>For each test case, print a single integer&nbsp;— the minimum number of coins required to sort the string $s$ in non-decreasing order.</p>





```input1|2,4,6
6
100
0
0101
00101101
1001101
11111
```




```output1
1000000000001
0
1000000000000
2000000000001
2000000000002
0
```



## Note

<p>In the first example, you have to remove the $1$-st element, so the string becomes equal to <span class="tex-font-style-tt">00</span>.</p><p>In the second example, the string is already sorted.</p><p>In the third example, you have to swap the $2$-nd and the $3$-rd elements, so the string becomes equal to <span class="tex-font-style-tt">0011</span>.</p><p>In the fourth example, you have to swap the $3$-rd and the $4$-th elements, so the string becomes equal to <span class="tex-font-style-tt">00011101</span>, and then remove the $7$-th element, so the string becomes equal to <span class="tex-font-style-tt">0001111</span>.</p><p>In the fifth example, you have to remove the $1$-st element, so the string becomes equal to <span class="tex-font-style-tt">001101</span>, and then remove the $5$-th element, so the string becomes equal to <span class="tex-font-style-tt">00111</span>.</p><p>In the sixth example, the string is already sorted.</p>
