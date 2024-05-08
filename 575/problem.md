## Description

<div><p>For an array of integers $[a_1, a_2, \dots, a_n]$, let's call the value $|a_1-a_2|+|a_2-a_3|+\cdots+|a_{n-1}-a_n|$ the <span class="tex-font-style-it">contrast</span> of the array. Note that the contrast of an array of size $1$ is equal to $0$.</p><p>You are given an array of integers $a$. Your task is to build an array of $b$ in such a way that all the following conditions are met:</p><ul> <li> $b$ is not empty, i.e there is at least one element; </li><li> $b$ is a subsequence of $a$, i.e $b$ can be produced by deleting some elements from $a$ (maybe zero); </li><li> the contrast of $b$ is equal to the contrast of $a$. </li></ul><p>What is the minimum possible size of the array $b$?</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 3 \cdot 10^5$)&nbsp;— the size of the array $a$.</p><p>The second line contains $n$ integers $a_1, a_2, \cdot, a_n$ ($0 \le a_i \le 10^9$)&nbsp;— elements of the array itself.</p><p>The sum of $n$ over all test cases doesn't exceed $3 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, print a single integer&nbsp;— the minimum possible size of the array $b$.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 3 \cdot 10^5$)&nbsp;— the size of the array $a$.</p><p>The second line contains $n$ integers $a_1, a_2, \cdot, a_n$ ($0 \le a_i \le 10^9$)&nbsp;— elements of the array itself.</p><p>The sum of $n$ over all test cases doesn't exceed $3 \cdot 10^5$.</p>

## Output

<p>For each test case, print a single integer&nbsp;— the minimum possible size of the array $b$.</p>





```input1|2,3,6,7
4
5
1 3 3 3 7
2
4 2
4
1 1 1 1
7
5 4 2 1 0 0 4
```




```output1
2
2
1
3
```


