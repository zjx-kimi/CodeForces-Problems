## Description

<div><p><span class="tex-font-style-it">This is a hard version of the problem. The constraints of $t$, $n$, $k$ are the only difference between versions.</span></p><p>You have a device with two CPUs. You also have $k$ programs, numbered $1$ through $k$, that you can run on the CPUs. </p><p>The $i$-th program ($1 \le i \le k$) takes $cold_i$ seconds to run on some CPU. However, if the last program we ran on this CPU was also program $i$, it only takes $hot_i$ seconds ($hot_i \le cold_i$). Note that this only applies if we run program $i$ multiple times consecutively &nbsp;— if we run program $i$, then some different program, then program $i$ again, it will take $cold_i$ seconds the second time.</p><p>You are given a sequence $a_1, a_2, \ldots, a_n$ of length $n$, consisting of integers from $1$ to $k$. You need to use your device to run programs $a_1, a_2, \ldots, a_n$ in sequence. For all $2 \le i \le n$, you cannot start running program $a_i$ until program $a_{i - 1}$ has completed.</p><p>Find the minimum amount of time needed to run all programs $a_1, a_2, \ldots, a_n$ in sequence.</p></div><div class="input-specification"><p>Input consists of multiple test cases. The first line contains a single integer $t$, the number of test cases ($1 \le t \le 10^5$).</p><p>The first line of each test case contains $n$ and $k$ ($1 \le n, k \le 3 \cdot 10^5$).</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le k$).</p><p>The third line of each test case contains $k$ integers $cold_1, cold_2, \ldots, cold_k$ ($1 \le cold_i \le 10^9$).</p><p>The fourth line of each test case contains $k$ integers $hot_1, hot_2, \ldots, hot_k$ ($1 \le hot_i \le cold_i$).</p><p>It is guaranteed the sum of $n$ and the sum of $k$ over all test cases do not exceed $3 \cdot 10^5$.</p></div><div class="output-specification"><p>For each test case, print the minimum time needed to run all programs in the given order.</p></div>

## Input

<p>Input consists of multiple test cases. The first line contains a single integer $t$, the number of test cases ($1 \le t \le 10^5$).</p><p>The first line of each test case contains $n$ and $k$ ($1 \le n, k \le 3 \cdot 10^5$).</p><p>The second line of each test case contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le k$).</p><p>The third line of each test case contains $k$ integers $cold_1, cold_2, \ldots, cold_k$ ($1 \le cold_i \le 10^9$).</p><p>The fourth line of each test case contains $k$ integers $hot_1, hot_2, \ldots, hot_k$ ($1 \le hot_i \le cold_i$).</p><p>It is guaranteed the sum of $n$ and the sum of $k$ over all test cases do not exceed $3 \cdot 10^5$.</p>

## Output

<p>For each test case, print the minimum time needed to run all programs in the given order.</p>





```input1|2,3,4,5,10,11,12,13,18,19,20,21,26,27,28,29,34,35,36,37
9
3 2
1 2 2
3 2
2 1
4 2
1 2 1 2
5 3
2 1
4 3
1 2 3 1
100 100 100
1 1 1
5 2
2 1 2 1 1
65 45
54 7
5 3
1 3 2 1 2
2 2 2
1 1 1
5 1
1 1 1 1 1
1000000000
999999999
5 6
1 6 1 4 1
3 6 4 1 4 5
1 1 1 1 4 1
1 3
3
4 5 6
1 2 3
8 3
3 3 3 1 2 3 2 1
10 10 8
10 10 5
```




```output1
6
11
301
225
8
4999999996
11
6
63
```



## Note

<p>In the first test case, we can do the following: </p><ul> <li> Run program $a_1 = 1$ on CPU $1$. It takes $cold_1 = 3$ seconds to run. </li><li> Run program $a_2 = 2$ on CPU $2$. It takes $cold_2 = 2$ seconds to run. </li><li> Run program $a_3 = 2$ on CPU $2$. The last program run on this CPU was also program $2$, so it takes $hot_2 = 1$ second to run. </li></ul><p>In total, we need $3 + 2 + 1 = 6$ seconds to run them all. We can show this is optimal.</p><p>In the second test case, we can use do the following: </p><ul> <li> Run program $a_1 = 1$ on CPU $1$. It takes $cold_1 = 5$ seconds to run. </li><li> Run program $a_2 = 2$ on CPU $2$. It takes $cold_2 = 3$ seconds to run. </li><li> Run program $a_3 = 1$ on CPU $1$. The last program run on this CPU was also program $1$, so it takes $hot_1 = 2$ seconds to run. </li><li> Run program $a_4 = 2$ on CPU $2$. The last program run on this CPU was also program $2$, so it takes $hot_2 = 1$ second to run. </li></ul><p>In total, we need $5 + 3 + 2 + 1 = 11$ seconds. We can show this is optimal.</p>
