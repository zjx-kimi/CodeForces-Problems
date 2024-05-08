## Description

<div><p>Karina has an array of $n$ integers $a_1, a_2, a_3, \dots, a_n$. She loves multiplying numbers, so she decided that the <span class="tex-font-style-it">beauty</span> of a pair of numbers is their product. And the <span class="tex-font-style-it">beauty</span> of an array is the maximum <span class="tex-font-style-it">beauty</span> of a pair of <span class="tex-font-style-bf">adjacent</span> elements in the array.</p><p>For example, for $n = 4$, $a=[3, 5, 7, 4]$, the <span class="tex-font-style-it">beauty</span> of the array is $\max$($3 \cdot 5$, $5 \cdot 7$, $7 \cdot 4$) = $\max$($15$, $35$, $28$) = $35$.</p><p>Karina wants her array to be as <span class="tex-font-style-it">beautiful</span> as possible. In order to achieve her goal, she can remove some elements (possibly zero) from the array. After Karina removes all elements she wants to, the array must contain at least two elements.</p><p>Unfortunately, Karina doesn't have enough time to do all her tasks, so she asks you to calculate the maximum <span class="tex-font-style-it">beauty</span> of the array that she can get by removing any number of elements (possibly zero).</p></div><div class="input-specification"><p>The first line of the input contains an integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. </p><p>The description of the test cases follows.</p><p>The first line of a test case contains an integer $n$ ($2 \le n \le 2 \cdot 10^5$)&nbsp;— the length of the array $a$.</p><p>The second line of a test case contains $n$ integers $a_1, a_2, a_3, \dots, a_n$ ($-10^9 \le a_i \le 10^9$)&nbsp;— the elements of the array $a$.</p><p>The sum of all values of $n$ across all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>Output $t$ integers, each of which is the answer to the corresponding test case&nbsp;— the maximum <span class="tex-font-style-it">beauty</span> of the array that Karina can get.</p></div>

## Input

<p>The first line of the input contains an integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. </p><p>The description of the test cases follows.</p><p>The first line of a test case contains an integer $n$ ($2 \le n \le 2 \cdot 10^5$)&nbsp;— the length of the array $a$.</p><p>The second line of a test case contains $n$ integers $a_1, a_2, a_3, \dots, a_n$ ($-10^9 \le a_i \le 10^9$)&nbsp;— the elements of the array $a$.</p><p>The sum of all values of $n$ across all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>Output $t$ integers, each of which is the answer to the corresponding test case&nbsp;— the maximum <span class="tex-font-style-it">beauty</span> of the array that Karina can get.</p>





```input1|2,3,6,7,10,11,14,15
7
4
5 0 2 1
3
-1 1 0
5
2 0 -1 -4 0
6
-8 4 3 7 1 -9
6
0 3 -2 5 -4 -4
2
1000000000 910000000
7
-1 -7 -2 -5 -4 -6 -3
```




```output1
10
0
4
72
16
910000000000000000
42
```



## Note

<p>In the first test case of the example, to get the maximum beauty, you need to remove the $2$-nd element.</p><p>In the second and third test cases of the example, there is no need to remove any elements to achieve maximum beauty.</p><p>In the fourth test case of the example, you need to leave only the first and last elements.</p>
