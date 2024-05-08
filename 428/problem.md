## Description

<div><p>The teachers of the Summer Informatics School decided to plant $n$ trees in a row, and it was decided to plant only oaks and firs. To do this, they made a plan, which can be represented as a binary string $s$ of length $n$. If $s_i = 0$, then the $i$-th tree in the row should be an oak, and if $s_i = 1$, then the $i$-th tree in the row should be a fir.</p><p>The day of tree planting is tomorrow, and the day after tomorrow an inspector will come to the School. The inspector loves nature very much, and he will evaluate the beauty of the row as follows:</p><ul> <li> First, he will calculate $l_0$ as the maximum number of consecutive oaks in the row (the maximum substring consisting of zeros in the plan $s$). If there are no oaks in the row, then $l_0 = 0$. </li><li> Then, he will calculate $l_1$ as the maximum number of consecutive firs in the row (the maximum substring consisting of ones in the plan $s$). If there are no firs in the row, then $l_1 = 0$. </li><li> Finally, he will calculate the <span class="tex-font-style-it">beauty</span> of the row as $a \cdot l_0 + l_1$ for some $a$&nbsp;— the inspector's favourite number. </li></ul><p>The teachers know the value of the parameter $a$, but for security reasons they cannot tell it to you. They only told you that $a$ is an integer from $1$ to $n$.</p><p>Since the trees have not yet been planted, the teachers decided to change the type of no more than $k$ trees to the opposite (i.e., change $s_i$ from $0$ to $1$ or from $1$ to $0$ in the plan) in order to maximize the beauty of the row of trees according to the inspector.</p><p>For each integer $j$ from $1$ to $n$ answer the following question <span class="tex-font-style-bf">independently</span>: </p><ul> <li> What is the maximum beauty of the row of trees that the teachers can achieve by changing the type of no more than $k$ trees if the inspector's favourite number $a$ is equal to $j$? </li></ul></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 1000$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains two integers $n$ and $k$ ($1 \le n \le 3000$, $0 \le k \le n$)&nbsp;— the number of trees in the row and the maximum number of changes.</p><p>The second line contains a string $s$ of length $n$, consisting of zeros and ones&nbsp;— the plan description.</p><p>It is guaranteed that the sum of all $n$ values for all test cases does not exceed $3000$.</p></div><div class="output-specification"><p>For each test case, print $n$ integers, the $j$-th ($1 \le j \le n$) of which is the maximum beauty of the row of trees after no more than $k$ changes if $a = j$ is used to calculate the beauty.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 1000$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains two integers $n$ and $k$ ($1 \le n \le 3000$, $0 \le k \le n$)&nbsp;— the number of trees in the row and the maximum number of changes.</p><p>The second line contains a string $s$ of length $n$, consisting of zeros and ones&nbsp;— the plan description.</p><p>It is guaranteed that the sum of all $n$ values for all test cases does not exceed $3000$.</p>

## Output

<p>For each test case, print $n$ integers, the $j$-th ($1 \le j \le n$) of which is the maximum beauty of the row of trees after no more than $k$ changes if $a = j$ is used to calculate the beauty.</p>





```input1|2,3,6,7,10,11
5
3 0
111
4 1
0110
5 0
10000
6 2
101101
7 1
0001101
```




```output1
3 3 3 
4 5 7 9 
5 9 13 17 21 
6 9 13 17 21 25 
7 10 13 17 21 25 29
```



## Note

<p>In the first test case no changes are allowed, so $l_0 = 0$ and $l_1 = 3$ always hold. Thus, regardless of the value of $a$, the beauty of the row of trees will be $3$.</p><p>In the second test case for $a \in \{1, 2\}$ the teachers can, for example, change the plan $s$ to $0111$ (by changing $s_4$), and for $a \in \{3, 4\}$&nbsp;— to $0010$ (by changing $s_2$). In this case, the beauty of the row for each $a$ is calculated as follows:</p><ul> <li> For $a = 1$: $l_0 = 1$, $l_1 = 3$. The beauty of the row is $1\cdot 1 + 3 = 4$. </li><li> For $a = 2$: $l_0 = 1$, $l_1 = 3$. The beauty of the row is $2\cdot 1 + 3 = 5$. </li><li> For $a = 3$: $l_0 = 2$, $l_1 = 1$. The beauty of the row is $3\cdot 2 + 1 = 7$. </li><li> For $a = 4$: $l_0 = 2$, $l_1 = 1$. The beauty of the row is $4\cdot 2 + 1 = 9$. </li></ul><p>It can be shown that the changes described above are optimal for all $a$ from $1$ to $4$.</p>
