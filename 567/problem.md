## Description

<div><p>You are given a permutation $p$ of length $n$.</p><p>A permutation is an array consisting of $n$ distinct integers from $1$ to $n$ in any order. For example, $\{2,3,1,5,4\}$ is a permutation, while $\{1,2,2\}$ is not (since $2$ appears twice), and $\{1,3,4\}$ is also not a permutation (as $n=3$, but the array contains $4$).</p><p>To the permutation $p$, you need to apply the following operation <span class="tex-font-style-bf">exactly once</span>:</p><ul> <li> First you choose a segment $[l, r]$ ($1 \le l \le r \le n$, a segment is a continuous sequence of numbers $\{p_l, p_{l+1}, \ldots, p_{r-1}, p_r\}$) and reverse it. Reversing a segment means swapping pairs of numbers $(p_l, p_r)$, $(p_{l+1}, p_{r-1})$, ..., $(p_{l + i}, p_{r - i})$ (where $l + i \le r - i$). </li><li> Then you swap the prefix and suffix: $[r+1, n]$ and $[1, l - 1]$ (note that these segments may be empty). </li></ul><p>For example, given $n = 5, p = \{2, \color{blue}{3}, \color{blue}{1}, 5, 4\}$, if you choose the segment $[l = 2, r = 3]$, after reversing the segment $p = \{\color{green}{2}, \color{blue}{1}, \color{blue}{3}, \color{green}{5}, \color{green}{4}\}$, then you swap the segments $[4, 5]$ and $[1, 1]$. Thus, $p = \{\color{green}{5}, \color{green}{4}, 1, 3, \color{green}{2}\}$. It can be shown that this is the maximum possible result for the given permutation.</p><p>You need to output the lexicographically <span class="tex-font-style-bf">maximum</span> permutation that can be obtained by applying the operation described <span class="tex-font-style-bf">exactly once</span>.</p><p>A permutation $a$ is lexicographically greater than permutation $b$ if there exists an $i$ ($1 \le i \le n$) such that $a_j = b_j$ for $1 \le j &lt; i$ and $a_i &gt; b_i$.</p></div><div class="input-specification"><p>The first line of the input contains a single integer $t$ ($1 \le t \le 1000$)&nbsp;— the number of test cases.</p><p>Then the descriptions of the test cases follow.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 2000$)&nbsp;— the size of the permutation.</p><p>The second line of each test case contains $n$ integers: $p_1, p_2, \ldots, p_n$ ($1 \le p_i \le n$)&nbsp;— the permutation $p$ itself.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2000$.</p></div><div class="output-specification"><p>For each test case, output in a separate line the lexicographically <span class="tex-font-style-bf">maximum</span> permutation of length $n$ that can be obtained from $p$ by applying the operation described in the problem <span class="tex-font-style-bf">exactly once</span>.</p></div>

## Input

<p>The first line of the input contains a single integer $t$ ($1 \le t \le 1000$)&nbsp;— the number of test cases.</p><p>Then the descriptions of the test cases follow.</p><p>The first line of each test case contains a single integer $n$ ($1 \le n \le 2000$)&nbsp;— the size of the permutation.</p><p>The second line of each test case contains $n$ integers: $p_1, p_2, \ldots, p_n$ ($1 \le p_i \le n$)&nbsp;— the permutation $p$ itself.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $2000$.</p>

## Output

<p>For each test case, output in a separate line the lexicographically <span class="tex-font-style-bf">maximum</span> permutation of length $n$ that can be obtained from $p$ by applying the operation described in the problem <span class="tex-font-style-bf">exactly once</span>.</p>





```input1|2,3,6,7,10,11,14,15,18,19
9
5
2 3 1 5 4
9
4 1 6 7 2 8 5 3 9
4
4 3 2 1
2
2 1
6
3 2 4 1 5 6
7
3 2 1 5 7 6 4
10
10 2 5 6 1 9 3 8 4 7
4
4 2 1 3
1
1
```




```output1
5 4 1 3 2 
9 4 1 6 7 2 8 5 3 
3 2 1 4 
1 2 
6 5 3 2 4 1 
7 6 4 5 3 2 1 
9 3 8 4 7 1 10 2 5 6 
3 4 2 1 
1
```



## Note

<p>The first example is explained in the problem statement.</p><p>In the second example, the segment $[l = 9, r = 9]$ should be chosen.</p><p>In the third example, the segment $[l = 1, r = 1]$ should be chosen.</p><p>In the fourth example, the segment $[l = 1, r = 2]$ should be chosen.</p><p>In the fifth example, the segment $[l = 5, r = 6]$ should be chosen.</p><p>In the sixth example, the segment $[l = 4, r = 4]$ should be chosen.</p><p>In the seventh example, the segment $[l = 5, r = 5]$ should be chosen.</p>
