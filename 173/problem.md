## Description

<div><p>Theofanis is busy after his <a href="https://codeforces.com/contest/1594/problem/A">last contest</a>, as now, he has to deliver many halloumis all over the world. He stored them inside $n$ boxes and each of which has some number $a_i$ written on it. </p><p>He wants to sort them in non-decreasing order based on their number, however, his machine works in a strange way. It can only reverse any subarray$^{\dagger}$ of boxes with length <span class="tex-font-style-bf">at most</span> $k$.</p><p>Find if it's possible to sort the boxes using <span class="tex-font-style-bf">any number of reverses</span>.</p><p>$^{\dagger}$ Reversing a subarray means choosing two indices $i$ and $j$ (where $1 \le i \le j \le n$) and changing the array $a_1, a_2, \ldots, a_n$ to $a_1, a_2, \ldots, a_{i-1}, \; a_j, a_{j-1}, \ldots, a_i, \; a_{j+1}, \ldots, a_{n-1}, a_n$. The length of the subarray is then $j - i + 1$.</p></div><div class="input-specification"><p>The first line contains a single integer $t$ ($1 \le t \le 100$)&nbsp;— the number of test cases.</p><p>Each test case consists of two lines. </p><p>The first line of each test case contains two integers $n$ and $k$ ($1 \le k \le n \le 100$)&nbsp;— the number of boxes and the length of the maximum reverse that Theofanis can make. </p><p>The second line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le 10^{9}$)&nbsp;— the number written on each box.</p></div><div class="output-specification"><p>For each test case, print <span class="tex-font-style-tt">YES</span> (case-insensitive), if the array can be sorted in non-decreasing order, or <span class="tex-font-style-tt">NO</span> (case-insensitive) otherwise.</p></div>

## Input

<p>The first line contains a single integer $t$ ($1 \le t \le 100$)&nbsp;— the number of test cases.</p><p>Each test case consists of two lines. </p><p>The first line of each test case contains two integers $n$ and $k$ ($1 \le k \le n \le 100$)&nbsp;— the number of boxes and the length of the maximum reverse that Theofanis can make. </p><p>The second line contains $n$ integers $a_1, a_2, \ldots, a_n$ ($1 \le a_i \le 10^{9}$)&nbsp;— the number written on each box.</p>

## Output

<p>For each test case, print <span class="tex-font-style-tt">YES</span> (case-insensitive), if the array can be sorted in non-decreasing order, or <span class="tex-font-style-tt">NO</span> (case-insensitive) otherwise.</p>





```input1|2,3,6,7,10,11
5
3 2
1 2 3
3 1
9 9 9
4 4
6 4 2 1
4 3
10 3 830 14
2 1
3 1
```




```output1
YES
YES
YES
YES
NO
```



## Note

<p>In the first two test cases, the boxes are already sorted in non-decreasing order.</p><p>In the third test case, we can reverse the whole array.</p><p>In the fourth test case, we can reverse the first two boxes and the last two boxes.</p><p>In the fifth test case, it can be shown that it's impossible to sort the boxes.</p>
