## Description

<div><p>You have an array $a$ of $n$ integers.</p><p>You perform exactly $k$ operations on it. In one operation, you select any contiguous subarray of the array $a$ (possibly empty) and insert the sum of this subarray anywhere in the array.</p><p>Your task is to find the maximum possible sum of the array after $k$ such operations.</p><p>As this number can be very large, output the answer modulo $10^9 + 7$.</p><p>Reminder: the remainder of a number $x$ modulo $p$ is the smallest non-negative $y$ such that there exists an integer $q$ and $x = p \cdot q + y$.</p></div><div class="input-specification"><p>Each test consists of several test cases. The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. Then follows the description of the test cases.</p><p>The first line of each test case contains two integers $n$ and $k$ ($1 \le n, k \le 2 \cdot 10^5$)&nbsp;— the length of the array $a$ and the number of operations, respectively.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($-10^9 \le a_i \le 10^9$)&nbsp;— the array $a$ itself.</p><p>It is guaranteed that the sum of the values of $n$ and $k$ for all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test, output a single integer&nbsp;— the maximum sum of the array that can be obtained after $k$ operations modulo $10^9 + 7$.</p></div>

## Input

<p>Each test consists of several test cases. The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. Then follows the description of the test cases.</p><p>The first line of each test case contains two integers $n$ and $k$ ($1 \le n, k \le 2 \cdot 10^5$)&nbsp;— the length of the array $a$ and the number of operations, respectively.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($-10^9 \le a_i \le 10^9$)&nbsp;— the array $a$ itself.</p><p>It is guaranteed that the sum of the values of $n$ and $k$ for all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test, output a single integer&nbsp;— the maximum sum of the array that can be obtained after $k$ operations modulo $10^9 + 7$.</p>





```input1|2,3,6,7,10,11,14,15,18,19,22,23
12
2 2
-4 -7
3 3
2 2 8
1 7
7
5 1
4 -2 8 -12 9
7 4
8 14 -9 6 0 -1 3
7 100
5 3 -8 12 -5 -9 3
6 1000
-1000000000 -1000000000 -1000000000 -1000000000 -1000000000 -1000000000
2 1
1000000000 8
5 4
0 0 0 0 0
6 10
48973 757292 58277 -38574 27475 999984
7 1
-1000 1000 -1000 1000 -1000 1000 -1000
10 10050
408293874 -3498597 7374783 295774930 -48574034 26623784 498754833 -294875830 283045804 85938045
```




```output1
999999996
96
896
17
351
716455332
42
2
0
897909241
0
416571966
```



## Note

<p>In the first test case, it is advantageous to take an empty subarray of the array twice and insert the sum of the empty subarray (zero) anywhere, then the sum of the resulting array will be $(-4) + (-7) + 0 + 0 = -11$, modulo $10^9 + 7$ this is $999\,999\,996$.</p><p>In the second test case, it is advantageous to take the sum of the entire array three times and place it anywhere in the array, then one of the possible sequences of actions: [$2, 2, 8$] $\rightarrow$ [$2, 2, 8, 12$] $\rightarrow$ [$2, 2, 8, 12, 24$] $\rightarrow$ [$2, 2, 8, 12, 24, 48$], the sum of the final array is $2 + 2 + 8 + 12 + 24 + 48 = 96$.</p><p>In the fourth test case, it is advantageous to take a subarray of the array consisting of the first three numbers (i.e. consisting of the numbers $4, -2$ and $8$) and insert its sum at the beginning of the array, thereby obtaining the array [$10, 4, -2, 8, -12, 9$], the sum of this array is $17$.</p><p>In the seventh test case, it will always be advantageous for us to take an empty subarray of the array. In this case, the sum of the resulting array will not differ from the sum of the original. The answer will be the sum of the original array, taken modulo&nbsp;— $42$, because $(-6 \cdot (10^9 + 7) + 42 = -6\,000\,000\,000)$.</p>
