## Description

<div><p>Koxia and Mahiru are playing a game with three arrays $a$, $b$, and $c$ of length $n$. Each element of $a$, $b$ and $c$ is an integer between $1$ and $n$ inclusive.</p><p>The game consists of $n$ rounds. In the $i$-th round, they perform the following moves:</p><ul> <li> Let $S$ be the multiset $\{a_i, b_i, c_i\}$. </li><li> Koxia removes one element from the multiset $S$ by her choice. </li><li> Mahiru chooses one integer from the two remaining in the multiset $S$. </li></ul><p>Let $d_i$ be the integer Mahiru chose in the $i$-th round. If $d$ is a permutation$^\dagger$, Koxia wins. Otherwise, Mahiru wins.</p><p>Currently, only the arrays $a$ and $b$ have been chosen. As an avid supporter of Koxia, you want to choose an array $c$ such that Koxia will win. Count the number of such $c$, modulo $998\,244\,353$.</p><p>Note that Koxia and Mahiru both play optimally.</p><p>$^\dagger$ A permutation of length $n$ is an array consisting of $n$ distinct integers from $1$ to $n$ in arbitrary order. For example, $[2,3,1,5,4]$ is a permutation, but $[1,2,2]$ is not a permutation ($2$ appears twice in the array), and $[1,3,4]$ is also not a permutation ($n=3$ but there is $4$ in the array).</p></div><div class="input-specification"><p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 2 \cdot 10^4$) — the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \leq n \leq {10}^5$) — the size of the arrays.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \leq a_i \leq n$).</p><p>The third line of each test case contains $n$ integers $b_1, b_2, \dots, b_n$ ($1 \leq b_i \leq n$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed ${10}^5$.</p></div><div class="output-specification"><p>Output a single integer — the number of $c$ makes Koxia win, modulo $998\,244\,353$.</p></div>

## Input

<p>Each test consists of multiple test cases. The first line contains a single integer $t$ ($1 \leq t \leq 2 \cdot 10^4$) — the number of test cases. The description of test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \leq n \leq {10}^5$) — the size of the arrays.</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \leq a_i \leq n$).</p><p>The third line of each test case contains $n$ integers $b_1, b_2, \dots, b_n$ ($1 \leq b_i \leq n$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed ${10}^5$.</p>

## Output

<p>Output a single integer — the number of $c$ makes Koxia win, modulo $998\,244\,353$.</p>





```input1|2,3,4
2
3
1 2 2
1 3 3
5
3 3 1 3 4
4 5 2 5 5
```




```output1
6
0
```



## Note

<p>In the first test case, there are $6$ possible arrays $c$ that make Koxia win — $[1, 2, 3]$, $[1, 3, 2]$, $[2, 2, 3]$, $[2, 3, 2]$, $[3, 2, 3]$, $[3, 3, 2]$.</p><p>In the second test case, it can be proved that no array $c$ makes Koxia win.</p>
