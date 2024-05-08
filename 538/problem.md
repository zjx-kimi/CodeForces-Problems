## Description

<div><p>You are given two integers $n$ and $k$.</p><p>An array $a_1, a_2, \ldots, a_n$ of length $n$, consisting of zeroes and ones is <span class="tex-font-style-it">good</span> if for <span class="tex-font-style-bf">all</span> integers $i$ from $1$ to $n$ <span class="tex-font-style-bf">both</span> of the following conditions are satisfied:</p><ul> <li> at least $\lceil \frac{i}{k} \rceil$ of the first $i$ elements of $a$ are equal to $1$, </li><li> at least $\lceil \frac{i}{k} \rceil$ of the last $i$ elements of $a$ are equal to $1$. </li></ul><p>Here, $\lceil \frac{i}{k} \rceil$ denotes the result of division of $i$ by $k$, rounded up. For example, $\lceil \frac{6}{3} \rceil = 2$, $\lceil \frac{11}{5} \rceil = \lceil 2.2 \rceil = 3$ and $\lceil \frac{7}{4} \rceil = \lceil 1.75 \rceil = 2$.</p><p>Find the minimum possible number of ones in a good array.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The only line of each test case contains two integers $n$, $k$ ($2 \le n \le 100$, $1 \le k \le n$)&nbsp;— the length of array and parameter $k$ from the statement.</p></div><div class="output-specification"><p>For each test case output one integer&nbsp;— the minimum possible number of ones in a good array.</p><p>It can be shown that under the given constraints at least one good array always exists.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases.</p><p>The only line of each test case contains two integers $n$, $k$ ($2 \le n \le 100$, $1 \le k \le n$)&nbsp;— the length of array and parameter $k$ from the statement.</p>

## Output

<p>For each test case output one integer&nbsp;— the minimum possible number of ones in a good array.</p><p>It can be shown that under the given constraints at least one good array always exists.</p>





```input1|2,4,6,8
7
3 2
5 2
9 3
7 1
10 4
9 5
8 8
```




```output1
2
3
4
7
4
3
2
```



## Note

<p>In the first test case, $n = 3$ and $k = 2$: </p><ul> <li> Array $[ \, 1, 0, 1 \, ]$ is good and the number of ones in it is $2$. </li><li> Arrays $[ \, 0, 0, 0 \, ]$, $[ \, 0, 1, 0 \, ]$ and $[ \, 0, 0, 1 \, ]$ are not good since for $i=1$ the first condition from the statement is not satisfied. </li><li> Array $[ \, 1, 0, 0 \, ]$ is not good since for $i=1$ the second condition from the statement is not satisfied. </li><li> All other arrays of length $3$ contain at least $2$ ones. </li></ul><p>Thus, the answer is $2$.</p><p>In the second test case, $n = 5$ and $k = 2$: </p><ul> <li> Array $[ \, 1, 1, 0, 0, 1 \, ]$ is not good since for $i=3$ the second condition is not satisfied. </li><li> Array $[ \, 1, 0, 1, 0, 1 \, ]$ is good and the number of ones in it is $3$. </li><li> It can be shown that there is no good array with less than $3$ ones, so the answer is $3$. </li></ul><p>In the third test case, $n = 9$ and $k = 3$: </p><ul> <li> Array $[ \, 1, 0, 1, 0, 0, 0, 1, 0, 1 \, ]$ is good and the number of ones in it is $4$. </li><li> It can be shown that there is no good array with less than $4$ ones, so the answer is $4$. </li></ul><p>In the fourth test case, $n = 7$ and $k = 1$. The only good array is $[ \, 1, 1, 1, 1, 1, 1, 1\, ]$, so the answer is $7$.</p>
