## Description

<div><p>You are given two permutations $a$ and $b$ of length $n$. A permutation is an array of $n$ elements from $1$ to $n$ where all elements are distinct. For example, an array [$2,1,3$] is a permutation, but [$0,1$] and [$1,3,1$] aren't.</p><p>You can (as many times as you want) choose two indices $i$ and $j$, then swap $a_i$ with $a_j$ and $b_i$ with $b_j$ simultaneously. </p><p>You hate inversions, so you want to minimize the total number of inversions in both permutations.</p><p>An inversion in a permutation $p$ is a pair of indices $(i, j)$ such that $i &lt; j$ and $p_i &gt; p_j$. For example, if $p=[3,1,4,2,5]$ then there are $3$ inversions in it (the pairs of indices are $(1,2)$, $(1,4)$ and $(3,4)$).</p></div><div class="input-specification"><p>The first line contains an integer $t$ ($1 \leq t \leq 20\,000$)&nbsp;— the number of test cases.</p><p>Each test case consists of three lines. The first line contains an integer $n$ ($1 \leq n \leq 2\cdot10^5$)&nbsp;— the length of the permutations $a$ and $b$. The second line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \leq a_i \leq n$)&nbsp;— permutation $a$. The third line contains $b$ in a similar format. </p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2\cdot10^5$.</p></div><div class="output-specification"><p>For each test case, output two permutations $a'$ and $b'$ (in the same format as in the input)&nbsp;— the permutations after all operations. The total number of inversions in $a'$ and $b'$ should be the minimum possible among all pairs of permutations that can be obtained using operations from the statement.</p><p>If there are multiple solutions, print any of them.</p></div>

## Input

<p>The first line contains an integer $t$ ($1 \leq t \leq 20\,000$)&nbsp;— the number of test cases.</p><p>Each test case consists of three lines. The first line contains an integer $n$ ($1 \leq n \leq 2\cdot10^5$)&nbsp;— the length of the permutations $a$ and $b$. The second line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \leq a_i \leq n$)&nbsp;— permutation $a$. The third line contains $b$ in a similar format. </p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2\cdot10^5$.</p>

## Output

<p>For each test case, output two permutations $a'$ and $b'$ (in the same format as in the input)&nbsp;— the permutations after all operations. The total number of inversions in $a'$ and $b'$ should be the minimum possible among all pairs of permutations that can be obtained using operations from the statement.</p><p>If there are multiple solutions, print any of them.</p>





```input1|2,3,4,8,9,10
3
5
1 2 3 4 5
5 4 3 2 1
3
3 1 2
3 1 2
6
2 5 6 1 3 4
1 5 3 6 2 4
```




```output1
3 2 5 1 4
3 4 1 5 2
1 2 3
1 2 3
2 3 4 6 5 1
1 2 4 3 5 6
```



## Note

<p>In the first test case, the minimum possible number of inversions is $10$.</p><p>In the second test case, we can sort both permutations at the same time. For this, the following operations can be done:</p><ul> <li> Swap the elements in the positions $1$ and $3$ in both permutations. After the operation, $a =$ [$2,1,3$], $b =$ [$2,1,3$]. </li><li> Swap the elements in the positions $1$ and $2$. After the operations, $a$ and $b$ are sorted. </li></ul><p>In the third test case, the minimum possible number of inversions is $7$.</p>
