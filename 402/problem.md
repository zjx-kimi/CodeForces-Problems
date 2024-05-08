## Description

<div><p>You are given a permutation$^{\dagger}$ $p_1, p_2, \ldots, p_n$ of integers $1$ to $n$.</p><p>You can change the current permutation by applying the following operation several (possibly, zero) times:</p><ul> <li> choose some $x$ ($2 \le x \le n$); </li><li> create a new permutation by: <ul> <li> first, writing down all elements of $p$ that are less than $x$, without changing their order; </li><li> second, writing down all elements of $p$ that are greater than or equal to $x$, without changing their order; </li></ul> </li><li> replace $p$ with the newly created permutation. </li></ul><p>For example, if the permutation used to be $[6, 4, 3, 5, 2, 1]$ and you choose $x = 4$, then you will first write down $[3, 2, 1]$, then append this with $[6, 4, 5]$. So the initial permutation will be replaced by $[3, 2, 1, 6, 4, 5]$.</p><p>Find the minimum number of operations you need to achieve $p_i = i$ for $i = 1, 2, \ldots, n$. We can show that it is always possible to do so.</p><p>$^{\dagger}$ A permutation of length $n$ is an array consisting of $n$ distinct integers from $1$ to $n$ in arbitrary order. For example, $[2,3,1,5,4]$ is a permutation, but $[1,2,2]$ is not a permutation ($2$ appears twice in the array), and $[1,3,4]$ is also not a permutation ($n=3$ but there is $4$ in the array).</p></div><div class="input-specification"><p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 1000$). The description of the test cases follows.</p><p>The first line of each test case contains one integer $n$ ($1 \le n \le 100\,000$).</p><p>The second line of each test case contains $n$ integers $p_1, p_2, \ldots, p_n$ ($1 \le p_i \le n$). It is guaranteed that $p_1, p_2, \ldots, p_n$ is a permutation.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $100\,000$.</p></div><div class="output-specification"><p>For each test case, output the answer on a separate line.</p></div>

## Input

<p>Each test contains multiple test cases. The first line contains the number of test cases $t$ ($1 \le t \le 1000$). The description of the test cases follows.</p><p>The first line of each test case contains one integer $n$ ($1 \le n \le 100\,000$).</p><p>The second line of each test case contains $n$ integers $p_1, p_2, \ldots, p_n$ ($1 \le p_i \le n$). It is guaranteed that $p_1, p_2, \ldots, p_n$ is a permutation.</p><p>It is guaranteed that the sum of $n$ over all test cases does not exceed $100\,000$.</p>

## Output

<p>For each test case, output the answer on a separate line.</p>





```input1|2,3,6,7,10,11
5
1
1
2
2 1
6
6 4 3 5 2 1
3
3 1 2
19
10 19 7 1 17 11 8 5 12 9 4 18 14 2 6 15 3 16 13
```




```output1
0
1
4
1
7
```



## Note

<p>In the first test case, $n = 1$ and $p_1 = 1$, so there is nothing left to do.</p><p>In the second test case, we can choose $x = 2$ and we immediately obtain $p_1 = 1$, $p_2 = 2$.</p><p>In the third test case, we can achieve the minimum number of operations in the following way:</p><ol> <li> $x = 4$: $[6, 4, 3, 5, 2, 1] \rightarrow [3, 2, 1, 6, 4, 5]$; </li><li> $x = 6$: $[3, 2, 1, 6, 4, 5] \rightarrow [3, 2, 1, 4, 5, 6]$; </li><li> $x = 3$: $[3, 2, 1, 4, 5, 6] \rightarrow [2, 1, 3, 4, 5, 6]$; </li><li> $x = 2$: $[2, 1, 3, 4, 5, 6] \rightarrow [1, 2, 3, 4, 5, 6]$. </li></ol>
