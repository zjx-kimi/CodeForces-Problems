## Description

<div><p><span class="tex-font-style-it"><span class="tex-font-style-bf">Please note that the time limit for this problem is only 0.5 seconds per test.</span></span></p><p>Vladislav wrote the integers from $1$ to $n$, inclusive, on the board. Then he replaced each integer with the sum of its digits.</p><p>What is the sum of the numbers on the board now?</p><p>For example, if $n=12$ then initially the numbers on the board are: $$1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12.$$ Then after the replacement, the numbers become: $$1, 2, 3, 4, 5, 6, 7, 8, 9, 1, 2, 3.$$ The sum of these numbers is $1+2+3+4+5+6+7+8+9+1+2+3=51$. Thus, for $n=12$ the answer is $51$.</p></div><div class="input-specification"><p>The first line contains an integer $t$ ($1 \leq t \leq 10^4$)&nbsp;— the number of test cases.</p><p>The only line of each test case contains a single integer $n$ ($1 \leq n \leq 2 \cdot 10^5$)&nbsp;— the largest number Vladislav writes.</p></div><div class="output-specification"><p>For each test case, output a single integer&nbsp;— the sum of the numbers at the end of the process.</p></div>

## Input

<p>The first line contains an integer $t$ ($1 \leq t \leq 10^4$)&nbsp;— the number of test cases.</p><p>The only line of each test case contains a single integer $n$ ($1 \leq n \leq 2 \cdot 10^5$)&nbsp;— the largest number Vladislav writes.</p>

## Output

<p>For each test case, output a single integer&nbsp;— the sum of the numbers at the end of the process.</p>





```input1|2,4,6,8
7
12
1
2
3
1434
2024
200000
```




```output1
51
1
3
6
18465
28170
4600002
```


