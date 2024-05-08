## Description

<div><p>Alphen has an array of positive integers $a$ of length $n$.</p><p>Alphen can perform the following operation: </p><ul> <li> For <span class="tex-font-style-bf">all</span> $i$ from $1$ to $n$, replace $a_i$ with $\max(0, a_i - 1)$. </li></ul><p>Alphen will perform the above operation until $a$ is sorted, that is $a$ satisfies $a_1 \leq a_2 \leq \ldots \leq a_n$. How many operations will Alphen perform? Under the constraints of the problem, it can be proven that Alphen will perform a finite number of operations.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line of input contains a single integer $t$ ($1 \le t \le 500$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2 \le n \le 50$)&nbsp;— the length of the array $a$.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le 10 ^ 9$)&nbsp;— the elements of the array $a$.</p></div><div class="output-specification"><p>For each test case, output a single integer&nbsp;— the number of operations that Alphen will perform.</p></div>

## Input

<p>Each test contains multiple test cases. The first line of input contains a single integer $t$ ($1 \le t \le 500$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2 \le n \le 50$)&nbsp;— the length of the array $a$.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le 10 ^ 9$)&nbsp;— the elements of the array $a$.</p>

## Output

<p>For each test case, output a single integer&nbsp;— the number of operations that Alphen will perform.</p>





```input1|2,3,6,7,10,11,14,15
7
3
1 2 3
5
2 1 2 1 2
4
3 1 5 4
2
7 7
5
4 1 3 2 5
5
2 3 1 4 5
3
1000000000 1 2
```




```output1
0
2
5
0
4
3
1000000000
```



## Note

<p>In the first test case, we have $a=[1,2,3]$. Since $a$ is already sorted, Alphen will not need to perform any operations. So, the answer is $0$.</p><p>In the second test case, we have $a=[2,1,2,1,2]$. Since $a$ is not initially sorted, Alphen will perform one operation to make $a=[1,0,1,0,1]$. After performing one operation, $a$ is still not sorted, so Alphen will perform another operation to make $a=[0,0,0,0,0]$. Since $a$ is sorted, Alphen will not perform any other operations. Since Alphen has performed two operations in total, the answer is $2$.</p>
