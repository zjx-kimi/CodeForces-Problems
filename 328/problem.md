## Description

<div><p>Jellyfish always uses OEIS to solve math problems, but now she finds a problem that cannot be solved by OEIS:</p><p>Count the number of permutations $p$ of $[1, 2, \dots, n]$ such that for all $(l, r)$ such that $l \leq r \leq m_l$, the subarray $[p_l, p_{l+1}, \dots, p_r]$ is not a permutation of $[l, l+1, \dots, r]$.</p><p>Since the answer may be large, you only need to find the answer modulo $10^9+7$.</p></div><div class="input-specification"><p>The first line of the input contains a single integer $n$ ($1 \leq n \leq 200$)&nbsp;— the length of the permutation.</p><p>The second line of the input contains $n$ integers $m_1, m_2, \dots, m_n$ ($0 \leq m_i \leq n$).</p></div><div class="output-specification"><p>Output the number of different permutations that satisfy the conditions, modulo $10^9+7$.</p></div>

## Input

<p>The first line of the input contains a single integer $n$ ($1 \leq n \leq 200$)&nbsp;— the length of the permutation.</p><p>The second line of the input contains $n$ integers $m_1, m_2, \dots, m_n$ ($0 \leq m_i \leq n$).</p>

## Output

<p>Output the number of different permutations that satisfy the conditions, modulo $10^9+7$.</p>





```input1
3
1 2 3
```




```input2
5
2 4 3 4 5
```




```input3
5
5 1 1 1 1
```




```output1
2
```




```output2
38
```




```output3
0
```



## Note

<p>In the first example, $[2, 3, 1]$ and $[3, 1, 2]$ satisfies the condition.</p>
