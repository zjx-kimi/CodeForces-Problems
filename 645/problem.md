## Description

<div><p>You're given a multiset of non-negative integers $\{a_1, a_2, \dots, a_n\}$.</p><p>In one step you take two elements $x$ and $y$ of the multiset, remove them and insert their mean value $\frac{x + y}{2}$ back into the multiset.</p><p>You repeat the step described above until you are left with only two numbers $A$ and $B$. What is the maximum possible value of their absolute difference $|A-B|$?</p><p>Since the answer is not an integer number, output it modulo $10^9+7$.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 100$). Description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2 \le n \le 10^6$) — the size of the multiset.</p><p>The second line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($0 \le a_i \le 10^9$) — the elements of the multiset.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^6$.</p></div><div class="output-specification"><p>For each test case, output a single integer, the answer to the problem modulo $10^9+7$.</p><p>Formally, let $M = 10^9+7$. It can be shown that the answer can be expressed as an irreducible fraction $\frac{p}{q}$, where $p$ and $q$ are integers and $q \not \equiv 0 \pmod{M}$. Output the integer equal to $p \cdot q^{-1} \bmod M$. In other words, output an integer $x$ such that $0 \le x &lt; M$ and $x \cdot q \equiv p \pmod{M}$.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 100$). Description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($2 \le n \le 10^6$) — the size of the multiset.</p><p>The second line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($0 \le a_i \le 10^9$) — the elements of the multiset.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $10^6$.</p>

## Output

<p>For each test case, output a single integer, the answer to the problem modulo $10^9+7$.</p><p>Formally, let $M = 10^9+7$. It can be shown that the answer can be expressed as an irreducible fraction $\frac{p}{q}$, where $p$ and $q$ are integers and $q \not \equiv 0 \pmod{M}$. Output the integer equal to $p \cdot q^{-1} \bmod M$. In other words, output an integer $x$ such that $0 \le x &lt; M$ and $x \cdot q \equiv p \pmod{M}$.</p>





```input1|2,3,6,7,10,11
5
2
7 3
4
1 2 10 11
3
1 2 3
6
64 32 64 16 64 0
4
1 1 1 1
```




```output1
4
9
500000005
59
0
```



## Note

<p>In the first case, you can't do any operations, so the answer is $|7-3|=4$.</p><p>In the second case, one of the optimal sequence of operations: </p><ol> <li> Substitute $1$ and $2$ with $1.5$; </li><li> Substitute $10$ and $11$ with $10.5$; </li><li> The difference between $1.5$ and $10.5$ is $9$. </li></ol><p>In the third case, the exact answer is $\frac{3}{2}$, and $500\,000\,005 \cdot 2 \equiv 3 \pmod{10^9+7}$.</p>
