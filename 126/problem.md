## Description

<div><div class="epigraph"><div class="epigraph-text"><span class="tex-font-style-it"><a href="https://soundcloud.com/penehlopeexd/keygen-8-dubmood">Dubmood - Keygen 8</a></span></div><div class="epigraph-source">⠀</div></div><p>You are given a permutation $p_1, p_2, \dots, p_n$ of $[1, 2, \dots, n]$. You can perform the following operation some (possibly $0$) times:</p><ul> <li> choose a subarray $[l, r]$ of even length; </li><li> swap $a_l$, $a_{l+1}$; </li><li> swap $a_{l+2}$, $a_{l+3}$ (if $l+3 \leq r$); </li><li> $\dots$ </li><li> swap $a_{r-1}$, $a_r$. </li></ul><p>Sort the permutation in at most $10^6$ operations. You do not need to minimize the number of operations.</p></div><div class="input-specification"><p>The first line contains a single integer $n$ ($2 \le n \le 3 \cdot 10^5$)&nbsp;— the length of the permutation.</p><p>The second line contains $n$ integers $p_1, p_2, \ldots, p_n$ ($1 \le p_i \le n$, the $p_i$ are distinct)&nbsp;— the permutation before performing the operations.</p></div><div class="output-specification"><p>Output your operations in the following format.</p><p>The first line should contain an integer $k$ ($0 \le k \le 10^6$)&nbsp;— the number of operations.</p><p>The next $k$ lines represent the $k$ operations in order. Each of these $k$ lines should contain two integers $l$ and $r$ ($1 \leq l &lt; r \leq n$, $r-l+1$ must be even)&nbsp;— the corresponding operation consists in choosing the subarray $[l, r]$ and swapping its elements according to the problem statement.</p><p>After all the operations, $a_i = i$ must be true for each $i$ ($1 \leq i \leq n$).</p></div>

## Input

<p>The first line contains a single integer $n$ ($2 \le n \le 3 \cdot 10^5$)&nbsp;— the length of the permutation.</p><p>The second line contains $n$ integers $p_1, p_2, \ldots, p_n$ ($1 \le p_i \le n$, the $p_i$ are distinct)&nbsp;— the permutation before performing the operations.</p>

## Output

<p>Output your operations in the following format.</p><p>The first line should contain an integer $k$ ($0 \le k \le 10^6$)&nbsp;— the number of operations.</p><p>The next $k$ lines represent the $k$ operations in order. Each of these $k$ lines should contain two integers $l$ and $r$ ($1 \leq l &lt; r \leq n$, $r-l+1$ must be even)&nbsp;— the corresponding operation consists in choosing the subarray $[l, r]$ and swapping its elements according to the problem statement.</p><p>After all the operations, $a_i = i$ must be true for each $i$ ($1 \leq i \leq n$).</p>





```input1|
5
2 5 4 1 3
```




```input2|
9
1 2 3 4 5 6 7 8 9
```




```input3|
10
6 4 2 3 8 10 9 1 5 7
```




```output1
5
1 4
1 2
2 5
1 4
4 5
```




```output2
0
```




```output3
15
1 8
6 9
1 8
3 10
1 10
1 10
1 6
6 9
6 9
2 7
9 10
5 10
1 6
2 9
1 10
```



## Note

<p>In the first test: </p><ul> <li> At the beginning, $p = [2, 5, 4, 1, 3]$. </li><li> In the first operation, you can choose $[l, r] = [1, 4]$. Then, $(a_1, a_2)$ are swapped and $(a_3, a_4)$ are swapped. The new permutation is $p = [5, 2, 1, 4, 3]$. </li><li> In the second operation, you can choose $[l, r] = [1, 2]$. Then, $(a_1, a_2)$ are swapped. The new permutation is $p = [2, 5, 1, 4, 3]$. </li><li> In the third operation, you can choose $[l, r] = [2, 5]$. Then, $(a_2, a_3)$ are swapped and $(a_4, a_5)$ are swapped. The new permutation is $p = [2, 1, 5, 3, 4]$. </li><li> In the fourth operation, you can choose $[l, r] = [1, 4]$. Then, $(a_1, a_2)$ are swapped and $(a_3, a_4)$ are swapped. The new permutation is $p = [1, 2, 3, 5, 4]$. </li><li> In the fifth operation, you can choose $[l, r] = [4, 5]$. Then, $(a_4, a_5)$ are swapped. The new permutation is $p = [1, 2, 3, 4, 5]$, which is sorted. </li></ul><p>In the second test, the permutation is already sorted, so you do not need to perform any operation.</p>
