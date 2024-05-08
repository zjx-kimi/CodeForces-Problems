## Description

<div><p>The <span class="tex-font-style-it">weight</span> of a sequence is defined as the number of unordered pairs of indexes $(i,j)$ (here $i \lt j$) with same value ($a_{i} = a_{j}$). For example, the weight of sequence $a = [1, 1, 2, 2, 1]$ is $4$. The set of unordered pairs of indexes with same value are $(1, 2)$, $(1, 5)$, $(2, 5)$, and $(3, 4)$.</p><p>You are given a sequence $a$ of $n$ integers. Print the sum of the weight of all subsegments of $a$. </p><p>A sequence $b$ is a subsegment of a sequence $a$ if $b$ can be obtained from $a$ by deletion of several (possibly, zero or all) elements from the beginning and several (possibly, zero or all) elements from the end.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^5$). Description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 10^5$).</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le 10^9$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p></div><div class="output-specification"><p>For each test case, print a single integer&nbsp;— the sum of the weight of all subsegments of $a$.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 10^5$). Description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 10^5$).</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le 10^9$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^5$.</p>

## Output

<p>For each test case, print a single integer&nbsp;— the sum of the weight of all subsegments of $a$.</p>





```input1
2
4
1 2 1 1
4
1 2 3 4
```




```output1
6
0
```



## Note

<ul> <li> In test case $1$, all possible subsegments of sequence $[1, 2, 1, 1]$ having size more than $1$ are: <ol> <li> $[1, 2]$ having $0$ valid unordered pairs; </li><li> $[2, 1]$ having $0$ valid unordered pairs; </li><li> $[1, 1]$ having $1$ valid unordered pair; </li><li> $[1, 2, 1]$ having $1$ valid unordered pairs; </li><li> $[2, 1, 1]$ having $1$ valid unordered pair; </li><li> $[1, 2, 1, 1]$ having $3$ valid unordered pairs. </li></ol> Answer is $6$.</li><li> In test case $2$, all elements of the sequence are distinct. So, there is no valid unordered pair with the same value for any subarray. Answer is $0$. </li></ul>
