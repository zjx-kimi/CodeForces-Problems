## Description

<div><p>An array $a_1,\dots,a_n$ of length $n$ is initially all blank. There are $n$ updates where one entry of $a$ is updated to some number, such that $a$ becomes a permutation of $1,2,\dots,n$ after all the updates.</p><p>After each update, find the number of ways (modulo $998\,244\,353$) to fill in the remaining blank entries of $a$ so that $a$ becomes a permutation of $1,2,\dots,n$ and all cycle lengths in $a$ are multiples of $3$.</p><p>A permutation of $1,2,\dots,n$ is an array of length $n$ consisting of $n$ distinct integers from $1$ to $n$ in arbitrary order. A <span class="tex-font-style-it">cycle</span> in a permutation $a$ is a sequence of pairwise distinct integers $(i_1,\dots,i_k)$ such that $i_2 = a_{i_1},i_3 = a_{i_2},\dots,i_k = a_{i_{k-1}},i_1 = a_{i_k}$. The length of this cycle is the number $k$, which is a multiple of $3$ if and only if $k \equiv 0 \pmod 3$.</p></div><div class="input-specification"><p>The first line contains a single integer $n$ ($3 \le n \le 3 \cdot 10^5$, $n \equiv 0 \pmod 3$).</p><p>The $i$-th of the next $n$ lines contains two integers $x_i$ and $y_i$, representing that the $i$-th update changes $a_{x_i}$ to $y_i$.</p><p>It is guaranteed that $x_1,\dots,x_n$ and $y_1,\dots,y_n$ are permutations of $1,2,\dots,n$, i.e. $a$ becomes a permutation of $1,2,\dots,n$ after all the updates.</p></div><div class="output-specification"><p>Output $n$ lines: the number of ways (modulo $998\,244\,353$) after the first $1,2,\dots,n$ updates.</p></div>

## Input

<p>The first line contains a single integer $n$ ($3 \le n \le 3 \cdot 10^5$, $n \equiv 0 \pmod 3$).</p><p>The $i$-th of the next $n$ lines contains two integers $x_i$ and $y_i$, representing that the $i$-th update changes $a_{x_i}$ to $y_i$.</p><p>It is guaranteed that $x_1,\dots,x_n$ and $y_1,\dots,y_n$ are permutations of $1,2,\dots,n$, i.e. $a$ becomes a permutation of $1,2,\dots,n$ after all the updates.</p>

## Output

<p>Output $n$ lines: the number of ways (modulo $998\,244\,353$) after the first $1,2,\dots,n$ updates.</p>





```input1
6
3 2
1 4
4 5
2 6
5 1
6 3
```




```input2
3
1 1
2 3
3 2
```




```input3
18
1 2
2 3
3 4
4 5
5 6
6 7
7 8
8 9
9 10
10 11
11 12
12 13
13 14
14 15
15 16
16 17
17 18
18 1
```




```output1
32
8
3
2
1
1
```




```output2
0
0
0
```




```output3
671571067
353924552
521242461
678960117
896896000
68992000
6272000
627200
62720
7840
1120
160
32
8
2
1
1
1
```



## Note

<p>In the first sample, for example, after the $3$rd update the $3$ ways to complete the permutation $a = [4,\_,2,5,\_,\_]$ are as follows: </p><ul> <li> $[4,1,2,5,6,3]$: The only cycle is $(1\,4\,5\,6\,3\,2)$, with length $6$. </li><li> $[4,6,2,5,1,3]$: The cycles are $(1\,4\,5)$ and $(2\,6\,3)$, with lengths $3$ and $3$. </li><li> $[4,6,2,5,3,1]$: The only cycle is $(1\,4\,5\,3\,2\,6)$, with length $6$. </li></ul><p>In the second sample, the first update creates a cycle of length $1$, so there are no ways to make all cycle lengths a multiple of $3$.</p>
