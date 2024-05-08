## Description

<div><p>Jayden has an array $a$ which is initially empty. There are $n$ operations of two types he must perform in the given order.</p><ol> <li> Jayden appends an integer $x$ ($1 \leq x \leq n$) to the end of array $a$. </li><li> Jayden appends $x$ copies of array $a$ to the end of array $a$. In other words, array $a$ becomes $[a,\underbrace{a,\ldots,a}_{x}]$. It is guaranteed that he has done at least one operation of the first type before this. </li></ol><p>Jayden has $q$ queries. For each query, you must tell him the $k$-th element of array $a$. The elements of the array are numbered from $1$.</p></div><div class="input-specification"><p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 5000$) — the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $q$ ($1 \leq n, q \leq 10^5$) — the number of operations and the number of queries.</p><p>The following $n$ lines describe the operations. Each line contains two integers $b$ and $x$ ($b \in \{1, 2\}$), where $b$ denotes the type of operation. If $b=1$, then $x$ ($1 \leq x \leq n$) is the integer Jayden appends to the end of the array. If $b=2$, then $x$ ($1 \leq x \leq 10^9$) is the number of copies Jayden appends to the end of the array. </p><p>The next line of each test case contains $q$ integers $k_1, k_2, \ldots, k_q$ ($1 \leq k_i \leq \min(10^{18}, c)$), which denote the queries, where $c$ is the size of the array after finishing all $n$ operations.</p><p>It is guaranteed that the sum of $n$ and the sum of $q$ over all test cases does not exceed $10^5$. </p></div><div class="output-specification"><p>For each test case, output $q$ integers — answers to Jayden's queries.</p></div>

## Input

<p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 5000$) — the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains two integers $n$ and $q$ ($1 \leq n, q \leq 10^5$) — the number of operations and the number of queries.</p><p>The following $n$ lines describe the operations. Each line contains two integers $b$ and $x$ ($b \in \{1, 2\}$), where $b$ denotes the type of operation. If $b=1$, then $x$ ($1 \leq x \leq n$) is the integer Jayden appends to the end of the array. If $b=2$, then $x$ ($1 \leq x \leq 10^9$) is the number of copies Jayden appends to the end of the array. </p><p>The next line of each test case contains $q$ integers $k_1, k_2, \ldots, k_q$ ($1 \leq k_i \leq \min(10^{18}, c)$), which denote the queries, where $c$ is the size of the array after finishing all $n$ operations.</p><p>It is guaranteed that the sum of $n$ and the sum of $q$ over all test cases does not exceed $10^5$. </p>

## Output

<p>For each test case, output $q$ integers — answers to Jayden's queries.</p>





```input1|2,3,4,5,6,7,8,21,22,23,24,25,26,27,28,29,30,31,32,33,34
4
5 10
1 1
1 2
2 1
1 3
2 3
1 2 3 4 5 6 14 15 16 20
10 10
1 3
1 8
2 15
1 6
1 9
1 1
2 6
1 1
2 12
2 10
32752 25178 3198 3199 2460 2461 31450 33260 9016 4996
12 5
1 6
1 11
2 392130334
1 4
2 744811750
1 10
1 5
2 209373780
2 178928984
1 3
2 658326464
2 1000000000
914576963034536490 640707385283752918 636773368365261971 584126563607944922 1000000000000000000
2 2
1 1
1 2
1 2
```




```output1
1 2 1 2 3 1 2 3 1 3
9 8 1 3 1 3 6 3 8 8
11 11 11 10 11
1 2
```



## Note

<p>In the first test case:</p><ul><li> After the first operation $a = [1]$;</li><li> After the second operation $a = [1, 2]$;</li><li> After the third operation $a = [1, 2, 1, 2]$;</li><li> After the fourth operation $a = [1, 2, 1, 2, 3]$;</li><li> After the fifth operation $a = [1, 2, 1, 2, 3, 1, 2, 1, 2, 3, 1, 2, 1, 2, 3, 1, 2, 1, 2, 3]$.</li></ul><p>In the fourth test case, after all operations $a = [1, 2]$.</p>
