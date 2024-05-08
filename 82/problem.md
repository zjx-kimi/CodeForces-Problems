## Description

<div><p>There are $n$ people on the number line; the $i$-th person is at point $a_i$ and wants to go to point $b_i$. For each person, $a_i &lt; b_i$, and the starting and ending points of all people are distinct. (That is, all of the $2n$ numbers $a_1, a_2, \dots, a_n, b_1, b_2, \dots, b_n$ are distinct.) </p><p>All the people will start moving simultaneously at a speed of $1$ unit per second until they reach their final point $b_i$. When two people meet at the same point, they will greet each other once. How many greetings will there be?</p><p>Note that a person can still greet other people even if they have reached their final point.</p></div><div class="input-specification"><p>The first line of the input contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$)&nbsp;— the number of people.</p><p>Then $n$ lines follow, the $i$-th of which contains two integers $a_i$ and $b_i$ ($-10^9 \leq a_i &lt; b_i \leq 10^9$)&nbsp;— the starting and ending positions of each person.</p><p>For each test case, all of the $2n$ numbers $a_1, a_2, \dots, a_n, b_1, b_2, \dots, b_n$ are distinct.</p><p>The sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output a single integer denoting the number of greetings that will happen.</p></div>

## Input

<p>The first line of the input contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 2 \cdot 10^5$)&nbsp;— the number of people.</p><p>Then $n$ lines follow, the $i$-th of which contains two integers $a_i$ and $b_i$ ($-10^9 \leq a_i &lt; b_i \leq 10^9$)&nbsp;— the starting and ending positions of each person.</p><p>For each test case, all of the $2n$ numbers $a_1, a_2, \dots, a_n, b_1, b_2, \dots, b_n$ are distinct.</p><p>The sum of $n$ over all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output a single integer denoting the number of greetings that will happen.</p>





```input1|2,3,4,12,13,14,15,16,23,24,25,26,27
5
2
2 3
1 4
6
2 6
3 9
4 5
1 8
7 10
-2 100
4
-10 10
-5 5
-12 12
-13 13
5
-4 9
-2 5
3 4
6 7
8 10
4
1 2
3 4
5 6
7 8
```




```output1
1
9
6
4
0
```



## Note

<p>In the first test case, the two people will meet at point $3$ and greet each other.</p>
