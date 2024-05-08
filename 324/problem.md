## Description

<div><p>You are given an array of $n$ nonnegative integers $a_1, a_2, \dots, a_n$. </p><p>Let $m$ be a variable that is initialized to $0$, Jellyfish will perform the following operation $n$ times:</p><ul> <li> select an index $i$ ($1 \leq i \leq |a|$) and delete $a_i$ from $a$. </li><li> add $\operatorname{MEX}(a)^{\dagger}$ to $m$. </li></ul><p>Now Jellyfish wants to know the minimum possible final value of $m$ if he performs all the operations optimally.</p><p>$^{\dagger}$ The MEX (minimum excluded) of an array is the smallest non-negative integer that does not belong to the array. For instance:</p><ul> <li> The MEX of $[2,2,1]$ is $0$, because $0$ does not belong to the array. </li><li> The MEX of $[3,1,0,1]$ is $2$, because $0$ and $1$ belong to the array, but $2$ does not. </li><li> The MEX of $[0,3,1,2]$ is $4$ because $0$, $1$, $2$, and $3$ belong to the array, but $4$ does not. </li></ul></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \leq t \leq 5000$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \leq n \leq 5000$)&nbsp;— the size of the array.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \dots, a_n$ ($0 \leq a_i \leq 10^9$)&nbsp;— the integers in the array.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $5000$.</p></div><div class="output-specification"><p>For each test case, output a single integer&nbsp;— the minimum value of $m$ if the operations are performed optimally.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \leq t \leq 5000$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \leq n \leq 5000$)&nbsp;— the size of the array.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \dots, a_n$ ($0 \leq a_i \leq 10^9$)&nbsp;— the integers in the array.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $5000$.</p>

## Output

<p>For each test case, output a single integer&nbsp;— the minimum value of $m$ if the operations are performed optimally.</p>





```input1|2,3,6,7
4
8
5 2 1 0 3 0 4 0
2
1 2
5
1 0 2 114514 0
8
0 1 2 0 1 2 0 3
```




```output1
3
0
2
7
```



## Note

<p>In the first test case, we delete elements from $a$ in the following order: $[5,2,\color{red}{1},0,3,0,4,0] \to [5,2,0,3,\color{red}{0},4,0] \to [5,2,\color{red}{0},3,4,0] \to [5,2,3,4,\color{red}{0}] \to [5,2,\color{red}{3},4] \to [\color{red}{5},2,4] \to [\color{red}{2},4] \to [\color{red}{4}] \to [~]$. The value of $m$ will be $1+1+1+0+0+0+0+0=3$.</p>
