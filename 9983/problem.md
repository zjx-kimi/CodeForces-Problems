## Description

<div><p>Stack has an array $a$ of length $n$ such that $a_i = i$ for all $i$ ($1 \leq i \leq n$). He will select a positive integer $k$ ($1 \leq k \leq \lfloor \frac{n-1}{2} \rfloor$) and do the following operation on $a$ any number (possibly $0$) of times.</p><ul> <li> Select a subsequence$^\dagger$ $s$ of length $2 \cdot k + 1$ from $a$. Now, he will delete the first $k$ elements of $s$ from $a$. To keep things perfectly balanced (as all things should be), he will also delete the last $k$ elements of $s$ from $a$. </li></ul><p>Stack wonders how many arrays $a$ can he end up with for each $k$ ($1 \leq k \leq \lfloor \frac{n-1}{2} \rfloor$). As Stack is weak at counting problems, he needs your help. </p><p>Since the number of arrays might be too large, please print it modulo $998\,244\,353$.</p><p>$^\dagger$ A sequence $x$ is a subsequence of a sequence $y$ if $x$ can be obtained from $y$ by deleting several (possibly, zero or all) elements. For example, $[1, 3]$, $[1, 2, 3]$ and $[2, 3]$ are subsequences of $[1, 2, 3]$. On the other hand, $[3, 1]$ and $[2, 1, 3]$ are not subsequences of $[1, 2, 3]$.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 2 \cdot 10^3$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($3 \leq n \leq 10^6$)&nbsp;— the length of the array $a$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^6$.</p></div><div class="output-specification"><p>For each test, on a new line, print $\lfloor \frac{n-1}{2} \rfloor$ space-separated integers&nbsp;— the $i$-th integer representing the number of arrays modulo $998\,244\,353$ that Stack can get if he selects $k=i$.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 2 \cdot 10^3$)&nbsp;— the number of test cases. The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($3 \leq n \leq 10^6$)&nbsp;— the length of the array $a$.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^6$.</p>

## Output

<p>For each test, on a new line, print $\lfloor \frac{n-1}{2} \rfloor$ space-separated integers&nbsp;— the $i$-th integer representing the number of arrays modulo $998\,244\,353$ that Stack can get if he selects $k=i$.</p>





```input1|2,4
4
3
4
5
10
```




```output1
2 
4 
10 2 
487 162 85 10
```



## Note

<p>In the first test case, two $a$ are possible for $k=1$: </p><ul> <li> $[1,2,3]$; </li><li> $[2]$. </li></ul><p>In the second test case, four $a$ are possible for $k=1$: </p><ul> <li> $[1,2,3,4]$; </li><li> $[1,3]$; </li><li> $[2,3]$; </li><li> $[2,4]$. </li></ul><p>In the third test case, two $a$ are possible for $k=2$: </p><ul> <li> $[1,2,3,4,5]$; </li><li> $[3]$. </li></ul>
