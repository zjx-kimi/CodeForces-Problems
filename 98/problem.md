## Description

<div><p>You are given a matrix $a$, consisting of $n$ rows by $m$ columns. Each element of the matrix is equal to $0$ or $1$.</p><p>You can perform the following operation any number of times (possibly zero): choose an element of the matrix and replace it with either $0$ or $1$.</p><p>You are also given two arrays $A$ and $B$ (of length $n$ and $m$ respectively). After you perform the operations, the matrix should satisfy the following conditions:</p><ol> <li> the number of ones in the $i$-th row of the matrix should be exactly $A_i$ for every $i \in [1, n]$. </li><li> the number of ones in the $j$-th column of the matrix should be exactly $B_j$ for every $j \in [1, m]$. </li></ol><p>Calculate the minimum number of operations you have to perform.</p></div><div class="input-specification"><p>The first line contains two integers $n$ and $m$ ($2 \le n, m \le 50$).</p><p>Then $n$ lines follow. The $i$-th of them contains $m$ integers $a_{i,1}, a_{i,2}, \dots, a_{i,m}$ ($0 \le a_{i,j} \le 1$).</p><p>The next line contains $n$ integers $A_1, A_2, \dots, A_n$ ($0\le A_i\le m$).</p><p>The next line contains $m$ integers $B_1, B_2, \dots, B_m$ ($0\le B_i\le n$).</p></div><div class="output-specification"><p>Print one integer — the minimum number of operations you have to perform, or <span class="tex-font-style-tt">-1</span> if it is impossible.</p></div>

## Input

<p>The first line contains two integers $n$ and $m$ ($2 \le n, m \le 50$).</p><p>Then $n$ lines follow. The $i$-th of them contains $m$ integers $a_{i,1}, a_{i,2}, \dots, a_{i,m}$ ($0 \le a_{i,j} \le 1$).</p><p>The next line contains $n$ integers $A_1, A_2, \dots, A_n$ ($0\le A_i\le m$).</p><p>The next line contains $m$ integers $B_1, B_2, \dots, B_m$ ($0\le B_i\le n$).</p>

## Output

<p>Print one integer — the minimum number of operations you have to perform, or <span class="tex-font-style-tt">-1</span> if it is impossible.</p>





```input1|
3 3
0 0 0
0 0 0
0 0 0
1 1 1
1 1 1
```




```input2|
3 3
1 1 1
1 1 1
1 1 1
3 2 1
1 2 3
```




```input3|
2 2
0 0
0 0
1 2
0 1
```




```output1
3
```




```output2
3
```




```output3
-1
```


