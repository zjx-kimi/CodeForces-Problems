## Description

<div><p>Some permutation of length $n$ is guessed.</p><p>You are given the indices of its prefix maximums and suffix maximums.</p><p>Recall that a permutation of length $k$ is an array of size $k$ such that each integer from $1$ to $k$ occurs exactly once.</p><p>Prefix maximums are the elements that are the maximum on the prefix ending at that element. More formally, the element $a_i$ is a prefix maximum if $a_i &gt; a_j$ for every $j &lt; i$.</p><p>Similarly, suffix maximums are defined, the element $a_i$ is a suffix maximum if $a_i &gt; a_j$ for every $j &gt; i$.</p><p>You need to output the number of different permutations that could have been guessed.</p><p>As this number can be very large, output the answer modulo $10^9 + 7$.</p></div><div class="input-specification"><p>Each test consists of several test cases. The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. Then follows the description of the test cases.</p><p>The first line of each test case contains three integers $n, m_1$ and $m_2$ ($1 \le m_1, m_2 \le n \le 2 \cdot 10^5$)&nbsp;— the length of the permutation, the number of prefix maximums, and the number of suffix maximums, respectively.</p><p>The second line of each test case contains $m_1$ integers $p_1 &lt; p_2 &lt; \ldots &lt; p_{m_1}$ ($1 \le p_i \le n$)&nbsp;— the indices of the prefix maximums in increasing order.</p><p>The third line of each test case contains $m_2$ integers $s_1 &lt; s_2 &lt; \ldots &lt; s_{m_2}$ ($1 \le s_i \le n$)&nbsp;— the indices of the suffix maximums in increasing order.</p><p>It is guaranteed that the sum of the values of $n$ for all test cases does not exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, output a single integer on a separate line&nbsp;— the number of suitable permutations modulo $10^9 + 7$.</p></div>

## Input

<p>Each test consists of several test cases. The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases. Then follows the description of the test cases.</p><p>The first line of each test case contains three integers $n, m_1$ and $m_2$ ($1 \le m_1, m_2 \le n \le 2 \cdot 10^5$)&nbsp;— the length of the permutation, the number of prefix maximums, and the number of suffix maximums, respectively.</p><p>The second line of each test case contains $m_1$ integers $p_1 &lt; p_2 &lt; \ldots &lt; p_{m_1}$ ($1 \le p_i \le n$)&nbsp;— the indices of the prefix maximums in increasing order.</p><p>The third line of each test case contains $m_2$ integers $s_1 &lt; s_2 &lt; \ldots &lt; s_{m_2}$ ($1 \le s_i \le n$)&nbsp;— the indices of the suffix maximums in increasing order.</p><p>It is guaranteed that the sum of the values of $n$ for all test cases does not exceed $2 \cdot 10^5$.</p>

## Output

<p>For each test case, output a single integer on a separate line&nbsp;— the number of suitable permutations modulo $10^9 + 7$.</p>





```input1|2,3,4,8,9,10,14,15,16
6
1 1 1
1
1
4 2 3
1 2
2 3 4
3 3 1
1 2 3
3
5 3 4
1 2 3
2 3 4 5
20 5 4
1 2 3 4 12
12 13 18 20
6 2 3
1 3
3 4 6
```




```output1
1
3
1
0
317580808
10
```



## Note

<p>The following permutations are suitable for the second set of input data:</p><ul> <li> $[1, 4, 3, 2]$ </li><li> $[2, 4, 3, 1]$ </li><li> $[3, 4, 2, 1]$ </li></ul><p>The following permutations are suitable for the sixth set of input data:</p><ul> <li> $[2, 1, 6, 5, 3, 4]$ </li><li> $[3, 1, 6, 5, 2, 4]$ </li><li> $[3, 2, 6, 5, 1, 4]$ </li><li> $[4, 1, 6, 5, 2, 3]$ </li><li> $[4, 2, 6, 5, 1, 3]$ </li><li> $[4, 3, 6, 5, 1, 2]$ </li><li> $[5, 1, 6, 4, 2, 3]$ </li><li> $[5, 2, 6, 4, 1, 3]$ </li><li> $[5, 3, 6, 4, 1, 2]$ </li><li> $[5, 4, 6, 3, 1, 2]$ </li></ul>
