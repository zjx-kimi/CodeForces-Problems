## Description

<div><p>You are given two integers $n$ and $k$ ($k \le n$), where $k$ is even.</p><p>A permutation of length $n$ is an array consisting of $n$ distinct integers from $1$ to $n$ in any order. For example, $[2,3,1,5,4]$ is a permutation, but $[1,2,2]$ is not a permutation (as $2$ appears twice in the array) and $[0,1,2]$ is also not a permutation (as $n=3$, but $3$ is not present in the array).</p><p>Your task is to construct a <span class="tex-font-style-it">$k$-level</span> permutation of length $n$.</p><p>A permutation is called <span class="tex-font-style-it">$k$-level</span> if, among all the sums of continuous segments of length $k$ (of which there are exactly $n - k + 1$), any two sums differ by no more than $1$.</p><p>More formally, to determine if the permutation $p$ is <span class="tex-font-style-it">$k$-level</span>, first construct an array $s$ of length $n - k + 1$, where $s_i=\sum_{j=i}^{i+k-1} p_j$, i.e., the $i$-th element is equal to the sum of $p_i, p_{i+1}, \dots, p_{i+k-1}$.</p><p>A permutation is called <span class="tex-font-style-it">$k$-level</span> if $\max(s) - \min(s) \le 1$.</p><p>Find <span class="tex-font-style-bf">any</span> <span class="tex-font-style-it">$k$-level</span> permutation of length $n$.</p></div><div class="input-specification"><p>The first line of the input contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. This is followed by the description of the test cases.</p><p>The first and only line of each test case contains two integers $n$ and $k$ ($2 \le k \le n \le 2 \cdot 10^5$, $k$ is even), where $n$ is the length of the desired permutation.</p><p>It is guaranteed that the sum of $n$ for all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output <span class="tex-font-style-bf">any</span> <span class="tex-font-style-it">$k$-level</span> permutation of length $n$.</p><p>It is guaranteed that such a permutation always exists given the constraints.</p></div>

## Input

<p>The first line of the input contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. This is followed by the description of the test cases.</p><p>The first and only line of each test case contains two integers $n$ and $k$ ($2 \le k \le n \le 2 \cdot 10^5$, $k$ is even), where $n$ is the length of the desired permutation.</p><p>It is guaranteed that the sum of $n$ for all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output <span class="tex-font-style-bf">any</span> <span class="tex-font-style-it">$k$-level</span> permutation of length $n$.</p><p>It is guaranteed that such a permutation always exists given the constraints.</p>





```input1|2,4,6
5
2 2
3 2
10 4
13 4
7 4
```




```output1
1 2
3 1 2
8 3 10 1 7 4 9 2 6 5
13 4 9 1 12 5 8 2 11 6 7 3 10
1 7 3 5 2 6 4
```



## Note

<p>In the second test case of the example: </p><ul> <li> $p_1 + p_2 = 3 + 1 = 4$; </li><li> $p_2 + p_3 = 1 + 2 = 3$. </li></ul> The maximum among the sums is $4$, and the minimum is $3$.
