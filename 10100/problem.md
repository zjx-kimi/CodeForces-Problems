## Description

<div><p>Oleg received a permutation $a$ of length $n$ as a birthday present.</p><p>Oleg's friend Nechipor asks Oleg $q$ questions, each question is characterized by two numbers $l$ and $r$, in response to the question Oleg must say the number of sets of indices $(t_1, t_2, \ldots, t_k)$ of any length $k \ge 1$ such that: </p><ul> <li> $l \le t_i \le r$ for each $i$ from $1$ to $k$. </li><li> $t_i &lt; t_{i+1}$ for each $i$ from $1$ to $k-1$. </li><li> $a_{t_{i+1}}$ is divisible by $a_{t_i}$ for each $i$ from $1$ to $k-1$. </li></ul><p>Help Oleg and answer all of Nechipor's questions.</p></div><div class="input-specification"><p>Each test consists of several sets of input data. The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of sets of input data. The description of the sets of input data follows.</p><p>The first line of each set of input data contains two integers $n$ and $q$ ($1 \le n, q \le 10^6$)&nbsp;— the length of the permutation and the number of Nechipor's questions.</p><p>The second line of each set of input data contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le n$)&nbsp;— the permutation $a$ itself.</p><p>In each of the next $q$ lines of each set of input data, there are two integers $l$ and $r$ ($1 \le l \le r \le n$)&nbsp;— the next question of Nechipor.</p><p>It is guaranteed that the sum of the values of $n$ and the sum of the values of $q$ over all test cases does not exceed $10^6$.</p></div><div class="output-specification"><p>For each set of input data, output the answers to all of Nechipor's questions.</p></div>

## Input

<p>Each test consists of several sets of input data. The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of sets of input data. The description of the sets of input data follows.</p><p>The first line of each set of input data contains two integers $n$ and $q$ ($1 \le n, q \le 10^6$)&nbsp;— the length of the permutation and the number of Nechipor's questions.</p><p>The second line of each set of input data contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le n$)&nbsp;— the permutation $a$ itself.</p><p>In each of the next $q$ lines of each set of input data, there are two integers $l$ and $r$ ($1 \le l \le r \le n$)&nbsp;— the next question of Nechipor.</p><p>It is guaranteed that the sum of the values of $n$ and the sum of the values of $q$ over all test cases does not exceed $10^6$.</p>

## Output

<p>For each set of input data, output the answers to all of Nechipor's questions.</p>





```input1|2,3,4,5,6,7,8,9,10,11,15,16,17,18,19
4
8 8
2 1 6 3 5 4 8 7
1 8
2 8
1 7
1 6
1 3
5 8
4 4
2 3
1 1
1
1 1
3 3
3 2 1
1 2
1 3
2 3
8 1
1 2 3 4 5 6 7 8
1 8
```




```output1
20 15 18 12 5 5 1 3
1
2 3 2
27
```



## Note

<p>All suitable arrays in the first set of input data: ($1$), ($2$), ($3$), ($4$), ($5$), ($6$), ($7$), ($8$), ($1, 3$), ($1, 6$), ($1, 7$), ($1, 6, 7$), ($2, 3$), ($2, 4$), ($2, 5$), ($2, 6$), ($2, 7$), ($2, 8$), ($2, 6, 7$), ($6, 7$).</p><p>All suitable arrays in the fourth set of input data: ($1$), ($2$), ($3$), ($4$), ($5$), ($6$), ($7$), ($8$), ($1, 2$), ($1, 3$), ($1, 4$), ($1, 5$), ($1, 6$), ($1, 7$), ($1, 8$), ($1, 2, 4$), ($1, 2, 6$), ($1, 2, 8$), ($1, 2, 4, 8$), ($1, 3, 6$), ($1, 4, 8$), ($2, 4$), ($2, 6$), ($2, 8$), ($2, 4, 8$), ($3, 6$), ($4, 8$).</p>
