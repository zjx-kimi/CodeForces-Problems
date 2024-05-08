## Description

<div><p>You are given a sequence of $n$ digits $d_1d_2 \dots d_{n}$. You need to paint all the digits in two colors so that:</p><ul> <li> each digit is painted either in the color $1$ or in the color $2$; </li><li> if you write in a row from left to right all the digits painted in the color $1$, and then after them all the digits painted in the color $2$, then the resulting sequence of $n$ digits will be non-decreasing (that is, each next digit will be greater than or equal to the previous digit). </li></ul><p>For example, for the sequence $d=914$ the only valid coloring is $211$ (paint in the color $1$ two last digits, paint in the color $2$ the first digit). But $122$ is not a valid coloring ($9$ concatenated with $14$ is not a non-decreasing sequence).</p><p>It is allowed that either of the two colors is not used at all. Digits painted in the same color are not required to have consecutive positions.</p><p>Find any of the valid ways to paint the given sequence of digits or determine that it is impossible to do.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10000$) — the number of test cases in the input.</p><p>The first line of each test case contains an integer $n$ ($1 \le n \le 2\cdot10^5$) — the length of a given sequence of digits.</p><p>The next line contains a sequence of $n$ digits $d_1d_2 \dots d_{n}$ ($0 \le d_i \le 9$). The digits are written in a row without spaces or any other separators. The sequence can start with <span class="tex-font-style-tt">0</span>.</p><p>It is guaranteed that the sum of the values ​​of $n$ for all test cases in the input does not exceed $2\cdot10^5$.</p></div><div class="output-specification"><p>Print $t$ lines — the answers to each of the test cases in the input.</p><p>If there is a solution for a test case, the corresponding output line should contain any of the valid colorings written as a string of $n$ digits $t_1t_2 \dots t_n$ ($1 \le t_i \le 2$), where $t_i$ is the color the $i$-th digit is painted in. If there are several feasible solutions, print any of them.</p><p>If there is no solution, then the corresponding output line should contain a single character '<span class="tex-font-style-tt">-</span>' (the minus sign).</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10000$) — the number of test cases in the input.</p><p>The first line of each test case contains an integer $n$ ($1 \le n \le 2\cdot10^5$) — the length of a given sequence of digits.</p><p>The next line contains a sequence of $n$ digits $d_1d_2 \dots d_{n}$ ($0 \le d_i \le 9$). The digits are written in a row without spaces or any other separators. The sequence can start with <span class="tex-font-style-tt">0</span>.</p><p>It is guaranteed that the sum of the values ​​of $n$ for all test cases in the input does not exceed $2\cdot10^5$.</p>

## Output

<p>Print $t$ lines — the answers to each of the test cases in the input.</p><p>If there is a solution for a test case, the corresponding output line should contain any of the valid colorings written as a string of $n$ digits $t_1t_2 \dots t_n$ ($1 \le t_i \le 2$), where $t_i$ is the color the $i$-th digit is painted in. If there are several feasible solutions, print any of them.</p><p>If there is no solution, then the corresponding output line should contain a single character '<span class="tex-font-style-tt">-</span>' (the minus sign).</p>





```input1
5
12
040425524644
1
0
9
123456789
2
98
3
987
```




```output1
121212211211
1
222222222
21
-
```



## Note

<p>In the first test case, $d=040425524644$. The output $t=121212211211$ is correct because $0022444$ (painted in $1$) concatenated with $44556$ (painted in $2$) is $002244444556$ which is a sorted sequence of $n$ given digits.</p>
