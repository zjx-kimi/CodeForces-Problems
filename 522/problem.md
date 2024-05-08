## Description

<div><p>Two segments $[l_1, r_1]$ and $[l_2, r_2]$ intersect if there exists at least one $x$ such that $l_1 \le x \le r_1$ and $l_2 \le x \le r_2$.</p><p>An array of segments $[[l_1, r_1], [l_2, r_2], \dots, [l_k, r_k]]$ is called <span class="tex-font-style-bf">beautiful</span> if $k$ is even, and is possible to split the elements of this array into $\frac{k}{2}$ pairs in such a way that:</p><ul> <li> every element of the array belongs to exactly one of the pairs; </li><li> segments in each pair intersect with each other; </li><li> segments in different pairs do not intersect. </li></ul><p>For example, the array $[[2, 4], [9, 12], [2, 4], [7, 7], [10, 13], [6, 8]]$ is beautiful, since it is possible to form $3$ pairs as follows:</p><ul> <li> the first element of the array (segment $[2, 4]$) and the third element of the array (segment $[2, 4]$); </li><li> the second element of the array (segment $[9, 12]$) and the fifth element of the array (segment $[10, 13]$); </li><li> the fourth element of the array (segment $[7, 7]$) and the sixth element of the array (segment $[6, 8]$). </li></ul><p>As you can see, the segments in each pair intersect, and no segments from different pairs intersect.</p><p>You are given an array of $n$ segments $[[l_1, r_1], [l_2, r_2], \dots, [l_n, r_n]]$. You have to remove the minimum possible number of elements from this array so that the resulting array is beautiful.</p></div><div class="input-specification"><p>The first line contains one integer $t$ ($1 \le t \le 1000$) — the number of test cases.</p><p>The first line of each test case contains one integer $n$ ($2 \le n \le 2000$) — the number of segments in the array. Then, $n$ lines follow, the $i$-th of them contains two integers $l_i$ and $r_i$ ($0 \le l_i \le r_i \le 10^9$) denoting the $i$-th segment.</p><p>Additional constraint on the input: the sum of $n$ over all test cases does not exceed $2000$.</p></div><div class="output-specification"><p>For each test case, print one integer — the minimum number of elements you have to remove so that the resulting array is beautiful.</p></div>

## Input

<p>The first line contains one integer $t$ ($1 \le t \le 1000$) — the number of test cases.</p><p>The first line of each test case contains one integer $n$ ($2 \le n \le 2000$) — the number of segments in the array. Then, $n$ lines follow, the $i$-th of them contains two integers $l_i$ and $r_i$ ($0 \le l_i \le r_i \le 10^9$) denoting the $i$-th segment.</p><p>Additional constraint on the input: the sum of $n$ over all test cases does not exceed $2000$.</p>

## Output

<p>For each test case, print one integer — the minimum number of elements you have to remove so that the resulting array is beautiful.</p>





```input1|2,3,4,5,6,7,8,9,16,17,18,19,20
3
7
2 4
9 12
2 4
7 7
4 8
10 13
6 8
5
2 2
2 8
0 10
1 2
5 6
4
1 1
2 2
3 3
4 4
```




```output1
1
3
4
```



## Note

<p>In the first test case of the example, it is enough to delete the $5$-th element of the array of segments. Then you get the array $[[2, 4], [9, 12], [2, 4], [7, 7], [10, 13], [6, 8]]$, which is beautiful.</p><p>In the second test case of the example, you can delete the $1$-st, $3$-rd and $4$-th element of the array. Then you get the array $[[2, 8], [5, 6]]$, which is beautiful.</p><p>In the third test case of the example, you have to delete the whole array.</p>
