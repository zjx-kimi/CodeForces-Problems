## Description

<div><p>In a carnival game, there is a huge pyramid of cans with $2023$ rows, numbered in a regular pattern as shown.</p><center> <img class="tex-graphics" src="file://x7rym6Di.png" style="max-width: 100.0%;max-height: 100.0%;"><p><span class="tex-font-size-small">If can $9^2$ is hit initially, then all cans colored red in the picture above would fall.</span> </p></center><p>You throw a ball at the pyramid, and it hits a single can with number $n^2$. This causes all cans that are stacked on top of this can to fall (that is, can $n^2$ falls, then the cans directly above $n^2$ fall, then the cans directly above those cans, and so on). For example, the picture above shows the cans that would fall if can $9^2$ is hit.</p><p>What is the <span class="tex-font-style-bf">sum</span> of the numbers on all cans that fall? Recall that $n^2 = n \times n$.</p></div><div class="input-specification"><p>The first line contains an integer $t$ ($1 \leq t \leq 1000$)&nbsp;— the number of test cases.</p><p>The only line of each test case contains a single integer $n$ ($1 \leq n \leq 10^6$)&nbsp;— it means that the can you hit has label $n^2$.</p></div><div class="output-specification"><p>For each test case, output a single integer&nbsp;— the sum of the numbers on all cans that fall.</p><p>Please note, that the answer for some test cases won't fit into 32-bit integer type, so you should use at least 64-bit integer type in your programming language (like <span class="tex-font-style-tt">long long</span> for C++). For all valid inputs, the answer will always fit into 64-bit integer type.</p></div>

## Input

<p>The first line contains an integer $t$ ($1 \leq t \leq 1000$)&nbsp;— the number of test cases.</p><p>The only line of each test case contains a single integer $n$ ($1 \leq n \leq 10^6$)&nbsp;— it means that the can you hit has label $n^2$.</p>

## Output

<p>For each test case, output a single integer&nbsp;— the sum of the numbers on all cans that fall.</p><p>Please note, that the answer for some test cases won't fit into 32-bit integer type, so you should use at least 64-bit integer type in your programming language (like <span class="tex-font-style-tt">long long</span> for C++). For all valid inputs, the answer will always fit into 64-bit integer type.</p>





```input1|2,4,6,8,10
10
9
1
2
3
4
5
6
10
1434
1000000
```




```output1
156
1
5
10
21
39
46
146
63145186
58116199242129511
```



## Note

<p>The first test case is pictured in the statement. The sum of the numbers that fall is $$1^2 + 2^2 + 3^2 + 5^2 + 6^2 + 9^2 = 1 + 4 + 9 + 25 + 36 + 81 = 156.$$</p><p>In the second test case, only the can labeled $1^2$ falls, so the answer is $1^2=1$.</p><p>In the third test case, the cans labeled $1^2$ and $2^2$ fall, so the answer is $1^2+2^2=1+4=5$.</p><p>In the fourth test case, the cans labeled $1^2$ and $3^2$ fall, so the answer is $1^2+3^2=1+9=10$.</p><p>In the fifth test case, the cans labeled $1^2$, $2^2$, and $4^2$ fall, so the answer is $1^2+2^2+4^2=1+4+16=21$.</p>
