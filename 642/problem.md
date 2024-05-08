## Description

<div><p>You're given a positive integer $n$.</p><p>Find a permutation $a_1, a_2, \dots, a_n$ such that for any $1 \leq l &lt; r \leq n$, the sum $a_l + a_{l+1} + \dots + a_r$ is not divisible by $r-l+1$.</p><p>A permutation of length $n$ is an array consisting of $n$ distinct integers from $1$ to $n$ in arbitrary order. For example, $[2,3,1,5,4]$ is a permutation, but $[1,2,2]$ is not a permutation ($2$ appears twice in the array), and $[1,3,4]$ is also not a permutation ($n=3$ but there is $4$ in the array).</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 100$). Description of the test cases follows.</p><p>The first line of each test case contain a single integer $n$ ($1 \leq n \leq 100$) — the size of the desired permutation.</p></div><div class="output-specification"><p>For each test case, if there is no such permutation print $-1$.</p><p>Otherwise, print $n$ distinct integers $p_1, p_{2}, \dots, p_n$ ($1 \leq p_i \leq n$) — a permutation satisfying the condition described in the statement.</p><p>If there are multiple solutions, print any.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 100$). Description of the test cases follows.</p><p>The first line of each test case contain a single integer $n$ ($1 \leq n \leq 100$) — the size of the desired permutation.</p>

## Output

<p>For each test case, if there is no such permutation print $-1$.</p><p>Otherwise, print $n$ distinct integers $p_1, p_{2}, \dots, p_n$ ($1 \leq p_i \leq n$) — a permutation satisfying the condition described in the statement.</p><p>If there are multiple solutions, print any.</p>





```input1
3
1
2
3
```




```output1
1
1 2
-1
```



## Note

<p>In the first example, there are no valid pairs of $l &lt; r$, meaning that the condition is true for all such pairs.</p><p>In the second example, the only valid pair is $l=1$ and $r=2$, for which $a_1 + a_2 = 1+2=3$ is not divisible by $r-l+1=2$.</p><p>in the third example, for $l=1$ and $r=3$ the sum $a_1+a_2+a_3$ is always $6$, which is divisible by $3$.</p>
