## Description

<div><p>You are given a binary string $s$ of length $2n$ where each element is $\mathtt{0}$ or $\mathtt{1}$. You can do the following operation:</p><ol><li> Choose a balanced bracket sequence$^\dagger$ $b$ of length $2n$. </li><li> For every index $i$ from $1$ to $2n$ in order, where $b_i$ is an open bracket, let $p_i$ denote the minimum index such that $b[i,p_i]$ is a balanced bracket sequence. Then, we perform a range toggle operation$^\ddagger$ from $i$ to $p_i$ on $s$. Note that since a balanced bracket sequence of length $2n$ will have $n$ open brackets, we will do $n$ range toggle operations on $s$. </li></ol><p>Your task is to find a sequence of no more than $10$ operations that changes all elements of $s$ to $\mathtt{0}$, or determine that it is impossible to do so. Note that you do <span class="tex-font-style-bf">not</span> have to minimize the number of operations.</p><p>Under the given constraints, it can be proven that if it is possible to change all elements of $s$ to $\mathtt{0}$, there exists a way that requires no more than $10$ operations.</p><p>$^\dagger$ A sequence of brackets is called balanced if one can turn it into a valid math expression by adding characters $+$ and $1$. For example, sequences "<span class="tex-font-style-tt">(())()</span>", "<span class="tex-font-style-tt">()</span>", and "<span class="tex-font-style-tt">(()(()))</span>" are balanced, while "<span class="tex-font-style-tt">)(</span>", "<span class="tex-font-style-tt">(()</span>", and "<span class="tex-font-style-tt">(()))(</span>" are not.</p><p>$^\ddagger$ If we perform a range toggle operation from $l$ to $r$ on a binary string $s$, then we toggle all values of $s_i$ such that $l \leq i \leq r$. If $s_i$ is toggled, we will set $s_i := \mathtt{0}$ if $s_i = \mathtt{1}$ or vice versa. For example, if $s=\mathtt{1000101}$ and we perform a range toggle operation from $3$ to $5$, $s$ will be changed to $s=\mathtt{1011001}$.</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 1000$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 2\cdot 10^5$)&nbsp;— where $2n$ is the length of string $s$.</p><p>The second line of each test case contains a binary string $s$ of length $2n$ ($s_i = \mathtt{0}$ or $s_i = \mathtt{1}$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2\cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output $-1$ in a single line if it is impossible to change all elements of $s$ to $\mathtt{0}$.</p><p>Otherwise, output a single integer $k$ ($0 \le k \le 10$) representing the number of operations needed to change all elements of $s$ to $\mathtt{0}$. Then, on each of the next $k$ lines, output a balanced bracket sequence of length $2n$ representing the operations needed to change all elements of $s$ to $0$s.</p><p>If there are multiple ways to change all elements of $s$ to $\mathtt{0}$ that require not more than $10$ operations, you can output any of them.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 1000$). The description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 2\cdot 10^5$)&nbsp;— where $2n$ is the length of string $s$.</p><p>The second line of each test case contains a binary string $s$ of length $2n$ ($s_i = \mathtt{0}$ or $s_i = \mathtt{1}$).</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2\cdot 10^5$.</p>

## Output

<p>For each test case, output $-1$ in a single line if it is impossible to change all elements of $s$ to $\mathtt{0}$.</p><p>Otherwise, output a single integer $k$ ($0 \le k \le 10$) representing the number of operations needed to change all elements of $s$ to $\mathtt{0}$. Then, on each of the next $k$ lines, output a balanced bracket sequence of length $2n$ representing the operations needed to change all elements of $s$ to $0$s.</p><p>If there are multiple ways to change all elements of $s$ to $\mathtt{0}$ that require not more than $10$ operations, you can output any of them.</p>





```input1|2,3,6,7
4
1
01
2
0000
3
100111
4
01011100
```




```output1
-1
2
()()
()()
1
(())()
2
(((())))
()()(())
```



## Note

<p>In the first test case, it can be proven that it is impossible to change all elements of $s$ to $\mathtt{0}$.</p><p>In the second test case, the first operation using the bracket sequence $b = \mathtt{()()}$ will convert the binary string $s=\mathtt{0000}$ to $s=\mathtt{1111}$. Then, the second operation using the same bracket sequence $b = \mathtt{()()}$ will convert the binary string $s=\mathtt{1111}$ back to $s=\mathtt{0000}$. Note that since all elements of $s$ is already $\mathtt{0}$ initially, using $0$ operations is also a valid answer.</p><p>In the third test case, a single operation using the bracket sequence $b = \mathtt{(())()}$ will change all elements of $s$ to $\mathtt{0}$. The operation will happen as follows.</p><ol> <li> $b_1$ is an open bracket and $p_1 = 4$ since $b[1,4]=\mathtt{(())}$ is a balanced bracket sequence. Hence, we do a range toggle operation from $1$ to $4$ on the binary string $s = \mathtt{100111}$ to obtain $s = \mathtt{011011}$. </li><li> $b_2$ is an open bracket and $p_2 = 3$ since $b[2,3]=\mathtt{()}$ is a balanced bracket sequence. Hence, we do a range toggle operation from $2$ to $3$ on the binary string $s = \mathtt{011011}$ to obtain $s = \mathtt{000011}$. </li><li> $b_3$ is not an open bracket, so no range toggle operation is done at this step. </li><li> $b_4$ is not an open bracket, so no range toggle operation is done at this step. </li><li> $b_5$ is an open bracket and $p_5 = 6$ since $b[5,6]=\mathtt{()}$ is a balanced bracket sequence. Hence, we do a range toggle operation from $5$ to $6$ on the binary string $s = \mathtt{000011}$ to obtain $s = \mathtt{000000}$. </li><li> $b_6$ is not an open bracket, so no range toggle operation is done at this step. </li></ol><p>In the fourth test case, the first operation using the bracket sequence $b = \mathtt{(((())))}$ will convert the binary string $s = \mathtt{01011100}$ to $s = \mathtt{11111001}$. Then, the second operation using the bracket sequence $b = \mathtt{()()(())}$ will convert the binary string $s = \mathtt{11111001}$ to $s=\mathtt{00000000}$.</p>
