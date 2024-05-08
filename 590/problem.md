## Description

<div><p>Victor wants to become "<span class="tex-font-style-it">Mr. Perfectly Fine</span>". For that, he needs to acquire a certain set of skills. More precisely, he has $2$ skills he needs to acquire. </p><p>Victor has $n$ books. Reading book $i$ takes him $m_i$ minutes and will give him some (possibly none) of the required two skills, represented by a binary string of length $2$.</p><p>What is the minimum amount of time required so that Victor acquires all of the two skills? </p></div><div class="input-specification"><p>The input consists of multiple test cases. The first line contains an integer $t$ ($1 \leq t \leq 1000$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains an integer $n$ ($1 \leq n \leq 2 \cdot 10^5$)&nbsp;— the number of books available.</p><p>Then $n$ lines follow. Line $i$ contains a positive integer $m_i$ ($1 \leq m_i \leq 2 \cdot 10^5$) and a binary string of length $2$, where $s_{i1} = 1$ if reading book $i$ acquires Victor skill $1$, and $s_{i1} = 0$ otherwise, and $s_{i2} = 1$ if reading book $i$ acquires Victor skill $2$, and $s_{i2} = 0$ otherwise.</p><p>It is guaranteed that the sum of $n$ over all test cases doesn't exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output a single integer denoting the minimum amount of minutes required for Victor to obtain both needed skills and $-1$ in case it's impossible to obtain the two skills after reading any amount of books. </p></div>

## Input

<p>The input consists of multiple test cases. The first line contains an integer $t$ ($1 \leq t \leq 1000$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains an integer $n$ ($1 \leq n \leq 2 \cdot 10^5$)&nbsp;— the number of books available.</p><p>Then $n$ lines follow. Line $i$ contains a positive integer $m_i$ ($1 \leq m_i \leq 2 \cdot 10^5$) and a binary string of length $2$, where $s_{i1} = 1$ if reading book $i$ acquires Victor skill $1$, and $s_{i1} = 0$ otherwise, and $s_{i2} = 1$ if reading book $i$ acquires Victor skill $2$, and $s_{i2} = 0$ otherwise.</p><p>It is guaranteed that the sum of $n$ over all test cases doesn't exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output a single integer denoting the minimum amount of minutes required for Victor to obtain both needed skills and $-1$ in case it's impossible to obtain the two skills after reading any amount of books. </p>





```input1|2,3,4,5,6,13,14,19,20,21,22,23,24,25
6
4
2 00
3 10
4 01
4 00
5
3 01
3 01
5 01
2 10
9 10
1
5 11
3
9 11
8 01
7 10
6
4 01
6 01
7 01
8 00
9 01
1 00
4
8 00
9 10
9 11
8 11
```




```output1
7
5
5
9
-1
8
```



## Note

<p>In the first test case, we can use books $2$ and $3$, with a total amount of minutes spent equal to $3 + 4 = 7$.</p><p>In the second test case, we can use the books $1$ and $4$, with a total amount of minutes spent equal to $3 + 2 = 5$.</p><p>In the third test case, we have only one option and that is reading book $1$ for a total amount of minutes spent equal to $5$.</p>
