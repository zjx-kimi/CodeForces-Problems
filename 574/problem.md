## Description

<div><p><span class="tex-font-style-bf">The only difference between easy and hard versions is the maximum values of $n$ and $q$</span>.</p><p>You are given an array, consisting of $n$ integers. Initially, all elements are red.</p><p>You can apply the following operation to the array multiple times. During the $i$-th operation, you select an element of the array; then: </p><ul> <li> if the element is red, it increases by $i$ and becomes blue; </li><li> if the element is blue, it decreases by $i$ and becomes red. </li></ul><p>The operations are numbered from $1$, i. e. during the first operation some element is changed by $1$ and so on.</p><p>You are asked $q$ queries of the following form: </p><ul> <li> given an integer $k$, what can the largest minimum in the array be if you apply <span class="tex-font-style-bf">exactly</span> $k$ operations to it? </li></ul><p>Note that the operations don't affect the array between queries, all queries are asked on the initial array $a$.</p></div><div class="input-specification"><p>The first line contains two integers $n$ and $q$ ($1 \le n, q \le 1000$)&nbsp;— the number of elements in the array and the number of queries.</p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le 10^9$).</p><p>The third line contains $q$ integers $k_1, k_2, \dots, k_q$ ($1 \le k_j \le 10^9$).</p></div><div class="output-specification"><p>For each query, print a single integer&nbsp;— the largest minimum that the array can have after you apply <span class="tex-font-style-bf">exactly</span> $k$ operations to it.</p></div>

## Input

<p>The first line contains two integers $n$ and $q$ ($1 \le n, q \le 1000$)&nbsp;— the number of elements in the array and the number of queries.</p><p>The second line contains $n$ integers $a_1, a_2, \dots, a_n$ ($1 \le a_i \le 10^9$).</p><p>The third line contains $q$ integers $k_1, k_2, \dots, k_q$ ($1 \le k_j \le 10^9$).</p>

## Output

<p>For each query, print a single integer&nbsp;— the largest minimum that the array can have after you apply <span class="tex-font-style-bf">exactly</span> $k$ operations to it.</p>





```input1
4 10
5 2 8 4
1 2 3 4 5 6 7 8 9 10
```




```input2
5 10
5 2 8 4 4
1 2 3 4 5 6 7 8 9 10
```




```input3
2 5
2 3
10 6 8 1 3
```




```output1
3 4 5 6 7 8 8 10 8 12
```




```output2
3 4 5 6 7 8 9 8 11 8
```




```output3
10 7 8 3 3
```


