## Description

<div><p>You have decided to open a new school. You have already found $n$ teachers and $m$ groups of students. The $i$-th group of students consists of $k_i \geq 2$ students. You know age of each teacher and each student. The ages of teachers are $a_1, a_2, \ldots, a_n$ and the ages of students of the $i$-th group are $b_{i, 1}, b_{i, 2}, \ldots, b_{i, k_i}$.</p><p>To <span class="tex-font-style-it">start lessons</span> you should assign the teacher to each group of students. Such assignment should satisfy the following requirements:</p><ul> <li> To each group exactly one teacher assigned. </li><li> To each teacher at most $1$ group of students assigned. </li><li> The average of students' ages in each group doesn't exceed the age of the teacher assigned to this group. </li></ul><p>The average of set $x_1, x_2, \ldots, x_k$ of $k$ integers is $\frac{x_1 + x_2 + \ldots + x_k}{k}$.</p><p>Recently you have heard that one of the students will refuse to study in your school. After this, the size of one group will decrease by $1$ while all other groups will remain unchanged.</p><p>You don't know who will refuse to study. For each student determine if you can start lessons in case of his refusal.</p><p>Note, that it is <span class="tex-font-style-bf">not guaranteed</span> that it is possible to start lessons before any refusal.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \leq t \leq 1000$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains two integers $n$ and $m$ ($1 \leq m \leq n \leq 10^5$)&nbsp;— the number of teachers and the number of groups of students.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \leq a_i \leq 10^5$)&nbsp;— the ages of teachers.</p><p>The next $2m$ lines contains descriptions of groups. </p><p>The first line of description of group contains a single integer $k_i$ ($2 \leq k_i \leq 10^5$)&nbsp;— the number of students in this group. </p><p>The second line of description of group contains $k_i$ integers $b_{i, 1}, b_{i, 2}, \ldots, b_{i, k_i}$ ($1 \leq b_{i, j} \leq 10^5$)&nbsp;— the ages of students of this group.</p><p>It is guaranteed that the total sum of $n$ over all test cases doesn't exceed $10^5$ and that the total sum of $k_1 + k_2 + \ldots + k_m$ over all test cases doesn't exceed $2 \cdot 10^5$</p></div><div class="output-specification"><p>For each test case output string of symbols $0$ and $1$ of length $k_1 + k_2 + \ldots + k_m$. The $i$-th symbol of this string should be equals $1$ if it is possible to start lessons in case of the $i$-th student refuse and it should be equals $0$ otherwise.</p><p>Students are numbered by integers from $1$ to $k_1 + k_2 + \ldots + k_m$ in the order they appear in the input. Thus, students of the $1$-st group are numbered by integers $1$, $2$, $\ldots$, $k_1$, students of the $2$-nd group are numbered by integers $k_1 + 1$, $k_1 + 2$, $\ldots$, $k_1 + k_2$ and so on.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \leq t \leq 1000$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains two integers $n$ and $m$ ($1 \leq m \leq n \leq 10^5$)&nbsp;— the number of teachers and the number of groups of students.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \leq a_i \leq 10^5$)&nbsp;— the ages of teachers.</p><p>The next $2m$ lines contains descriptions of groups. </p><p>The first line of description of group contains a single integer $k_i$ ($2 \leq k_i \leq 10^5$)&nbsp;— the number of students in this group. </p><p>The second line of description of group contains $k_i$ integers $b_{i, 1}, b_{i, 2}, \ldots, b_{i, k_i}$ ($1 \leq b_{i, j} \leq 10^5$)&nbsp;— the ages of students of this group.</p><p>It is guaranteed that the total sum of $n$ over all test cases doesn't exceed $10^5$ and that the total sum of $k_1 + k_2 + \ldots + k_m$ over all test cases doesn't exceed $2 \cdot 10^5$</p>

## Output

<p>For each test case output string of symbols $0$ and $1$ of length $k_1 + k_2 + \ldots + k_m$. The $i$-th symbol of this string should be equals $1$ if it is possible to start lessons in case of the $i$-th student refuse and it should be equals $0$ otherwise.</p><p>Students are numbered by integers from $1$ to $k_1 + k_2 + \ldots + k_m$ in the order they appear in the input. Thus, students of the $1$-st group are numbered by integers $1$, $2$, $\ldots$, $k_1$, students of the $2$-nd group are numbered by integers $k_1 + 1$, $k_1 + 2$, $\ldots$, $k_1 + k_2$ and so on.</p>





```input1|2,3,4,5
2
1 1
30
3
25 16 37
4 2
9 12 12 6
2
4 5
3
111 11 11
```




```output1
101
00100
```



## Note

<p>In the first test case there is one group of students with average age $\frac{25+16+37}{3}=26$ and one teacher with age $30$. There exists only one assignment that allows to start lessons.</p><p>If the student with age $16$ will refuse to study, the average age of students in this group will become $\frac{25+37}{2}=31$ so there won't be any assignment that allows to start lessons.</p><p>In the second test case it is impossible to start lessons initially. However, if the $3$-rd student with age $111$ will refuse to study, the average ages of groups will become $\frac{4 + 5}{2}=4.5$ and $\frac{11+11}{2} = 11$ correspondingly. Then it is possible to assing the first group to the first teacher and the second group to the third teacher.</p>
