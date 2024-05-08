## Description

<div><p>Olya has an array of integers $a_1, a_2, \ldots, a_n$. She wants to split it into tandem repeats. Since it's rarely possible, before that she wants to perform the following operation several (possibly, zero) number of times: insert a pair of equal numbers into an arbitrary position. Help her!</p><p>More formally:</p><ul> <li> A tandem repeat is a sequence $x$ of even length $2k$ such that for each $1 \le i \le k$ the condition $x_i = x_{i + k}$ is satisfied. </li><li> An array $a$ could be split into tandem repeats if you can split it into several parts, each being a subsegment of the array, such that each part is a tandem repeat. </li><li> In one operation you can choose an arbitrary letter $c$ and insert $[c, c]$ to any position in the array (at the beginning, between any two integers, or at the end). </li><li> You are to perform several operations and split the array into tandem repeats or determine that it is impossible. Please note that you do <span class="tex-font-style-bf">not</span> have to minimize the number of operations. </li></ul></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 30\,000$) — the number of test cases. Description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 500$). </p><p>The second line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le 10^9$) &nbsp;— the initial array. </p><p>It is guaranteed that the sum of $n^2$ over all test cases does not exceed $250\,000$.</p></div><div class="output-specification"><p>For each test case print answer in the following format.</p><p>If you cannot turn the array into a concatenation of tandem repeats, print a single integer $-1$.</p><p>Otherwise print the number of operations $q$ ($0 \le q \le 2 \cdot n^2$) that you want to do. Then print the descriptions of operations.</p><p>In each of the following $q$ lines print two integers $p$ and $c$ ($1 \le c \le 10^9$), which mean that you insert the integer $c$ twice after $p$ elements of the array. If the length of the array is $m$ before the operation, then the condition $0 \le p \le m$ should be satisfied.</p><p>Then you should print any way to split the resulting array into tandem repeats. First, print a single integer $d$, and then print a sequence $t_1, t_2, \ldots, t_d$ of even integers of size $d$ ($d, t_i \ge 1$). These numbers are the lengths of the subsegments from left to right.</p><p>Note that the size of the resulting array $a$ is $m = n + 2 \cdot q$. The following statements must hold: </p><ul> <li> $m = \sum\limits_{i = 1}^{d}{t_i}$.   </li><li> For all integer $i$ such that $1 \le i \le d$, the sequence $a_l, a_{l+1}, \ldots, a_r$ is a tandem repeat, where $l = \sum\limits_{j = 1}^{i - 1}{t_j} + 1$, $r = l + t_i - 1$. </li></ul><p>It can be shown that if the array can be turned into a concatenation of tandem repeats, then there exists a solution satisfying all constraints. If there are multiple answers, you can print any.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains a single integer $t$ ($1 \le t \le 30\,000$) — the number of test cases. Description of the test cases follows.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 500$). </p><p>The second line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le 10^9$) &nbsp;— the initial array. </p><p>It is guaranteed that the sum of $n^2$ over all test cases does not exceed $250\,000$.</p>

## Output

<p>For each test case print answer in the following format.</p><p>If you cannot turn the array into a concatenation of tandem repeats, print a single integer $-1$.</p><p>Otherwise print the number of operations $q$ ($0 \le q \le 2 \cdot n^2$) that you want to do. Then print the descriptions of operations.</p><p>In each of the following $q$ lines print two integers $p$ and $c$ ($1 \le c \le 10^9$), which mean that you insert the integer $c$ twice after $p$ elements of the array. If the length of the array is $m$ before the operation, then the condition $0 \le p \le m$ should be satisfied.</p><p>Then you should print any way to split the resulting array into tandem repeats. First, print a single integer $d$, and then print a sequence $t_1, t_2, \ldots, t_d$ of even integers of size $d$ ($d, t_i \ge 1$). These numbers are the lengths of the subsegments from left to right.</p><p>Note that the size of the resulting array $a$ is $m = n + 2 \cdot q$. The following statements must hold: </p><ul> <li> $m = \sum\limits_{i = 1}^{d}{t_i}$.   </li><li> For all integer $i$ such that $1 \le i \le d$, the sequence $a_l, a_{l+1}, \ldots, a_r$ is a tandem repeat, where $l = \sum\limits_{j = 1}^{i - 1}{t_j} + 1$, $r = l + t_i - 1$. </li></ul><p>It can be shown that if the array can be turned into a concatenation of tandem repeats, then there exists a solution satisfying all constraints. If there are multiple answers, you can print any.</p>





```input1
4
2
5 7
2
5 5
6
1 3 1 2 2 3
6
3 2 1 1 2 3
```




```output1
-1
0
1
2
4
1 3
5 3
5 3
10 3
2
8 6 
5
0 3
8 3
5 3 
6 2 
7 1
4
2 6 6 2
```



## Note

<p>In the first test case, you cannot apply operations to the array to make it possible to split it into tandem repeats.</p><p>In the second test case the array is already a tandem repeat $[5, 5] = \underbrace{([5] + [5])}_{t_1 = 2}$, thus we can do no operations at all.</p><p>In the third test case, initially, we have the following array: $$[1, 3, 1, 2, 2, 3].$$ After the first insertion with $p = 1, c = 3$: $$[1, \textbf{3, 3}, 3, 1, 2, 2, 3].$$ After the second insertion with $p = 5, c = 3$: $$[1, 3, 3, 3, 1, \textbf{3, 3}, 2, 2, 3].$$ After the third insertion with $p = 5, c = 3$: $$[1, 3, 3, 3, 1, \textbf{3, 3}, 3, 3, 2, 2, 3].$$ After the fourth insertion with $p = 10, c = 3$: $$[1, 3, 3, 3, 1, 3, 3, 3, 3, 2, \textbf{3, 3}, 2, 3].$$ The resulting array can be represented as a concatenation of tandem repeats: $$\underbrace{([1, 3, 3, 3] + [1, 3, 3, 3])}_{t_1 = 8} + \underbrace{([3, 2, 3] + [3, 2, 3])}_{t_2 = 6}.$$</p><p>In the fourth test case, initially, we have the following array: $$[3, 2, 1, 1, 2, 3].$$ After the first insertion with $p = 0, c = 3$: $$[\textbf{3, 3}, 3, 2, 1, 1, 2, 3].$$ After the second insertion with $p = 8, c = 3$: $$[3, 3, 3, 2, 1, 1, 2, 3, \textbf{3, 3}].$$ After the third insertion with $p = 5, c = 3$ $$[3, 3, 3, 2, 1, \textbf{3, 3}, 1, 2, 3, 3, 3].$$ After the fourth insertion with $p = 6, c = 2$: $$[3, 3, 3, 2, 1, 3, \textbf{2, 2}, 3, 1, 2, 3, 3, 3].$$ After the fifth insertion with $p = 7, c = 1$: $$[3, 3, 3, 2, 1, 3, 2, \textbf{1, 1}, 2, 3, 1, 2, 3, 3, 3].$$ The resulting array can be represented as a concatenation of tandem repeats: $$\underbrace{([3] + [3])}_{t_1 = 2} + \underbrace{([3, 2, 1] + [3, 2, 1])}_{t_2 = 6} + \underbrace{([1, 2, 3] + [1, 2, 3])}_{t_3 = 6} + \underbrace{([3] + [3])}_{t_4 = 2}.$$</p>
