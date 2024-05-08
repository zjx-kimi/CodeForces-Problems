## Description

<div><p>You are given a permutation $p_1, p_2, \ldots, p_n$ of length $n$. You have to choose two integers $l,r$ ($1 \le l \le r \le n$) and reverse the subsegment $[l,r]$ of the permutation. The permutation will become $p_1,p_2, \dots, p_{l-1},p_r,p_{r-1}, \dots, p_l,p_{r+1},p_{r+2}, \dots ,p_n$.</p><p>Find the lexicographically smallest permutation that can be obtained by performing <span class="tex-font-style-bf">exactly</span> one reverse operation on the initial permutation.</p><p>Note that for two distinct permutations of equal length $a$ and $b$, $a$ is lexicographically smaller than $b$ if at the first position they differ, $a$ has the smaller element.</p><p>A permutation is an array consisting of $n$ distinct integers from $1$ to $n$ in arbitrary order. For example, $[2,3,1,5,4]$ is a permutation, but $[1,2,2]$ is not a permutation ($2$ appears twice in the array) and $[1,3,4]$ is also not a permutation ($n=3$ but there is $4$ in the array).</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 500$)&nbsp;— the number of test cases. Description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 500$)&nbsp;— the length of the permutation.</p><p>The second line of each test case contains $n$ integers $p_1, p_2, \dots, p_n$ ($1 \le p_i \le n$)&nbsp;— the elements of the permutation.</p></div><div class="output-specification"><p>For each test case print the lexicographically smallest permutation you can obtain.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 500$)&nbsp;— the number of test cases. Description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 500$)&nbsp;— the length of the permutation.</p><p>The second line of each test case contains $n$ integers $p_1, p_2, \dots, p_n$ ($1 \le p_i \le n$)&nbsp;— the elements of the permutation.</p>

## Output

<p>For each test case print the lexicographically smallest permutation you can obtain.</p>





```input1|2,3,6,7
4
1
1
3
2 1 3
4
1 4 2 3
5
1 2 3 4 5
```




```output1
1 
1 2 3 
1 2 4 3 
1 2 3 4 5
```



## Note

<p>In the first test case, the permutation has length $1$, so the only possible segment is $[1,1]$. The resulting permutation is $[1]$.</p><p>In the second test case, we can obtain the identity permutation by reversing the segment $[1,2]$. The resulting permutation is $[1,2,3]$.</p><p>In the third test case, the best possible segment is $[2,3]$. The resulting permutation is $[1,2,4,3]$.</p><p>In the fourth test case, there is no lexicographically smaller permutation, so we can leave it unchanged by choosing the segment $[1,1]$. The resulting permutation is $[1,2,3,4,5]$.</p>
