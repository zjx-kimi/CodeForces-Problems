## Description

<div><p>Once upon a time Mike and Mike decided to come up with an outstanding problem for some stage of ROI (rare olympiad in informatics). One of them came up with a problem prototype but another stole the idea and proposed that problem for another stage of the same olympiad. Since then the first Mike has been waiting for an opportunity to propose the original idea for some other contest... Mike waited until this moment!</p><p>You are given an array $a$ of $n$ integers. You are also given $q$ queries of two types:</p><ul> <li> Replace $i$-th element in the array with integer $x$. </li><li> Replace each element in the array with integer $x$. </li></ul><p>After performing each query you have to calculate the sum of all elements in the array.</p></div><div class="input-specification"><p>The first line contains two integers $n$ and $q$ ($1 \le n, q \le 2 \cdot 10^5$)&nbsp;— the number of elements in the array and the number of queries, respectively.</p><p>The second line contains $n$ integers $a_1, \ldots, a_n$ ($1 \le a_i \le 10^9$)&nbsp;— elements of the array $a$.</p><p>Each of the following $q$ lines contains a description of the corresponding query. Description begins with integer $t$ ($t \in \{1, 2\}$) which denotes a type of the query:</p><ul> <li> If $t = 1$, then two integers $i$ and $x$ are following ($1 \le i \le n$, $1 \le x \le 10^9$)&nbsp;— position of replaced element and it's new value. </li><li> If $t = 2$, then integer $x$ is following ($1 \le x \le 10^9$)&nbsp;— new value of each element in the array. </li></ul></div><div class="output-specification"><p>Print $q$ integers, each on a separate line. In the $i$-th line print the sum of all elements in the array after performing the first $i$ queries.</p></div>

## Input

<p>The first line contains two integers $n$ and $q$ ($1 \le n, q \le 2 \cdot 10^5$)&nbsp;— the number of elements in the array and the number of queries, respectively.</p><p>The second line contains $n$ integers $a_1, \ldots, a_n$ ($1 \le a_i \le 10^9$)&nbsp;— elements of the array $a$.</p><p>Each of the following $q$ lines contains a description of the corresponding query. Description begins with integer $t$ ($t \in \{1, 2\}$) which denotes a type of the query:</p><ul> <li> If $t = 1$, then two integers $i$ and $x$ are following ($1 \le i \le n$, $1 \le x \le 10^9$)&nbsp;— position of replaced element and it's new value. </li><li> If $t = 2$, then integer $x$ is following ($1 \le x \le 10^9$)&nbsp;— new value of each element in the array. </li></ul>

## Output

<p>Print $q$ integers, each on a separate line. In the $i$-th line print the sum of all elements in the array after performing the first $i$ queries.</p>





```input1
5 5
1 2 3 4 5
1 1 5
2 10
1 5 11
1 4 1
2 1
```




```output1
19
50
51
42
5
```



## Note

<p>Consider array from the example and the result of performing each query:</p><ol> <li> Initial array is $[1, 2, 3, 4, 5]$. </li><li> After performing the first query, array equals to $[5, 2, 3, 4, 5]$. The sum of all elements is $19$. </li><li> After performing the second query, array equals to $[10, 10, 10, 10, 10]$. The sum of all elements is $50$. </li><li> After performing the third query, array equals to $[10, 10, 10, 10, 11$]. The sum of all elements is $51$. </li><li> After performing the fourth query, array equals to $[10, 10, 10, 1, 11]$. The sum of all elements is $42$. </li><li> After performing the fifth query, array equals to $[1, 1, 1, 1, 1]$. The sum of all elements is $5$. </li></ol>
