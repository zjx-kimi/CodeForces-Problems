## Description

<div><p>You are given a binary string $s$. A binary string is a string consisting of characters <span class="tex-font-style-tt">0</span> and/or <span class="tex-font-style-tt">1</span>.</p><p>You can perform the following operation on $s$ any number of times <span class="tex-font-style-bf">(even zero)</span>:</p><ul> <li> choose an integer $i$ such that $1 \le i \le |s|$, then erase the character $s_i$. </li></ul><p>You have to make $s$ alternating, i. e. after you perform the operations, every two adjacent characters in $s$ should be different.</p><p>Your goal is to calculate two values:</p><ul> <li> the minimum number of operations required to make $s$ alternating; </li><li> the number of different <span class="tex-font-style-bf">shortest</span> sequences of operations that make $s$ alternating. Two sequences of operations are different if in at least one operation, the chosen integer $i$ is different in these two sequences. </li></ul></div><div class="input-specification"><p>The first line contains one integer $t$ ($1 \le t \le 10^4$) — the number of test cases.</p><p>Each test case consists of one line containing the string $s$ ($1 \le |s| \le 2 \cdot 10^5$). The string $s$ consists of characters <span class="tex-font-style-tt">0</span> and/or <span class="tex-font-style-tt">1</span> only.</p><p>Additional constraint on the input:</p><ul> <li> the total length of strings $s$ over all test cases does not exceed $2 \cdot 10^5$. </li></ul></div><div class="output-specification"><p>For each test case, print two integers: the minimum number of operations you have to perform, and the number of different shortest sequences of operations. Since the second number might be large, print its remainder modulo $998244353$.</p></div>

## Input

<p>The first line contains one integer $t$ ($1 \le t \le 10^4$) — the number of test cases.</p><p>Each test case consists of one line containing the string $s$ ($1 \le |s| \le 2 \cdot 10^5$). The string $s$ consists of characters <span class="tex-font-style-tt">0</span> and/or <span class="tex-font-style-tt">1</span> only.</p><p>Additional constraint on the input:</p><ul> <li> the total length of strings $s$ over all test cases does not exceed $2 \cdot 10^5$. </li></ul>

## Output

<p>For each test case, print two integers: the minimum number of operations you have to perform, and the number of different shortest sequences of operations. Since the second number might be large, print its remainder modulo $998244353$.</p>





```input1|2,4
3
10010
111
0101
```




```output1
1 2
2 6
0 1
```



## Note

<p>In the first test case of the example, the shortest sequences of operations are:</p><ul> <li> $[2]$ (delete the $2$-nd character); </li><li> $[3]$ (delete the $3$-rd character). </li></ul><p>In the second test case of the example, the shortest sequences of operations are: </p><ul> <li> $[2, 1]$ (delete the $2$-nd character, then delete the $1$-st character); </li><li> $[2, 2]$; </li><li> $[1, 1]$; </li><li> $[1, 2]$; </li><li> $[3, 1]$; </li><li> $[3, 2]$. </li></ul><p>In the third test case of the example, the only shortest sequence of operations is $[]$ (empty sequence).</p>
