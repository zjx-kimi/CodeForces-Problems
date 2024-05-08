## Description

<div><p><span class="tex-font-style-bf">This is hard version of the problem, it differs from the easy one only by constraints on $n$ and $k$</span>.</p><p>Vlad found a row of $n$ tiles and the integer $k$. The tiles are indexed from left to right and the $i$-th tile has the color $c_i$. After a little thought, he decided what to do with it.</p><p>You can start from any tile and jump to any number of tiles <span class="tex-font-style-bf">right</span>, forming the path $p$. Let's call the path $p$ of length $m$ <span class="tex-font-style-it">nice</span> if:</p><ul> <li> $p$ can be divided into blocks of length exactly $k$, that is, $m$ is divisible by $k$; </li><li> $c_{p_1} = c_{p_2} = \ldots = c_{p_k}$; </li><li> $c_{p_{k+1}} = c_{p_{k+2}} = \ldots = c_{p_{2k}}$; </li><li> $\ldots$ </li><li> $c_{p_{m-k+1}} = c_{p_{m-k+2}} = \ldots = c_{p_{m}}$; </li></ul><p>Your task is to find the number of <span class="tex-font-style-it">nice</span> paths of <span class="tex-font-style-bf">maximum</span> length. Since this number may be too large, print it modulo $10^9 + 7$.</p></div><div class="input-specification"><p>The first line of each test contains the integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases in the test.</p><p>The first line of each test case contains two integers $n$ and $k$ ($1 \le k \le n \le 5000$) — the number of tiles in a row and the length of the block.</p><p>The second line of each test case contains $n$ integers $c_1, c_2, c_3, \dots, c_n$ ($1 \le c_i \le n$) — tile colors.</p><p>It is guaranteed that the sum of $n^2$ over all test cases does not exceed $25 \cdot 10^6$.</p></div><div class="output-specification"><p>Print $t$ numbers, each of which is the answer to the corresponding test case&nbsp;— the number of <span class="tex-font-style-it">nice</span> paths of maximum length modulo $10^9 + 7$.</p></div>

## Input

<p>The first line of each test contains the integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of test cases in the test.</p><p>The first line of each test case contains two integers $n$ and $k$ ($1 \le k \le n \le 5000$) — the number of tiles in a row and the length of the block.</p><p>The second line of each test case contains $n$ integers $c_1, c_2, c_3, \dots, c_n$ ($1 \le c_i \le n$) — tile colors.</p><p>It is guaranteed that the sum of $n^2$ over all test cases does not exceed $25 \cdot 10^6$.</p>

## Output

<p>Print $t$ numbers, each of which is the answer to the corresponding test case&nbsp;— the number of <span class="tex-font-style-it">nice</span> paths of maximum length modulo $10^9 + 7$.</p>





```input1|2,3,6,7,10,11
5
5 2
1 2 3 4 5
7 2
1 3 1 3 3 1 3
11 4
1 1 1 1 1 1 1 1 1 1 1
5 2
1 1 2 2 2
5 1
1 2 3 4 5
```




```output1
1
4
165
3
1
```



## Note

<p>In the first sample, it is impossible to make a <span class="tex-font-style-it">nice</span> path with a length greater than $0$.</p><p>In the second sample, we are interested in the following paths:</p><ul> <li> $1 \rightarrow 3 \rightarrow 4 \rightarrow 5$ </li><li> $2 \rightarrow 4 \rightarrow 5 \rightarrow 7$ </li><li> $1 \rightarrow 3 \rightarrow 5 \rightarrow 7$ </li><li> $1 \rightarrow 3 \rightarrow 4 \rightarrow 7$ </li></ul><p>In the third example, any path of length $8$ is <span class="tex-font-style-it">nice</span>.</p>
