## Description

<div><p>You are given a permutation$^\dagger$ $a$ of length $n$.</p><p>Find any permutation $b$ of length $n$ such that $a_1+b_1 \le a_2+b_2 \le a_3+b_3 \le \ldots \le a_n+b_n$.</p><p>It can be proven that a permutation $b$ that satisfies the condition above always exists.</p><p>$^\dagger$ A permutation of length $n$ is an array consisting of $n$ distinct integers from $1$ to $n$ in arbitrary order. For example, $[2,3,1,5,4]$ is a permutation, but $[1,2,2]$ is not a permutation ($2$ appears twice in the array), and $[1,3,4]$ is also not a permutation ($n=3$ but there is $4$ in the array).</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line of input contains a single integer $t$ ($1 \le t \le 2000$)&nbsp;— the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 100$)&nbsp;— the length of permutations $a$ and $b$.</p><p>The second line of each test case contains $n$ distinct integers $a_1,a_2,\ldots,a_n$ ($1 \le a_i \le n$)&nbsp;— the elements of permutation $a$. All elements of $a$ are distinct.</p><p>Note that there is no bound on the sum of $n$ over all test cases.</p></div><div class="output-specification"><p>For each test case, output <span class="tex-font-style-bf">any</span> permutation $b$ which satisfies the constraints mentioned in the statement. It can be proven that a permutation $b$ that satisfies the condition above always exists.</p></div>

## Input

<p>Each test contains multiple test cases. The first line of input contains a single integer $t$ ($1 \le t \le 2000$)&nbsp;— the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 100$)&nbsp;— the length of permutations $a$ and $b$.</p><p>The second line of each test case contains $n$ distinct integers $a_1,a_2,\ldots,a_n$ ($1 \le a_i \le n$)&nbsp;— the elements of permutation $a$. All elements of $a$ are distinct.</p><p>Note that there is no bound on the sum of $n$ over all test cases.</p>

## Output

<p>For each test case, output <span class="tex-font-style-bf">any</span> permutation $b$ which satisfies the constraints mentioned in the statement. It can be proven that a permutation $b$ that satisfies the condition above always exists.</p>





```input1|2,3,6,7,10,11
5
5
1 2 4 5 3
2
1 2
1
1
3
3 2 1
4
1 4 3 2
```




```output1
1 2 4 3 5
2 1
1
1 2 3
1 2 3 4
```



## Note

<p>In the first test case $a=[1, 2, 4, 5, 3]$. Then the permutation $b=[1, 2, 4, 3, 5]$ satisfies the condition because $1 + 1 \le 2 + 2 \le 4 + 4 \le 5 + 3 \le 3 + 5$.</p>
