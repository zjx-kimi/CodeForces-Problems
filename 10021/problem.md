## Description

<div><p>You are given an array $a_1, a_2, \ldots, a_n$.</p><p>In one move, you can perform either of the following two operations:</p><ul> <li> Choose an element from the array and remove it from the array. As a result, the length of the array decreases by $1$;</li><li> Choose an element from the array and increase its value by $1$. </li></ul><p>You can perform any number of moves. If the current array becomes empty, then no more moves can be made.</p><p>Your task is to find the <span class="tex-font-style-bf">minimum</span> number of moves required to make the sum of the elements of the array $a$ divisible by $3$. It is possible that you may need $0$ moves.</p><p>Note that the sum of the elements of an empty array (an array of length $0$) is equal to $0$.</p></div><div class="input-specification"><p>The first line of the input contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 10^5$).</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le 10^4$).</p><p>The sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output a single integer: the minimum number of moves.</p></div>

## Input

<p>The first line of the input contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 10^5$).</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le 10^4$).</p><p>The sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output a single integer: the minimum number of moves.</p>





```input1|2,3,6,7,10,11,14,15
8
4
2 2 5 4
3
1 3 2
4
3 7 6 8
1
1
4
2 2 4 2
2
5 5
7
2 4 8 1 9 3 4
2
4 10
```




```output1
1
0
0
1
1
2
1
1
```



## Note

<p>In the first test case, initially the array $a = [2, 2, 5, 4]$. One of the optimal ways to make moves is: </p><ul> <li> remove the current $4$th element and get $a = [2, 2, 5]$; </li></ul> As a result, the sum of the elements of the array $a$ will be divisible by $3$ (indeed, $a_1 + a_2 + a_3 = 2 + 2 + 5 = 9$).<p>In the second test case, initially, the sum of the array is $1+3+2 = 6$, which is divisible by $3$. Therefore, no moves are required. Hence, the answer is $0$.</p><p>In the fourth test case, initially, the sum of the array is $1$, which is not divisible by $3$. By removing its only element, you will get an empty array, so its sum is $0$. Hence, the answer is $1$.</p>
