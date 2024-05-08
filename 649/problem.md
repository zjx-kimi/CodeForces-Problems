## Description

<div><p>A sequence is <span class="tex-font-style-it">almost-increasing</span> if it does not contain three <span class="tex-font-style-bf">consecutive</span> elements $x, y, z$ such that $x\ge y\ge z$.</p><p>You are given an array $a_1, a_2, \dots, a_n$ and $q$ queries.</p><p>Each query consists of two integers $1\le l\le r\le n$. For each query, find the length of the longest <span class="tex-font-style-it">almost-increasing</span> subsequence of the subarray $a_l, a_{l+1}, \dots, a_r$. </p><p>A subsequence is a sequence that can be derived from the given sequence by deleting zero or more elements without changing the order of the remaining elements.</p></div><div class="input-specification"><p>The first line of input contains two integers, $n$ and $q$ ($1 \leq n, q \leq 200\,000$) &nbsp;— the length of the array $a$ and the number of queries.</p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \leq a_i \leq 10^9$) &nbsp;— the values of the array $a$.</p><p>Each of the next $q$ lines contains the description of a query. Each line contains two integers $l$ and $r$ ($1 \leq l \leq r \leq n$) &nbsp;— the query is about the subarray $a_l, a_{l+1}, \dots, a_r$.</p></div><div class="output-specification"><p>For each of the $q$ queries, print a line containing the length of the longest almost-increasing subsequence of the subarray $a_l, a_{l+1}, \dots, a_r$.</p></div>

## Input

<p>The first line of input contains two integers, $n$ and $q$ ($1 \leq n, q \leq 200\,000$) &nbsp;— the length of the array $a$ and the number of queries.</p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \leq a_i \leq 10^9$) &nbsp;— the values of the array $a$.</p><p>Each of the next $q$ lines contains the description of a query. Each line contains two integers $l$ and $r$ ($1 \leq l \leq r \leq n$) &nbsp;— the query is about the subarray $a_l, a_{l+1}, \dots, a_r$.</p>

## Output

<p>For each of the $q$ queries, print a line containing the length of the longest almost-increasing subsequence of the subarray $a_l, a_{l+1}, \dots, a_r$.</p>





```input1
9 8
1 2 4 3 3 5 6 2 1
1 3
1 4
2 5
6 6
3 7
7 8
1 8
8 8
```




```output1
3
4
3
1
4
2
7
1
```



## Note

<p>In the first query, the subarray is $a_1, a_2, a_3 = [1,2,4]$. The whole subarray is almost-increasing, so the answer is $3$.</p><p>In the second query, the subarray is $a_1, a_2, a_3,a_4 = [1,2,4,3]$. The whole subarray is a almost-increasing, because there are no three consecutive elements such that $x \geq y \geq z$. So the answer is $4$.</p><p>In the third query, the subarray is $a_2, a_3, a_4, a_5 = [2, 4, 3, 3]$. The whole subarray is not almost-increasing, because the last three elements satisfy $4 \geq 3 \geq 3$. An almost-increasing subsequence of length $3$ can be found (for example taking $a_2,a_3,a_5 = [2,4,3]$ ). So the answer is $3$.</p>
