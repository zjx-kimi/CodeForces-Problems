## Description

<div><p>Monocarp has got an array $a$ consisting of $n$ integers. Let's denote $k$ as the mathematic mean of these elements (note that it's possible that $k$ is not an integer). </p><p>The mathematic mean of an array of $n$ elements is the sum of elements divided by the number of these elements (i. e. sum divided by $n$).</p><p>Monocarp wants to delete exactly two elements from $a$ so that the mathematic mean of the remaining $(n - 2)$ elements is still equal to $k$.</p><p>Your task is to calculate the number of pairs of positions $[i, j]$ ($i &lt; j$) such that if the elements on these positions are deleted, the mathematic mean of $(n - 2)$ remaining elements is equal to $k$ (that is, it is equal to the mathematic mean of $n$ elements of the original array $a$).</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of testcases.</p><p>The first line of each testcase contains one integer $n$ ($3 \le n \le 2 \cdot 10^5$) — the number of elements in the array.</p><p>The second line contains a sequence of integers $a_1, a_2, \dots, a_n$ ($0 \le a_i \le 10^{9}$), where $a_i$ is the $i$-th element of the array.</p><p>The sum of $n$ over all testcases doesn't exceed $2 \cdot 10^5$.</p></div><div class="output-specification"><p>Print one integer — the number of pairs of positions $[i, j]$ ($i &lt; j$) such that if the elements on these positions are deleted, the mathematic mean of $(n - 2)$ remaining elements is equal to $k$ (that is, it is equal to the mathematic mean of $n$ elements of the original array $a$).</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 10^4$)&nbsp;— the number of testcases.</p><p>The first line of each testcase contains one integer $n$ ($3 \le n \le 2 \cdot 10^5$) — the number of elements in the array.</p><p>The second line contains a sequence of integers $a_1, a_2, \dots, a_n$ ($0 \le a_i \le 10^{9}$), where $a_i$ is the $i$-th element of the array.</p><p>The sum of $n$ over all testcases doesn't exceed $2 \cdot 10^5$.</p>

## Output

<p>Print one integer — the number of pairs of positions $[i, j]$ ($i &lt; j$) such that if the elements on these positions are deleted, the mathematic mean of $(n - 2)$ remaining elements is equal to $k$ (that is, it is equal to the mathematic mean of $n$ elements of the original array $a$).</p>





```input1
4
4
8 8 8 8
3
50 20 10
5
1 4 7 3 5
7
1 2 3 4 5 6 7
```




```output1
6
0
2
3
```



## Note

<p>In the first example, any pair of elements can be removed since all of them are equal.</p><p>In the second example, there is no way to delete two elements so the mathematic mean doesn't change.</p><p>In the third example, it is possible to delete the elements on positions $1$ and $3$, or the elements on positions $4$ and $5$.</p>
